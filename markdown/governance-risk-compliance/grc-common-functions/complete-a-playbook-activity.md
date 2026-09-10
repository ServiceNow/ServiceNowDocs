---
title: Complete a playbook activity
description: Complete playbook activities to progress an issue through the stages defined in its workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/complete-a-playbook-activity.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Complete a playbook activity

Complete playbook activities to progress an issue through the stages defined in its workflow.

## Before you begin

The issue's workflow must have a playbook associated with it. See [Add the layout, state model, and playbook to a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-the-layout-state-model-and-playbook-to-a-workflow.md).

Role required: none

## About this task

Activities become available in sequence within a stage. Activities that are not yet available display a message indicating that previous activities must be completed first. Each activity can have a different assignee, which is displayed on the activity card.

The activities, fields, and stages displayed for an issue depend on the playbook associated with the issue's workflow. The steps below follow the default issue workflow playbook's states as an example. Some activities can be optional and can be skipped.

## Procedure

1.  Open the issue and select the **Lifecycle** tab.

2.  Work through the activities in the New state.

    1.  Complete the fields for each activity.

        See [New state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/new-state-fields.md).

    2.  Select **Mark as complete** on the last activity, then confirm the state change.

        A confirmation message identifies the state transition that will occur.

3.  Work through the activities in the Analyze state.

    1.  Complete the fields for each activity.

        One activity, Group this issue, is optional and has a **Skip** option.

    2.  Select **Mark as complete** or **Skip** on the last activity, then confirm the state change.

        A confirmation message identifies the state transition that will occur.

4.  Work through the activities in the Respond state.

    1.  Complete the fields for each activity.

        See [Respond state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/respond-state-fields.md).

    2.  Select **Mark as complete** on the last activity, then confirm the state change.

        A confirmation message identifies the state transition that will occur.

5.  Work through the activities in the Review and close state.

    1.  Complete the fields for each activity.

        See [Review and close state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-close-state-fields.md).

    2.  Select **Mark as complete** on the last activity to close the issue.


## Result

As activities are completed and state changes are confirmed, the issue progresses through its workflow. The progress indicator is updated to reflect the current stage.

-   **[New state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/new-state-fields.md)**  
Fields used in the activities of the New state in an issue's lifecycle.
-   **[Analyze state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/analyze-state-fields.md)**  
Fields used in the activities of the Analyze state in an issue's lifecycle.
-   **[Respond state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/respond-state-fields.md)**  
Fields used in the activities of the Respond state in an issue's lifecycle.
-   **[Review and close state fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-close-state-fields.md)**  
Fields used in the activities of the Review and close state in an issue's lifecycle.
-   **[Remediation task fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/remediation-task-fields.md)**  
Fields on a remediation task record.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/common-grc-features.md)

