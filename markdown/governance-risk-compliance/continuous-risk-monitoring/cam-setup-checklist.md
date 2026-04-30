---
title: Checklist for Continuous Authorization and Monitoring setup
description: The checklist includes the tasks that you must complete to prepare the base system.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Checklist for Continuous Authorization and Monitoring setup

The checklist includes the tasks that you must complete to prepare the base system.

## Before you begin

Role required: admin, sn\_irm\_cont\_auth.admin

## Procedure

1.  Create and print a PDF of the checklist topic and check off tasks as you complete them.

    To generate a PDF, select the **Save As PDF** icon \(![Save as PDF icon](../image/pdf-icon-new.png)\) at the top of this topic and select **Selected topic**.

<table id="table_lqq_1qt_rhb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the System Administrator role, verify that you have the GRC core applications installed on a ServiceNow AI Platform instance.

 **Note:** The GRC applications and the ServiceNow AI Platform instance must be from the same family release.

 1.  To verify that the GRC: GRC Profile application is installed on your instance, navigate to **Plugins** and search for `GRC Profile`.
2.  If the GRC Profile core application is not installed, select **Install**.
3.  Also install the following applications as needed:
    -   GRC: Policy and Compliance Management
    -   GRC: Risk Management
    -   GRC: Audit Management
4.  After the applications have been installed, install the Continuous Authorization and Monitoring core application.
 If any application is not visible in your instance, you can download it from the ServiceNow Store. For more information about getting entitlement, downloading, and installing the GRC core applications, see [GRC and the ServiceNow Store](../../grc-common/concept/grc-and-store.md).

</td></tr><tr><td>

![checkbox](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a CAM Administrator, make sure you assign the necessary roles to users and groups as described in the [Assign Continuous Authorization and Monitoring roles to users and groups](assign-cam-roles.md).

</td></tr></tbody>
</table>
## Result

Congratulations! You have successfully set up the CAM base system. Many of the elements included in the base system can be customized for your particular business needs. Refer to the links in the checklist for more information.

