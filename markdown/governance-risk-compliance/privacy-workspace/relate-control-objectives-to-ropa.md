---
title: Map a control objective to a question response
description: Map the control objectives to the responses of the assessment questions to automatically create and apply the respective controls on the processing activity.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a privacy assessment, Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Map a control objective to a question response

Map the control objectives to the responses of the assessment questions to automatically create and apply the respective controls on the processing activity.

## Before you begin

You can apply active and inactive controls to an assessment response. However, when an assessment is submitted by the business user, only the mapped control objectives that are in the **Active** state are considered to create and apply the controls on the processing activity.

Role required: sn\_privacy.admin and sn\_privacy.manager

## About this task

You can relate control objectives to an assessment question only if the questions are of the following types:

-   Choice
-   Image scale
-   Numeric scale
-   Ranking
-   Boolean
-   Template

**Note:** For Boolean questions, the question can either use yes or no answers or use check boxes that must be selected or cleared.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Assessment Templates**.

2.  Click and open the required assessment template.

<table id="choicetable_rlk_wqh_sqb"><thead><tr><th align="left" id="d66956e113">

Type of questions

</th><th align="left" id="d66956e116">

Steps to map controls

</th></tr></thead><tbody><tr><td id="d66956e122">

**Boolean, Template**

</td><td>

To create and apply controls for a response, perform the following steps.1.  Select the response in the **User response to create controls** field.
2.  From the Control Objectives related list, click **Edit**.
3.  Double-click the required control objectives in the Collection list.

**Note:** Double-clicking automatically moves the objects to the Control objectives List list.

4.  Click **Save**.


</td></tr><tr><td id="d66956e157">

**Choice, Image scale, Numeric, Ranking**

</td><td>

To create and apply controls for a response, perform the following steps.1.  In the Metric Categories related list, click the required metric.
2.  In the Assessment Metrics related list, click the required question.
3.  In the Assessment Metric Definitions related list, select a value for which you want to map control objectives.
4.  From the Control Objectives related list, click **Edit**.
5.  Double-click the required control objectives in the Collection list.

**Note:** Double-clicking automatically moves the objects to the Control objectives List list.

6.  Click **Save**.


</td></tr></tbody>
</table>3.  Click **Update**.


## Result

The control objectives are related to the processing activity.

**Parent Topic:**[Create a privacy assessment](create-assessment-template.md)

