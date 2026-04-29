---
title: Set up the approval rules for due diligence requests
description: Set up the rules at each approval level for your due diligence requests by selecting an approver type and the number of approvals that you require in the Third-party Risk Management application. You can also filter the table conditions that apply to each rule so that you can help ensure that the correct user or group is assigned as an approver.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Approve or reject due diligence requests, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Set up the approval rules for due diligence requests

Set up the rules at each approval level for your due diligence requests by selecting an approver type and the number of approvals that you require in the Third-party Risk Management application. You can also filter the table conditions that apply to each rule so that you can help ensure that the correct user or group is assigned as an approver.

## Before you begin

Set up the approval levels. For more information, see [Set up the approval levels for due diligence requests](tprm-set-request-approval-levels.md).

Role required: admin or sn\_vdr\_risk\_asmt.vendor\_risk\_admin

## About this task

For each rule, you can select the individual approvers, approvers from the Third-party due diligence request \[sn\_tprm\_dd\_request\] table, or dynamic approvers. Dynamic approvers refer to individuals or groups who are assigned as approvers based on the Approver table that is defined in the approval rule form. The approvers can be a Third-party risk \(TPR\) manager or TPR administrator.

Each approval level can contain multiple approval rules. Each approval rule can be created on the table of the approving record or any other related table of the approving table.

## Procedure

1.  Navigate to **All** &gt; **Approval Configurator** &gt; **Approval Configurations**.

2.  Select an approval configuration record.

3.  In the Name column of the Approval Levels section, select the approval level record that you want.

4.  In the Approval Rules section, select **New**.

5.  On the approval rule form, specify the name of the rule.

6.  Enter a brief description of the approval rule.

7.  Select the source for the request.

    For descriptions of all these fields, see [Approval rule form](../reference/tprm-ar-form.md).

8.  Select **Submit**.


**Related topics**  


[Set up the approval levels for due diligence requests](tprm-set-request-approval-levels.md)

