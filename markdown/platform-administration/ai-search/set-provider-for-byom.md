---
title: Set a provider for embedding model
description: Determine which AI provider to use for your embedding model to work in the AI Search RAG application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/set-provider-for-byom.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring an external or custom embedding model, Semantic index configuration for indexed sources, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set a provider for embedding model

Determine which AI provider to use for your embedding model to work in the AI Search RAG application.

## Before you begin

Configure a connection and credential alias for your preferred provider. See [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connection-alias.md).

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_one_extend_capability.list` in the filter to go to the OneExtend Capabilities table.

2.  Select the **Bring Your Own Embedding Model** capability to configure.

3.  In the OneExtend Capability Definitions related list, select **New**.

4.  In the **Name** field, enter the name of the capability definition.

5.  In the **API type** field, select **system**.

6.  In the **API** field, select the search icon to select the document.

    1.  In the **Table name** field, select One API System Executor \[one\_api\_system\_executor\].

    2.  In the **Document** field, select **Generic Embedder**.

    3.  Select **OK**.

7.  In the Connection And Credential Alias, select the alias that you want to integrate with your custom embedding model.

8.  Select the **Advanced** option.

9.  Write pre-processing and post-processing scripts.

    To have AI Search RAG application understand the format of the inputs and outputs of your embedding model, you must write pre-processing and post-processing scripts. These scripts depend on the expected request and response objects that are interpreted by your model.

    For example, the Azure OpenAI request structure looks like the following script:

    ```
    {"messages": [{"role":"user", "content":"Summarize the following text: <<content>>"}], "max_tokens": 800, "temperature": 0.7}
    ```

    The preprocessor script for that request structure is the following script:

    ```
    (function(inputs) {
        /* write code here to transform capability input to definition input.*/     
    	     
    	inputs = JSON.parse(inputs);     
    	     
    	return inputs;     
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

    Because of that response structure, the response postprocessor script looks like this script:

    ```
    (function(inputs) {
        /* write code here to transform definition output to capability output.*/ to transform the llm response into an array of text responses, using the inputs object
        inputs structure: {
            inputs = JSON.parse(inputs);     
    	     
    	return inputs;   
    
    })(inputs);
    ```

10. Select **Submit**.


