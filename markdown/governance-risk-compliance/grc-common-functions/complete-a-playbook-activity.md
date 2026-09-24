---
title: Complete a playbook activity
description: Complete playbook activities to progress an issue through the stages defined in its workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/complete-a-playbook-activity.html
release: brazil
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Complete a playbook activity

Complete playbook activities to progress an issue through the stages defined in its workflow.

## Before you begin

The issue's workflow must have a playbook associated with it. See [Add the layout, state model, and playbook to a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.md).

Role required: none

## About this task

Activities become available in sequence within a stage. Activities that are not yet available display a message indicating that previous activities must be completed first. Each activity can have a different assignee, which is displayed on the activity card.

The activities, fields, and stages displayed for an issue depend on the playbook associated with the issue's workflow. Some activities can be optional and can be skipped.

## Procedure

1.  Open the issue and select the **Lifecycle** tab.

2.  Complete the fields for the current activity.

3.  Select **Mark as complete**.

    If the activity is optional, you can select **Skip** instead.

4.  When prompted, confirm the state change.

    The confirmation message identifies the state transition that will occur. Continue to the next state by selecting the confirmation button. If you aren't ready to continue, select **Cancel**.

5.  Repeat [2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/complete-a-playbook-activity.md) through [4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/complete-a-playbook-activity.md) until all required activities are completed.


## Result

As activities are completed and state changes are confirmed, the issue progresses through its workflow. The progress indicator is updated to reflect the current stage.

-   **[New state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/new-state-fields.md)**  
Fields used in the activities of the New state in an issue's lifecycle.
-   **[Analyze state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/analyze-state-fields.md)**  
Fields used in the activities of the Analyze state in an issue's lifecycle.
-   **[Respond state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/respond-state-fields.md)**  
Fields used in the activities of the Respond state in an issue's lifecycle.
-   **[Review and close state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/review-and-close-state-fields.md)**  
Fields used in the activities of the Review and close state in an issue's lifecycle.
-   **[Remediation task fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/remediation-task-fields.md)**  
Fields on the remediation task form.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-common-functions/common-grc-features.md)

