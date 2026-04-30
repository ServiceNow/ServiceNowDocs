---
title: Configure a generic large language model \(LLM\) connector
description: Connect an external LLM to the ServiceNow AI Platform by using a generic LLM connector. With a connector, you can write your own prompts to send to the LLM and create your own generative AI capabilities.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure a generic large language model \(LLM\) connector

Connect an external LLM to the ServiceNow AI Platform by using a generic LLM connector. With a connector, you can write your own prompts to send to the LLM and create your own generative AI capabilities.

## Before you begin

You must configure API credentials for your LLM before setting up the connector. For more information, see [configure API credentials for a generic LLM](configure-api-credentials-for-a-generic-large-language-model-llm.md).

Role required: admin

## About this task

Generative AI Controller offers several base system connections to popular AI service providers such as Azure OpenAI and Google Vertex. However, you might want to incorporate an industry LLM, a case-specific LLM into your custom workflows, or an LLM that adheres to your organization's data handling policies.

**Note:** Generative AI Controller only supports text generation.

## Procedure

1.  In the navigation filter, go to the Generative AI Model Configuration \[sys\_generative\_ai\_model\_config\] table by entering `sys_generative_ai_model_config.list`.

2.  Select **New**.

3.  In the **Model** field, enter the name of the model.

    If you are using Azure OpenAI, then the model name is the deployment name of your resource.

4.  In the **Provider** field, select **Custom LLM**.

5.  In the **Connection and Credential Alias** field, select the alias that you created when you set up your credentials.

    If you haven't already configured your API credentials, see [configure API credentials for a generic large language model](configure-api-credentials-for-a-generic-large-language-model-llm.md) to learn how. ![Generative AI Model Config record with the Provider field set to Custom LLM and the Connection and Credentials Alias field set to My_Model_Alias.](../image/gai-connector-1.png)

6.  Create the model configuration by selecting **Submit**.

    The model configuration is associated with the API key of the external model.

7.  In the navigation filter, go to the Generative AI Configuration \[sys\_generative\_ai\_config\] table by entering `sys_generative_ai_config.list`.

8.  Select **New**.

9.  Select the list lookup icon \(![List lookup icon with magnifying glass.](../../now-assist-admin/image/na-list-lookup-icon.png)\) next to the **Definition** field.

10. In the Select the document modal, select a capability that you want to configure with the Custom LLM provider.

    For example, if you're configuring a Summarize capability, select **Summarize \(Custom LLM\)**.

11. Select **OK** to save your selection and close the modal.

12. In the **Model** field, choose the model configuration that you created in step 6.

    After you select a **Definition**, the **Model** field changes into a drop-down menu with options that use the Custom LLM provider. The model configuration that you made should appear in this list. If it doesn't, go back to step 1 and make sure that your model configuration has the **Provider** field set to **Custom LLM**.

13. In the **Prompt template** field, enter the prompt for the capability.

    The prompt template is the instruction that is sent to the LLM to execute a capability. Use two braces around the capability attribute names to incorporate them into the prompt template. For example, if you're configuring a Summarize capability, your prompt template could be `Summarize the following for me in a friendly and helpful tone: {{textToSummarize}}`. To learn which attributes are available to include in the prompt, go to the OneExtend Capability \[sys\_one\_extend\_capability\] table, find the record for the capability you're configuring, and look at the OneExtend Capability Attributes related list. ![Generative AI Configuration record with Definition, Model, and Prompt template fields filled in.](../image/gai-connector-2.png) ![Summarize capability record open with OneExtend Capability Attributes related list highlighted and the attributes identified: error, errorCode, provider, response, status, and textToSummarize.](../image/gai-connector-3.png) You might need to experiment with different prompts to determine what works best for your use cases.

14. Create the new Generative AI Configuration by selecting **Submit**.

15. In the navigation filter, go to the Generative AI Custom LLM Transformer \[sys\_generative\_ai\_custom\_llm\_transformer\] table by entering `sys_generative_ai_custom_llm_transformer`.

16. Select **New**.

17. Write transformer scripts.

    To have Generative AI Controller understand the format of the inputs and outputs of your custom LLM, you must write transformer scripts. When you create a transformer record, code and comments are provided for you to use as a guide while you edit. These scripts depend on the expected request and response objects that are interpreted by your model.

    For example, the Azure OpenAI request structure looks like the following script:

    ```
    {"messages": [{"role":"user", "content":"Summarize the following text: <<content>>"}], "max_tokens": 800, "temperature": 0.7}
    ```

    The request transformer script for that request structure is the following script:

    ```
    (function(inputs) {
        /* write code here to construct the request body and any custom headers needed using the inputs object.
        inputs structure: {
            prompt_data: object,
            request_data: object
        } */
        var requestData = inputs.request_data;    
        var promptData = inputs.prompt_data;
        var prompt = promptData.prompt;
        var model = promptData.model;
    
        // construct body using the inputs
        var body = {
            messages: [{
            "role": "user",
            "content": prompt
            }],
            max_tokens: parseInt(promptData.max_tokens),
            temperature: parseInt(promptData.temperature)    
        };
    
        //construct headers using the inputs
        var headers = {};                        
        return {
            body: body,
            headers: headers
        };
    })(inputs);
    ```

    The response structure from Azure OpenAI looks like this script:

    ```
    {
        "choices": [{
        "finish_reason": "stop",
        "index": 0,
        "message": {
            "content": "<<response>>",
            "role": "assistant"
            }
        }],
        "created": 1714994995,
        "id": "chatcmpl-9LqpXeLVXDAi6kciPfLeIDjmALeea",
        "model": "gpt-35-turbo-16k",
        "object": "chat.completion",
        "usage": {    
            "completion_tokens": 47,
            "prompt_tokens": 70,
            "total_tokens": 117
        }
    }
    ```

    Because of that response structure, the response transformer script looks like this script:

    ```
    (function(inputs) {
        /* write code here to transform the llm response into an array of text responses, using the inputs object
        inputs structure: {
            prompt_data: object,
            request_data: object,
            response_body: string,
            response_headers: string
        } */
        var requestData = inputs.request_data;
        var promptData = inputs.prompt_data;
        var responseBody = JSON.parse(inputs.response_body);
        gs.info("response : " + inputs.response_body);
        var responseTexts = [];
    
        // write code here to populate the responseTexts array.
        responseTexts.push(responseBody.choices[0].message.content);
    
        return responseTexts;
    
    })(inputs);
    ```

18. Create the transformer scripts by selecting **Submit**.


## Result

Your external LLM is connected to Generative AI Controller. You can use the AI service provider for generative AI capabilities on the ServiceNow AI Platform.

## What to do next

After you connect the LLM, you can set a provider for the generative AI capabilities of Generative AI Controller. The capabilities are Generic Prompt, Generate Content, Sentiment Analysis, and Summarize. For more information on choosing a provider, see [Set a provider for a generative AI capability](configure-a-provider-for-a-generative-ai-capability.md).

