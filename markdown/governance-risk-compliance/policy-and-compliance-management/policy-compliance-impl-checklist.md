---
title: Implement setup checklist for the GRC: Policy and Compliance Management application
description: This checklist includes the setup tasks that you are required to complete in your ServiceNow AI Platform instance. When you have completed these tasks, the base system is ready for operation. Optional setup procedures are also included to enhance GRC: Policy and Compliance Management functionality.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Implementing Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Implement setup checklist for the GRC: Policy and Compliance Management application

This checklist includes the setup tasks that you are required to complete in your ServiceNow AI Platform® instance. When you have completed these tasks, the base system is ready for operation. Optional setup procedures are also included to enhance GRC: Policy and Compliance Management functionality.

## Before you begin

Role required: sn\_compliance.admin, sn\_compliance.manager

Consider creating and printing a PDF of this checklist topic. You can then check off tasks as you complete them.

## Procedure

1.  To generate a PDF, click the **Save As PDF** icon \(![Save as PDF icon](../../grc-cam/image/save-as-pdf.png)\) at the top of the topic and click **Selected topic**.

<table id="table_lqq_1qt_rhb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator or Compliance Manager role, verify that you have the GRC core applications installed on a ServiceNow AI Platform instance.

 **Note:** The GRC core applications and the ServiceNow AI Platform instance should be from the same family release.

 1.  To verify the GRC: GRC Profile Dependencies core application is installed on your instance, navigate to **Plugins** and search for GRC Profile.
2.  If the GRC Profile core application is not already installed, click **Install** to install it.
3.  After the GRC Profile application is installed, install the Policy and Compliance Management core application.
 If Policy and Compliance Management is not visible in your instance, all of the GRC core applications are available from the ServiceNow Store. For more information about getting entitlement, downloading, and installing the GRC core applications, see [GRC and the ServiceNow Store](../../grc-common/concept/grc-and-store.md).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator role, in your ServiceNow AI Platform instance, verify that you have assigned users with the required ServiceNow AI Platform roles.

 For detailed instructions and a list of Policy and Compliance Management roles, see [Assign Policy and Compliance Management roles to your users](assign-user-roles.md).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator role, set Policy and Compliance Management properties to control various behaviors in the system. For example, you can define states for which a control is active or inactive.

 For detailed instructions, see [Set Policy and Compliance Management properties](set-policy-compliance-properties.md).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator or Compliance Manager role, create policies. A policy is a document that defines an internal practice that processes must follow. Policies are defined as policies, procedures, standards, plans, checklists, frameworks, and templates.

 For detailed instructions, see [Create a policy](../../grc-policy-and-compliance/task/t_DefineAPolicy.md).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator or Compliance Manager role, create control objectives. A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. They can be categorized, classified, and related to policies.

 For detailed instructions, see [Create a control objective](../../grc-policy-and-compliance/task/t_CreateAPolicyStatement.md).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator or Compliance Manager role, relate control objectives to policies. You can associate control objectives to a policy individually when the policy is in the Review or Draft state.

 For detailed instructions, see [Relate a control objective to a policy](../../grc-policy-and-compliance/task/t_RelatePolicyStateToPolicy.md).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator, Compliance Manager, or Attestation Creator role, create an attestation. The Attestation Designer allows you to create and edit metric types, as well as define different metric types for different controls.

 For detailed instructions, see [Create a control attestation using the Attestation Designer](../../grc-policy-and-compliance/concept/c_Attestations.md#).

</td></tr><tr><td>

![check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the Compliance Administrator or Compliance Manager role, create control indicators. Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.

 For detailed instructions, see [Create a control indicator](../../grc-policy-and-compliance/concept/manage-indicators-policy-comp.md#).

</td></tr></tbody>
</table>    Congratulations! You have successfully set up the GRC: Policy and Compliance Management base system. Depending on the needs of your organization, optional setup procedures are available. For example, if you integrate with Network Frontiers Unified Compliance Framework \(UCF\), procedures for managing the integration are here. Or if you want to set up the mobile experience for GRC: Policy and Compliance Management, those procedures are also here.

    For detailed instructions for optional features, see [Policy and Compliance Management enhancement steps](../concept/policy-compliance-optional-steps.md).


