---
title: Tracking a managed activity
description: View managed activities in the usage analytics activities table for tracking and verification purposes in the Third-party Risk Management application.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Tracking a managed activity

View managed activities in the usage analytics activities table for tracking and verification purposes in the Third-party Risk Management application.

## Overview of managed activities

You can track and verify managed activities in the Usage analytics activities \[sn\_vdr\_risk\_asmt\_ua\_activity\] table.

An engagement only consumes one license, regardless of whether there’s one managed activity or many managed activities per contract year. Managed activity usage is triggered only when an activity is initiated.

Activities that are associated with a new third party going through the due diligence onboarding workflow aren’t counted as managed activities. In this context, a new third party is defined as a company that is not in the Company \[core\_company\] table.

If any of the following activities aren’t related to a new third party going through the due diligence onboarding workflow, they’re counted as managed activities:

-   An Inherent risk questionnaire \(IRQ\) that is sent by the system has a status of **Awaiting response**. For more information, see [Assessing your third-party risk](tprm-assessing-tpr.md).
-   A tiering assessment with a questionnaire that is sent by the system has a status of **Awaiting response**.
-   A third-party risk assessment with a questionnaire that is sent by the system has a status of **Submitted to third party**. For more information, see [Life cycle states of a external assessment](tprm-external-assessment-lifecycle.md).
-   The creation of a task or issue for a third-party risk assessment. For more information, see [Create a task for a third party or engagement](../task/tprm-ws-task-create.md) and [Create an issue for a third party or engagement](../task/tprm-ws-issue-create.md).

If a third-party risk assessment or due diligence request is automatically created by an event-driven management rule and later recalled, it isn’t counted as a managed activity. An assessment that is related to an event-driven management rule can be recalled up until the time that it’s submitted to the third party. For more information, see [Event-driven management — automate assessment processes](../../grc-workspace-vrm/task/tprm-event-drvn-mgt-rule-create.md).

**Note:** If an assessment isn’t related to an event-driven management rule, you can't recall it and it’s counted as a managed activity. If an assessment is canceled, it’s still considered as a managed activity.

## Using the usage analytics activities table for verification

The usage analytics activities table stores a record every time a managed activity occurs. This table is read only. Records that are two years or older are automatically archived. You must have the Third-party assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] role to view this table.

You can access the Usage analytics activities table by navigating to **All** &gt; **Third Party Risk Management** &gt; **Administration** &gt; **Managed Activity Analytics**.

The following example and table show the Usage analytics activities \[sn\_vdr\_risk\_asmt\_ua\_activity\] table.

![Usage analytics activities table with sample data.](../image/usage-analytics-activities.png "Usage analytics activities table")

<table id="table_tpddr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time that the activity occurred.

</td></tr><tr><td>

Activity

</td><td>

Record that is related to the activity.

</td></tr><tr><td>

Activity type

</td><td>

Managed activities that can be associated with tiering assessments, internal assessments, third-party risk assessments \(TPRA\), issues, and tasks.

</td></tr><tr><td>

Applies to

</td><td>

-   **Third party**: The activity applies to the parent third-party organization.
-   **Engagement**: The activity applies to the engagement.

</td></tr><tr><td>

Third party

</td><td>

Third party that is related to the activity.

</td></tr><tr><td>

Engagement

</td><td>

Engagement that is related to the activity.

</td></tr><tr><td>

Status

</td><td>

State of the activity:-   **Tracked**: The activity is logged.
-   **Recalled**: The activity was recalled by a user after it occurred.

</td></tr></tbody>
</table>**Note:** The calculated risk scores that are updated by assessments are managed activities. However, they aren’t logged in the Usage analytics activities \[sn\_vdr\_risk\_asmt\_ua\_activity\] table. The score updates from the risk intelligence score providers aren’t managed activities. For more information on the risk intelligence scores, see [Viewing risk intelligence scores](../../grc-workspace-vrm/reference/tprm-ws-tab-risk-intel-scores.md).

