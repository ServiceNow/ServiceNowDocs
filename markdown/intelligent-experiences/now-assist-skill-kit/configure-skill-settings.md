---
title: Configure deployment and skill settings
description: Configure where a skill appears in AI Admin Hub, review general information, set security controls, choose a provider, and add evaluation metrics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/configure-skill-settings.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-08-06"
reading_time_minutes: 4
breadcrumb: [Configuring AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Configure deployment and skill settings

Configure where a skill appears in AI Admin Hub, review general information, set security controls, choose a provider, and add evaluation metrics.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

The **Deployment and skill settings** tab contains five sections that you can configure in any order:

-   **Deployment settings**: Choose where the admin can find and activate the skill in AI Admin Hub.
-   **General information**: Review or edit the skill name and description.
-   **Security controls**: Restrict which roles can run the skill.
-   **Providers**: View the language model providers available for the skill.
-   **Evaluation metrics**: Add metrics that measure the quality of skill responses.

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you want to configure.

3.  Select the **Deployment and skill settings** tab.

4.  Configure the **Deployment settings** section.

    \[Omitted image "nask-deploy-settings.png"\] Alt text: Deployment Settings page for AI Skill Kit.

    Under **Now Assist features**, fill in the fields.

<table id="table_qfd_3nh_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workflow

</td><td>

The high-level category that this skill pertains to, such as **Technology**, **Employee**, **Creator**, or **Platform**. You can also select **Other** if none of the categories fit.

 The workflow that you choose is where the skill appears in the AI Admin Hub console.

</td></tr><tr><td>

Product

</td><td>

The specific product that this skill operates within, such as ITSM, ITOM, HR Service Delivery, AI Admin Hub.

</td></tr><tr><td>

Feature

</td><td>

The feature that the skill is used on, such as Agent Chat, Knowledge, Virtual Agent. You can also define a custom feature if necessary.

</td></tr><tr><td>

Name

</td><td>

The name of the feature.

</td></tr><tr><td>

Description

</td><td>

A description of the feature.

</td></tr></tbody>
</table>    Under **Select where you'd like to let the admin activate the skill**, select one or more activation points.

    -   **Now Assist panel**
    -   **UI Action**
    -   **Flow action**
    -   **Now Assist context menu**
    -   **Virtual assistants**

        For more information about Now Assist in Virtual Agent, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

    -   **UI Builder**
5.  Review the **General information** section.

    This section shows the information that you added when you created the skill. You can edit the skill name and description here.

6.  Configure the **Security controls** section to restrict which roles can run the skill.

    For the procedure, see [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md).

7.  Review the **Providers** section.

    The **Providers** section lists the language model providers available for the skill. Each provider is tagged as **Default** or **Not supported** where applicable.

    **Important:** The runtime model depends on the configuration in AI Admin Hub and may differ from what's shown in the **Providers** section.

8.  Add one or more **Evaluation metrics** to measure the quality of skill responses.

    Evaluation metrics attached in this section apply to every prompt test that you run on the skill.

    **Important:**

    LLM-judged evaluation metrics consume additional Now Assist assists during prompt testing. Metric execution is billed as a custom call at one assist per 1,000 output tokens, so metrics that produce longer output consume more assists.

    Script-based metrics \(metrics with a script instead of a judge prompt\) don't consume assists.

    For details about Now Assist consumption during prompt testing, see [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md).

    1.  In the **Evaluation metrics** section, select the add icon \[Omitted image "icon-nask-add.png"\] Alt text: add icon.

    2.  From the list of available metrics, select the metric that you want to add.

        Metrics are grouped by category. Each metric shows the language model provider that runs the metric, such as **Amazon Bedrock**, **Now LLM Generic**, or **Multiple LLMs**. Metrics that run as scripts don't display a provider tag.

        For descriptions of the available metrics, see [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md).

    3.  Review the metric details.

        |Tab|Description|
        |---|-----------|
        |**About**|A description of the metric, how it works, when to use it, and its output format.|
        |**Judge Prompt / Script**|The prompt that a language model uses to judge the response, or the script that evaluates the response, depending on how the metric is implemented.|

    4.  Select **Add**.

9.  Select **Save**.


## What to do next

After you configure the deployment and skill settings, you can publish your skill. To learn more about publishing skills, see [Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/publish-skill.md).

**Parent Topic:**[Configuring AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure a skill prompt]()

[Configure security controls for a skill]()

