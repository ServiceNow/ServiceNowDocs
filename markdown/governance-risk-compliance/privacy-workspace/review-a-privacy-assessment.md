---
title: Review a privacy assessment
description: As a privacy analyst, review a privacy assessment after the business user submits it. You can either close the assessment after a review or request a revision if you determine that the assessment requires more information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/review-a-privacy-assessment.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Review a privacy assessment

As a privacy analyst, review a privacy assessment after the business user submits it. You can either close the assessment after a review or request a revision if you determine that the assessment requires more information.

## Before you begin

Role required: sn\_privacy.analyst

## About this task

As a reviewer, you can preview the assessment with the applicable risk statements, information objects, and control objectives.

After a business user submits a privacy assessment, it moves to the Review state. As the assigned analyst, you can perform the following actions on it:

-   Review the relationships added to a hierarchy by the business user.
-   Review the data transfer records generated from hierarchy relationships and remove those that aren't applicable.
-   Request a revision of the assessment.
-   Mark the assessment as complete.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the Tasks icon \[Omitted image "icon-tprm-ws-tasks.png"\] Alt text:.

3.  In the My pending tasks tab, select **Privacy assessments**.

4.  Open the assessment to be reviewed.

5.  To review the hierarchy relationships defined by the business user, navigate to the **Hierarchy** tab.

    This displays the relationships between the primary node and each of its related nodes.

    To see the locations and data elements scoped to each data subject type involved in a particular transfer, select **Cell actions** &gt; **View details** in the Data subjects involved column.

6.  To review the data transfers generated from the hierarchy relationships, navigate to the **Data transfers** tab.

    This lists the data transfer records created for each movement of personal data. For more information, refer to [Manage data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/data-transfers.md).

    If one or more data transfers aren't applicable to the processing activity, select the record\(s\), and select **Remove**.

7.  To view the records added through smart assessment automation rules, navigate to the **Applicable scope** tab.

    To generate AI-recommendations of control objectives and risk statements based on assessment responses, see [AI reviewer assist for privacy assessment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/ai-reccos-for-pia.md).

8.  To request more information from the responder, select **Request for revision**.

9.  Mark the assessment as complete.

    1.  Select **Update state**.

    2.  In the **State** field, select **Closed complete**.

    3.  In the **Additional comments** field, provide any additional information.

    4.  Select **Submit**.


## Result

-   The corresponding controls and risks for the records in Applicable scope are automatically scoped to the processing activity.
-   The hierarchy relationships are mapped to the processing activity. You can manage these relationships or add new ones directly from the processing activity record by navigating to **Processing data inventory** &gt; **Hierarchy**. For steps to add a new relationship, see [Add relationships to a hierarchy for a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/create-a-data-lineage-for-a-processing-activity.md).
-   The data transfers are mapped to the processing activity. You can add or remove data transfers directly from the processing activity record by navigating to **Regulatory details** &gt; **Data transfers**. For steps, see [Create a data transfer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/create-a-data-transfer.md) and [Delete a data transfer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/delete-a-data-transfer.md).

## What to do next

A data transfer record generated from a hierarchy relationship does not have a transfer mechanism assigned by default. Add transfer mechanisms to such records. For steps, see [Add a transfer mechanism to a data transfer record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/add-transfer-mechanism-dt.md).

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

