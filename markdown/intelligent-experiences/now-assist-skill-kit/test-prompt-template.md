---
title: Test a prompt
description: After you create a prompt for your custom skill, test the prompt template before you finalize it. Testing the prompt verifies that you’re seeing the expected prompt results before it’s activated.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-09-16"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Test a prompt

After you create a prompt for your custom skill, test the prompt template before you finalize it. Testing the prompt verifies that you’re seeing the expected prompt results before it’s activated.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you created the prompt for.

3.  In the Test prompt section, select **Run tests**.

4.  Choose a test incident or record.

5.  Select **Run test**.

    **Note:** Testing your skill consumes an assist.

    |Tab|Description|
    |---|-----------|
    |Response|The response is the result that the large language model \(LLM\) sends back from the prompt.|
    |Grounded prompt|The grounded prompt enables you to see the data that was brought into the prompt from your skill inputs and tools. With this view, you can see if your skill inputs and tools are returning the correct data.|

6.  If the skill is deployed as a flow, disable the system property com.glide.oneapi.fdih.async.quick.mode, and then enable flow reporting.

    This property allows the generation of flow execution details when running flows, subflows, and actions from a custom skill. You can use flow execution details to test and troubleshoot your flow, subflow, or action. For more information about the system property, see [Workflow Studio flow system properties](https://www.servicenow.com/docs/access?context=flow-designer-system-properties&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

7.  Refine the prompt if you want, and repeat testing as necessary.

8.  Select the run test history icon ![Run test history icon.](../image/icon-nask-test-history.png) to see the results from your previous run tests.


## What to do next

After you test your prompt, you must finalize and publish it. To learn more about publishing a skill, see [Finalize and publish a skill](publish-skill.md).

If you have not configured the deployment settings for your skill, see [Configure skill deployment settings](configure-skill-settings.md).

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)

