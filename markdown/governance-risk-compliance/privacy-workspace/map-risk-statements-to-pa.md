---
title: Map a risk statement to a question response
description: Map the risk statements to the responses of the assessment questions to automatically create and apply the respective risks on the processing activity.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a privacy assessment, Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Map a risk statement to a question response

Map the risk statements to the responses of the assessment questions to automatically create and apply the respective risks on the processing activity.

## Before you begin

Role required: sn\_privacy.admin and sn\_privacy.manager

## About this task

When a user responds to a question, based on the answers, the corresponding risk statement is mapped to the processing activity.

You can relate risk statements to an assessment question only if the questions are of the following types:

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

3.  Open the question for which you want to add risk statement

<table id="choicetable_rlk_wqh_sqb"><thead><tr><th align="left" id="d194031e110">

Type of questions

</th><th align="left" id="d194031e113">

Steps to map risk statements

</th></tr></thead><tbody><tr><td id="d194031e119">

**Boolean, Template**

</td><td>

To create and apply risk statements for a response, perform the following steps.1.  Select the response in the **User response to create controls** field.
2.  From the Risk Statements related list, click **Edit**.
3.  Double-click the required risk statements in the Collection list.

**Note:** Double-clicking automatically moves the objects to the Risk statements list.

4.  Click **Save**.


</td></tr><tr><td id="d194031e154">

**Choice, Image scale, Numeric, Ranking**

</td><td>

To create and apply risk statements for a response, perform the following steps.1.  In the Metric Categories related list, click the required metric.
2.  In the Assessment Metrics related list, click the required question.
3.  In the Assessment Metric Definitions related list, select a value for which you want to map risk statements.
4.  From the risk statements related list, click **Edit**.
5.  Double-click the required risk statements in the Collection list.

**Note:** Double-clicking automatically moves the objects to the Risk statements list list.

6.  Click **Save**.


</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Create a privacy assessment](create-assessment-template.md)

