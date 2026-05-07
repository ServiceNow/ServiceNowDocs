---
title: Assess risks of policy exception using advanced risk assessments
description: Take the advanced risk assessment to evaluate the risk involved with the policy exception.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage policy exceptions and extensions using the Compliance Workspace, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Assess risks of policy exception using advanced risk assessments

Take the advanced risk assessment to evaluate the risk involved with the policy exception.

## Before you begin

Role required: sn\_compliance.manager

GRC: Advanced Risk is the required plugin for the integration with Advanced risk assessment to assess risk using the advanced risk assessment feature.

## About this task

After the policy exception is submitted, as a compliance manager you can do the risk analysis on the policy exception to evaluate its risk status and determine its approval based on its risk impact on the policy.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, click the ![List icon](../../grc-cam-workspace/image/ws-list-icon.png) icon.

3.  Click **All policy exceptions** in the Policy exceptions list.

4.  Click the link to the policy exception record, for which you want to assess the risk, in the **Name** column.

5.  Select the **Take risk assessment** option in the **Method** field of the Risk assessment section.

    For more information on the risk assessment options, see [Risk assessment](request-policy-exception-ws.md#take-risk-assess) section.

6.  Click **Save**.

7.  Click the **Assess risk** button.

    You can assess the risk of a policy exception only when its state is Analyze.

8.  Select a risk assessor and an approver in the Specify risk assessor and approver pop-up.

    Any user with compliance user role or risk user role can be a risk assessor or an approver.

9.  Click the **Send assessment** button.

    Assessment is sent to the user selected in the pop-up. For more information, see [Assess risks and objects on an assessment instance](../../grc-risk/task/assessing-risks.md).

    After the assessment is complete, the **Risk rating** field on the policy exception form is auto-populated with the values configured in Policy exception risk rating mapping table.

10. Click the **Details** tab.

    The score calculated based on the risk assessment responses that you provided is mapped with the value in the **Risk rating** field.


