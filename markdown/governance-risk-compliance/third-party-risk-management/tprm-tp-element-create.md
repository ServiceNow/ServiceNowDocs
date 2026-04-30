---
title: Create a third-party element record
description: Create a third-party element record after you collect the responses from a third party by using a collection template questionnaire in the Third-party Risk Management application. Third-party element records are assessed directly as part of the due diligence workflow.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-01-26"
reading_time_minutes: 3
breadcrumb: [Monitoring third-party elements, Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a third-party element record

Create a third-party element record after you collect the responses from a third party by using a collection template questionnaire in the Third-party Risk Management application. Third-party element records are assessed directly as part of the due diligence workflow.

## Before you begin

Make sure your due diligence request has completed the Inherent Risk Questionnaire \(IRQ\) process so that you can start the Third-party \(TP\) element collection process.

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor that is the due diligence request owner or sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

In the Vendor Management Workspace, the Third-party risk \(TPR\) manager or due diligence request owner selects **Start collection** for the due diligence request and a collection task is created. A collection task is an external assessment for collecting elements. After receiving and verifying responses to the collection template questionnaire, a Third-party risk \(TPR\) manager or due diligence request owner creates third-party element records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**.

2.  Select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Due diligence requests** &gt; **All requests**.

3.  Select the due diligence request that you want.

4.  On the **Collection task** tab of the due diligence request, select the External assessment \(VRA\) number to open the external assessment for collecting elements.

    For descriptions of all fields, see [Third-party element form](../../grc-workspace-vrm/reference/tprm-tpe-form.md).

    **Note:** The TP element classification determines which scoring model is applied. You can create additional classifications by navigating to **All** &gt; **Third-party Risk Management** &gt; **Third-party Elements** &gt; **Classifications**.

5.  On the **Questionnaire templates** tab, select **Add** to assign a third-party element questionnaire to the external assessment and then select the collection template questionnaire.

    You can send the third-party element questionnaire only to third parties.

    For more information on assessments, see [Assessing your third-party risk](../concept/tprm-assessing-tpr.md).

6.  After you receive responses from the third-party contact, navigate to the **Risk overview** tab of the assessment.

7.  In the Questionnaires and document requests section, select the collection template questionnaire and review the responses.

8.  After confirming that you received all the required information, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Third-party Elements** &gt; **All third-party elements**.

9.  Create a third-party element record by selecting **New** and filling in the form by using the information that was collected from each set of responses in the third-party element questionnaire.

    For descriptions of all these fields, see [Third-party element form](../../grc-workspace-vrm/reference/tprm-tpe-form.md).

    **Note:** The TP element classification determines which scoring model is applied to the third-party element. You can create new third-party element classifications by navigating to **All** &gt; **Third-party Risk Management** &gt; **Third-party Elements** &gt; **Classifications**.

10. Select **Submit**.

    A third-party element record is created and is available for review and assignment to engagements.


## What to do next

Close the external assessment for collecting elements and then manually add elements to the Engagement elements tab of an engagement. After all third-party elements are assigned to an engagement, you can start the due diligence process. For more information, see [Add a third-party element record to an engagement](tprm-tp-element-engagement.md) and [Monitoring third-party elements](../concept/tprm-monitor-tp-elements.md).

