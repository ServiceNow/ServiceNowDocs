---
title: Test a prompt
description: After you create a prompt for your custom skill, test it before you finalize it to verify that it returns the expected results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skill-kit/test-prompt-template.html
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 3
breadcrumb: [Using AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Test a prompt

After you create a prompt for your custom skill, test it before you finalize it to verify that it returns the expected results.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you created the prompt for.

3.  In the Test prompt section, select **Run tests**.

4.  Select a test record, such as an incident.

5.  Select **Run test**.

    **Important:**

    Testing a skill consumes at least one Now Assist assist for the base prompt call.

    If the skill has LLM-judged evaluation metrics attached on the **Deployment and skill settings** tab, each metric execution consumes additional assists. Metric execution is billed as a custom call at one assist per 1,000 output tokens. Script-based metrics \(metrics with a script instead of a judge prompt\) don't consume assists.

    For information about adding evaluation metrics, see [Configure deployment and skill settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/configure-skill-settings.md).

    |Tab|Description|
    |---|-----------|
    |Response|Result that the large language model \(LLM\) returns for the prompt.|
    |Grounded prompt|Prompt with the data from your skill inputs and tools filled in. Use this view to verify that your skill inputs and tools return the correct data.|

6.  If the skill is deployed as a flow, turn off the **com.glide.oneapi.fdih.async.quick.mode** system property, and then turn on flow reporting.

    This property controls whether flow execution details are generated when running flows, subflows, and actions from a custom skill. You can use flow execution details to test and troubleshoot your flow, subflow, or action. For more information about the system property, see [Workflow Studio flow system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/flow-designer-system-properties.md).

7.  Refine the prompt and repeat testing as needed.

8.  Select the run test history icon \[Omitted image "icon-nask-test-history.png"\] Alt text: to see the results from your previous run tests.


## What to do next

After you test your prompt, finalize the prompt and publish the skill. To learn more about publishing a skill, see [Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/publish-skill.md).

If you have not configured the deployment settings for your skill, see [Configure deployment and skill settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/configure-skill-settings.md).

**Parent Topic:**[Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill]()

[Create a prompt]()

[Use prompt assistance]()

[Evaluate a prompt]()

[Finalize and publish a skill]()

[Activate a skill]()

[Call a custom skill from a script]()

