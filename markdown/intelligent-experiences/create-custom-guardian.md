---
title: Create a custom guardian
description: Create your own custom guardian to monitor and detect requests sent to LLM.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-02-13"
reading_time_minutes: 2
breadcrumb: [Configuring a Guardrail Service Provider, Now Assist Guardian, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Create a custom guardian

Create your own custom guardian to monitor and detect requests sent to LLM.

## Before you begin

Configure a connection and credential alias for your preferred provider. For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_generative_ai_custom_guardian_transformer_list.do` in the filter to go to the Generative AI Custom Guardian Transformer \[sys\_generative\_ai\_custom\_guardian\_transformer\_list.do\] table.

2.  Select **New**.

3.  In the **Name** field, enter the name of the custom guardian.

4.  Create a request transformer script.

    1.  In the **Request Transformer** filed, enable the **Turn on ECMAScript 2021 \(ES12\) mode** toggle to create script.

        The following example shows the request transformer script for the custom guardian request structure.

        ```
        ((function(inputs) {     
        	/*        
        	inputs structure: {     
        		prompt: object, The textual content that needs to be evaluated with guardian           
        		threshold_setting: object           
        		connection_attributes: object        
        	}     
        	write code here to construct the request body and any custom headers needed using the inputs object.     
        	*/     
        	// construct body using the inputs like input.prompt and so on.      
        	var body = {};      
        	//construct headers using the inputs      
        	var headers = {};      
        	return {     
        		body: body,     
        		headers: headers     
        	};     
        })(inputs);
        
        	 
        ```

5.  Select the **Active** option.

6.  Create a response transformer script.

    1.  In the **Response Transformer** filed, enable the **Turn on ECMAScript 2021 \(ES12\) mode** toggle to create script.

        The following example shows the response transformer script for the custom guardian response structure.

        ```
        (function(inputs) {     
        	/*     
        	write code here to transform the custom guardian response into standard guardian response format expected by platform     
        	inputs structure: {           
        		response_body: object,     
        		threshold_setting: object     
        	}     
        	*/     
        	// write code here to populate the response object.     
        	var guardianResponse = {};     
        	//Set flagged to true, if the guardian has flagged the text. Categories are optional and are for logging purpose only     
        	// if transformer setting is Prompt Injection, expected response format: {security:{flagged:false,categories:[]}}     
        	// if transformer setting is Offensiveness, expected response format: {safety:{flagged:false,categories:[]}}     
        	// if transformer setting is ALL, expected response format: {safety:{flagged:false,categories:[]},security:{flagged:false,categories:[]}}      
        	return guardianResponse;     
        })(inputs);
        
        	 
        ```

7.  In the **Guardian Setting** field, select a guardrail of your choice.

    -   Select **All** to handle the detection of both offensiveness and prompt injection together.
    -   Select **Offensiveness** to enable the detection of offensive or harmful content.
    -   Select **Prompt Injection** to enable the detection of prompt attacks.
    **Note:** If your LLM can evaluate both offensiveness and prompt injection in a single request, select All. If not, create separate guardrail records for each offensiveness and prompt injection.

8.  In the **Connection And Credential Alias** field, select the alias that you want to integrate with your custom guardian.

9.  Set up the custom guardian token limit.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Select the **Gen AI Control Setting Data \[sys\_gen\_ai\_control\_setting\_data\]** table.

    3.  In the Related Links section, select **Show List**.

    4.  Search for the **Custom Guardian Token limit** record in the **Gen AI Control Data** column.

    5.  Update the **Value** field of the Custom Guardian Token limit record with the maximum number of tokens per request.

        The token limit defines the maximum number of tokens the guardrail can process in a single evaluation. If the request content exceeds this limit, the content splits into smaller parts. Each part is evaluated separately against the guardrail rules.

        For example, if the token limit is 1000 and the request content is 2500 tokens, the system splits it into three parts and evaluates each one individually.


**Parent Topic:**[Configuring a Guardrail Service Provider](../concept/configuring-byog.md)

