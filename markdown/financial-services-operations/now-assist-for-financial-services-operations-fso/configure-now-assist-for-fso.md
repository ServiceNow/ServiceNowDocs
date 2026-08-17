---
title: Configure case summarization in ServiceNow Otto for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure the ServiceNow Otto for Financial Services Operations \(FSO\) application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-now-assist-for-fso.html
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [Configure, ServiceNow Otto for FSO, Financial Services Operations \(FSO\)]
---

# Configure case summarization in ServiceNow Otto for Financial Services Operations \(FSO\)

If you have the admin role, you can configure the ServiceNow Otto for Financial Services Operations \(FSO\) application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.

## Before you begin

Role required: admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for FSO. This console contains what you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the case summarization skills that you can access from the AI Admin Hub console.

|Area|Skills|
|----|------|
|Banking|Dispute case summarization|
|Insurance|Claim case summarization|

**Note:**

Now LLM Service is currently the only provider for this application's skills.

## Procedure

1.  Install the ServiceNow Otto for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/supporting-information-for-now-assist-for-financial-services-operations-fso.md).
    -   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **Admin** &gt; **** &gt; **AI Skills**.

3.  Select the **Customer** &gt; **FSO** workflow group.

4.  On the tile for your skill, select **Activate skill**.

5.  Review the inputs for the selected skill.

    The input table fields are read-only.

    For information about the inputs for each skill, see [Skill inputs for ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/skill-inputs-and-triggers-for-now-assist-for-financial-services-operations-fso.md).

6.  After you review the inputs for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

7.  Select where you would like to display the skill.

    -   **In-product**: When selected, the ServiceNow Otto skills are displayed on forms and workspaces.

        For the skills that appear in-product, select the down arrow to define the roles that can use the skill.

    -   **ServiceNow Otto panel**: When selected, the skills are available in the ServiceNow Otto panel. If you don't see this option, you must activate the panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

        For the skills that appear in the panel, select the down arrow to define the roles that can use the skill.

8.  After you configure the display for the selected skill, select **Save and continue** to go to the next step.

9.  Review your choices and select **Activate** to complete the configuration.


## Result

A message appears confirming the summarization skill has been successfully activated. Select **Return to Banking** to return to the Banking skills screen.

## What to do next

You can choose which service provider to use for this skill in ServiceNow Otto Admin. For more information, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md).

