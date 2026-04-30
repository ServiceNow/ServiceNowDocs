---
title: Request a policy exception through Service Portal
description: Your employees and business users within your company can request a policy exception through the ServiceNow Service Portal.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage policy exceptions and extensions, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Request a policy exception through Service Portal

Your employees and business users within your company can request a policy exception through the ServiceNow® Service Portal.

## Before you begin

Role required: sn\_compliance.user, sn\_grc.business\_user, sn\_grc.business\_user\_lite, sn\_grc\_emp\_user.grc\_employee

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

2.  In the screen header, navigate to **GRC** &gt; **My Policy Exceptions** to view all policy exceptions that you requested.

3.  Click **New Policy Exception**.

4.  On the form, fill in the fields.

    Complete the [Policy Exception form](create-policy-exception-employee-center.md). Specify what the policy exception is for and select appropriate policy, control objective, or issue. This question is for you to identify the appropriate source type.

    When you select a control objective, the **Impacted controls** tab appears, where you can select controls associated to the control objective. You can also search and select an entity.

    Select **Control** to associate multiple controls from different control objectives. This option supports your policy exception for multiple controls objectives, instead of creating multiple policy exceptions that could be applied on multiple controls.

    If you are creating a policy exception from **GRC** &gt; **My Policy Acknowledgements**, then **What is the exception for?** field auto-populates the value as Policy. The name of the policy also appears in the **Policy** field.

    In **Issue** field, you can search by the description and select the appropriate issue.

5.  Click **Submit**.

    If you raise a policy exception from Service Portal and if verification rules are not configured, then the policy exception moves to the Analyze state. However, if verification rules are configured for the policy exception, then the policy exception moves to the New state and the verification approval process is triggered. As verification rules are configured the approver is required to verify the policy exception and approve it, only then the policy exception moves to Analyze state.


**Parent Topic:**[Manage policy exceptions and extensions](../concept/manage-policy-exceptions.md)

