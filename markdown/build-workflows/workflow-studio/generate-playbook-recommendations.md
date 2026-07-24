---
title: Generate recommendations for placeholder activities
description: Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/generate-playbook-recommendations.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Playbook recommendations for placeholder activity, Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Generate recommendations for placeholder activities

Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.

## Before you begin

-   Verify that the Now Assist for Creator plugin is installed and the **Playbook recommendations** skill is active.

    **Note:** Skills are available in **Admin** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Creator**. If you don't see **Creator** under **Now Assist Skills**, the plugin is not installed.

    \[Omitted image "now-assist-creator-skills.png"\] Alt text: Now assist for creator skills page.

    For information about installing Now Assist for Creator, see 

-   You can only generate recommendations for placeholder activities in a generated playbook outline. To learn how to generate a playbook outline, see [Generate a playbook from text or image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md).
-   Role required:
    -   admin, playbook.admin, pd\_author, or a delegated developer permission

## Procedure

1.  Open you playbook and hover over the placeholder activity and select the recommendations icon \(\[Omitted image "recommendations-icon.png"\] Alt text: Now Recommendations icon\) in the mini-picker.

2.  Select one of the recommended activity definitions, if appropriate.

    **Note:** If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

3.  Try updating the **Label** and **Description** to improve results.

    1.  Open the placeholder activity.

    2.  Update the **Label** and **Description**.

    3.  Under the **Activity definition** field, select the recommendations button \(\[Omitted image "now-recommendations-button.png"\] Alt text: Recommendations button\) to try to generate recommendations again.

    4.  Select one of the recommended activity definitions, if appropriate.

4.  Continue on with activity configuration from Step [8.e](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md) of the [Generate a playbook from text or image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/generate-a-playbook-outline.md) procedure.


## Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Create a sample playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/design-automated-process.md).

## What to do next

Design the Playbook Experience for your agents and fulfillers in UI Builder. To learn how to design and customize the runtime playbook experience in UI Builder, see [Customizing the Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-customize-playbook.md).

**Parent Topic:**[Playbook recommendations for placeholder activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-recommendations.md)

**Related topics**  


[Playbook recommendations for placeholder activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-recommendations.md)

