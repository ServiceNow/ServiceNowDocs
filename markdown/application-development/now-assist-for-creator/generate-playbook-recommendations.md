---
title: Generate playbook recommendations
description: Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook recommendations, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Generate playbook recommendations

Select the activity definition for a placeholder activity from a list of AI-generated recommendations. The system generates recommendations based on an activity’s name and description.

## Before you begin

-   Make sure the playbook recommendations skill is turned on. To learn how to turn on the recommendations skill for playbooks, see [Turn on Playbook recommendations](turn-on-playbook-recommendations.md).
-   You can only generate recommendations for placeholder activities in a generated playbook outline. To learn how to generate a playbook outline, see [Generate a playbook](generate-a-playbook-outline.md).
-   Role required:
    -   admin, playbook.admin, pd\_author, or a delegated developer permission

## Procedure

1.  In your playbook outline, hover over the placeholder activity and select the recommendations icon \(![Now Recommendations icon](../images/recommendations-icon.png)\) in the mini-picker.

2.  Select one of the recommended activity definitions, if appropriate.

    **Note:** If there are no recommendations listed, then no activity definitions are considered relevant to the activity name and description.

3.  Try updating the **Label** and **Description** to improve results.

    1.  Open the placeholder activity.

    2.  Update the **Label** and **Description**.

    3.  Under the **Activity definition** field, select the recommendations button \(![Recommendations button](../images/now-recommendations-button.png)\) to try to generate recommendations again.

    4.  Select one of the recommended activity definitions, if appropriate.

4.  Continue on with activity configuration from Step [11.e](generate-a-playbook-outline.md#configure-activity-inputs) of the [Generate a playbook](generate-a-playbook-outline.md) procedure.


## Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Create a sample playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/design-automated-process.md).

## What to do next

Design the Playbook Experience for your agents and fulfillers in UI Builder. To learn how to design and customize the runtime playbook experience in UI Builder, see [Customizing the Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-customize-playbook.md).

**Parent Topic:**[Playbook recommendations](../concept/playbook-recommendations-landing.md)

