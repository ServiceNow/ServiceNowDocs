---
title: Configure case summarization in ServiceNow Otto for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure the ServiceNow Otto for Financial Services Operations \(FSO\) application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/configure-now-assist-for-fso.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configuring generative AI for financial services operations, configuring generative AI for FSO]
breadcrumb: [Configure AI skills, Enable AI capabilities, Configure, Financial Services Operations \(FSO\)]
---

# Configure case summarization in ServiceNow Otto for Financial Services Operations \(FSO\)

If you have the admin role, you can configure the ServiceNow Otto for Financial Services Operations \(FSO\) application so that your agents can use case summarization skills in Financial Services Workspace and Core UI.

## Before you begin

Verify the ServiceNow Otto for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\) is installed.

-   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   For general information about configuring AI skills in FSO, see [Configure Financial Services Operations AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-now-assist-skills.md).

Role required: admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for FSO. This console contains what you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the FSO case summarization skills that you can access from the AI Admin Hub console.

|Area|Skills|
|----|------|
|Banking|Dispute case summarization|
|Insurance|Claim case summarization|

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  On the tile for your skill, select **Activate skill**.

4.  Review the inputs for the selected skill.

    The input table fields are read-only.

    For information about the inputs for each skill, see [Skill inputs for ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/skill-inputs-and-triggers-for-now-assist-for-financial-services-operations-fso.md).

5.  After you review the inputs for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

6.  Select where you would like to display the skill.

    -   **In-product**: When selected, the AI skills are displayed on forms and workspaces. For the skills that appear in-product, select the down arrow to define the roles that can use the skill.
    -   **ServiceNow Otto panel**: When selected, the ServiceNow Otto for FSO skills are available in the ServiceNow Otto panel. If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

        For the skills that appear in the ServiceNow Otto panel, select the down arrow to define the roles that can use the skill.

7.  After you configure the display for the selected skill, select **Save and continue** to go to the next step.

8.  Review your choices and select **Activate** to complete the configuration.


## Result

A message appears confirming the summarization skill has been successfully activated. Select **Return to Banking** to return to the Banking skills screen.

## What to do next

You can choose which service provider to use for this skill in ServiceNow Otto Admin. For more information, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

