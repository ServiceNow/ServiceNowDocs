---
title: Set up advanced risk assessments for policy exception
description: Customize the risk assessment methodology by creating your values for each question in risk assessment and calculate your risk rating scores.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assess risks of policy exception using advanced risk assessments, Manage policy exceptions and extensions using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Set up advanced risk assessments for policy exception

Customize the risk assessment methodology by creating your values for each question in risk assessment and calculate your risk rating scores.

## Before you begin

Role required: sn\_compliance.admin

## About this task

If you want to make changes to the Risk Assessment Methodology that is provided by the base system or create a new methodology for policy exception, then the following procedure must be followed after creating or updating the risk assessment methodology for policy exception.

Map the Qualitative Rating Criteria of the risk assessment methodology with the risk rating of the policy exception in the Policy exception risk rating mapping \(sn\_compliance\_policy\_exception\_risk\_rating\_mapping\) table for the final risk rating score.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Policy exception risk rating mapping**.

2.  Enter the corresponding policy exception risk rating value for each risk assessment rating.

    **Note:** The qualitative rating criteria of a residual assessment from a published risk assessment methodology on policy exception table are available options in this field.

3.  Click **Save**.

    The score in the risk assessment is converted to the corresponding value in the policy exception risk rating column.

    **Note:** All qualitative rating criteria that are newly configured must have an equivalent mapping with the policy exception risk rating. If the mapping of the Risk assessment rating with the Policy exception risk rating in the Policy exception risk rating mapping table is incorrect, then the **Risk rating** field displays the result as **NONE** along with a message. In this case, you have an option to override the risk rating result of the **Take risk assessment** method and select a value in the **Risk rating** field by selecting the **Override** check box.

    If you are creating a different assessment methodology from the one that is provided by the base system, then you must add the sys\_ID of the new methodology in the value field of **sn\_risk\_advanced.rams\_with\_extension\_points** system property.


