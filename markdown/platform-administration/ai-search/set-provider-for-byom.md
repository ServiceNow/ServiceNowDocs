---
title: Set a provider for an embedding model
description: Determine which AI provider to use so that your embedding model can work in the AI Search Retrieval Augmented Generation \(RAG\) application.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring bring your own model \(BYOM\), Configuring an external or custom embedding model, AI Search Retrieval Augmented Generation \(RAG\), Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set a provider for an embedding model

Determine which AI provider to use so that your embedding model can work in the AI Search Retrieval Augmented Generation \(RAG\) application.

## Before you begin

Configure a connection and credential alias for your preferred provider. For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_one_extend_capability.list` in the filter to go to the OneExtend Capabilities table.

2.  Select the **Bring Your Own Embedding Model** capability.

3.  In the OneExtend Capability Definitions related list, select **New**.

4.  In the **Name** field, enter the name of the capability definition.

    For example, Embedding Generation \(Azure OpenAI\)

5.  In the **API type** field, select **system**.

6.  In the **API** field, select the search icon \(![Lookup documents using list.](../../../common/image/Banner_GlobalTextSearchIcon.png)\) to select the document.

    1.  In the **Table name** field, select the One API System Executor \[one\_api\_system\_executor\] table.

    2.  In the **Document** field, select **Generic Embedder**.

    3.  Select **OK**.

7.  In the **Connection And Credential Alias** field, select the alias that you want to integrate with your custom embedding model.

8.  Select the **Advanced** option.

9.  Create pre-processing and post-processing scripts.

    To enable your AI Search RAG application to work seamlessly with your embedding model, you must create pre-processing and post-processing scripts. These scripts help the AI Search RAG application understand the format of the data that your model expects and produces.

    The following example shows the preprocessor script for the Azure OpenAI request structure.

    ```
    (function(inputs) {                                                               //// inputs is the capability inputs which contains request.
                /* write code here to transform capability input to definition input.            
                 *{
    		"request": {                                                                  //request contains rawInput which will be system-provided.
    			"rawInput": {                                                          //rawInput contains passages(Array of text segments), type(Context of the input) and modelId(Name of the embedding model)
    				"passages": ["Sample text"],
    				"type": "ingest/query",
    				"model": "text-embedding-3-large"
    			},
    			"providerInput": {                                                     //providerInput should be populated using the relevant data from rawInput.passages.
    				"input": ["Sample text"]                                        //The field name "input" inside providerInput is provider-specific and rawInput.passages should be mapped to the appropriate field expected by your provider
    			}
    		}
    	  }
    	 try {
            var parsedInputs = JSON.parse(inputs);
            var request = parsedInputs.request;
            var rawInput = request.rawInput;
            var passagesArray = rawInput.passages;
            var type = rawInput.type;
    
            if (passagesArray && passagesArray.length > 0) {
                parsedInputs.request.providerInput = {};
                parsedInputs.request.providerInput.input = passagesArray;
            }
    
        } catch (ex) {
            gs.error("Exception occured while preprocessing of the inputs." + ex);
            throw new Error("Exception occured while OE preprocessing of the inputs : " + ex);
        }
    
        inputs = parsedInputs;
        return inputs;
    })(inputs);
    	 
    ```

    The following example shows the response postprocessor script for the Azure OpenAI request structure.

    ```
    (function(outputs) {
        /* write code here to transform definition output to capability output.
    	* outputs contains result from the provider definition implementation.
    	* Expected outputs format from provider definition implementation in success scenario:
    	   "result": {
    			"provider": "custom_embedding_model",
    			"logId": "0ee6f4f4ff112210b6e1ffffffffff03",
    			"status": "success",
    			"response": {"object":"list","data":[{"object":"embedding","index":0,"embedding":[0.008695375,0.0011188902]},{"object":"embedding","index":1,"embedding":[0.012572239,0.017366657]}],"model":"text-embedding-3-large","usage":{"prompt_tokens":4,"total_tokens":4}}
    	    }
    	* Expected outputs format from provider definition implementation in error scenario:
    	   "result": {
    			"responseHeaders": "[Content-Length: 224\r\n, Content-Type: application/json\r\n, apim-request-id: 72b1519e-a367-4f01-b249-8f37d35d50d3\r\n, Date: Thu, 01 May 2025 12:03:44 GMT\r\n]",
    			"responseBody": "{\"error\":{\"code\":\"401\",\"message\":\"Access denied due to invalid subscription key or wrong API endpoint. Make sure to provide a valid key for an active subscription and use a correct regional API endpoint for your resource.\"}}",
    			"provider": "custom_embedding_model",
    			"errorCode": "401",
    			"logId": "0ee6f4f4ff112210b6e1ffffffffff03",
    			"error": "PermissionDenied",
    			"status": "error"
    	   }
    	* Extract the embeddings from the response key of the provider result (in a successful scenario) and elevate it in the final output. Sample format for the same:
    	  "result": {
    			"provider": "custom_embedding_model",
    			"logId": "0ee6f4f4ff112210b6e1ffffffffff03",
    			"status": "success",
    			"response": {"object":"list","data":[{"object":"embedding","index":0,"embedding":[0.008695375,0.0011188902]},{"object":"embedding","index":1,"embedding":[0.012572239,0.017366657]}],"model":"text-embedding-3-large","usage":{"prompt_tokens":4,"total_tokens":4}}
    			"embeddings": [[0.008695375,0.0011188902], [0.012572239,0.017366657]]
    	   }
    	*/
        try {
            outputs = JSON.parse(outputs);
            var embeddingsArray = [];
    
            if (!gs.nil(outputs.result) && !gs.nil(outputs.result.response)) {
                var responseBody = outputs.result.response;
                if (!gs.nil(responseBody)) {
                    var data = JSON.parse(responseBody).data;
                    for (var i = 0; i < data.length; i++) {
                        var embeddingResponse = data[i];
                        if (!gs.nil(embeddingResponse) && !gs.nil(embeddingResponse.embedding))
                            embeddingsArray.push(embeddingResponse.embedding);
                    }
                }
    
                outputs.result.embeddings = embeddingsArray;
            }
        } catch (ex) {
            gs.error("Exception occured while OE postprocessing of the outputs = " + ex);
            outputs.result.status = "error";
            outputs.result.error = gs.getMessage("Exception occured while OE postprocessing of the outputs : " + ex);
        }
    
        return outputs;
    })(outputs);
    ```

10. Select **Submit**.


**Parent Topic:**[Configuring bring your own model \(BYOM\)](../concept/creating-byom.md)

