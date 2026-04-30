---
title: Use a script with Generative AI Controller
description: Use background scripts and Generative AI Controller Generic Prompt to interact directly with the generative AI model API.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Use a script with Generative AI Controller

Use background scripts and Generative AI Controller Generic Prompt to interact directly with the generative AI model API.

## Before you begin

You must be on Vancouver patch 2 or above to script with `sn_one_extend.OneExtendUtil` objects.

Role required: admin

## About this task

With scripting, you have greater flexibility in how you use Generative AI Controller capabilities across the platform. By accessing the capability programmatically, you can capture the LLM's response and use that to determine next actions.

For more information on tracking Generative AI Controller usage, see [Monitoring Now Assist usage](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Create the text content for a Generic Prompt by creating a `request` array with a singular `executionRequests` object.

3.  Inside the `executionRequests`, add the `payload` and `capabilityID` attributes.

    The `capabilityID` is the sys\_id of the capability on the OneExtend Capabilities \(sys\_one\_extend\_capability\) table, such as Generic Prompt.

4.  Add the required inputs as attributes in the `payload` object.

<table><thead><tr><th>

Capability

</th><th>

Required attributes

</th></tr></thead><tbody><tr><td>

Generic Prompt

</td><td>

prompt: Prompt for the generative AI to respond to.

</td></tr><tr><td>

Generate Content

</td><td>

topic: Subject for content generation.

</td></tr><tr><td>

Sentiment Analysis

</td><td>

utterance: Text to analyze for user sentiment.

</td></tr><tr><td>

Summarize

</td><td>

textToSummarize: Topic for the AI to generate a summary.

</td></tr></tbody>
</table>    The following is an example `request` array for the Generic Prompt capability.

    ```
    var request = {
       "executionRequests": [
        {
           "payload": {
              "prompt": "Can you act like my business partner and give me some advice on a pitch?"
            },
            "capabilityId": "0c90ca79533121106b38ddeeff7b12d7"
         }
      ]
    };
    ```

5.  Call the `execute` method on sn\_one\_extend.OneExtendUtil.

6.  To display the response after running the background script, print the response in readable JSON by using the following code:

    ```
    gs.info(JSON.stringify(sn_one_extend.OneExtendUtil.execute(request)));
    ```


