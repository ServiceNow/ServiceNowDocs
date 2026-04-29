---
title: Configure Linked Records in Major Security Incident Management
description: Use Linked Records Configuration to store the information of task tables that can be used to link/promote/propose to Major Security Incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Linked Records in Major Security Incident Management

Use Linked Records Configuration to store the information of task tables that can be used to link/promote/propose to Major Security Incident.

Role required: admin and sn\_msi.workspace\_admin.

**Note:** Admin can create the record and MSIM workspace admin can update the record.

**Procedure**

1.  Navigate to **Major Security Incident Management** &gt; **Linked Record Configurations**.

    The Linked Record Configuration page displays.

    ![Linked Record configuration](../image/linked-record-config.png "Linked Record Configuration")

2.  On the Linked Record Configuration page, click **New**

    **Note:** Ensure that the application is in Major Security Incident Management scope.

    ![Create record](../image/linked-record-new-form.png)

3.  On the record configuration form, fill in the fields.

<table id="table_swd_yks_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Table

</td><td>

Indicates the task table that must be linked and rolled up to Major Security Incident.

</td></tr><tr><td>

Order

</td><td>

Allows you to control the order of the current source table in MSIM workspace drop-down. Below is an example of the **order**.Refer to image 1 below, which is provided after this table.

</td></tr><tr><td>

Model ListView

</td><td>

Select a view which can control the list layout that is shown in the Linked Record Modal List.

</td></tr><tr><td>

Can Promote to MSI

</td><td>

Select this check box to confirm whether the record is a primary record. Below is an example of **Can Promote to MSI** option selection.Refer to the following image 2, which is provided after this table.

 If this check box is selected and the value is true, then:

-   you can directly propose and promote a source record to Major Security Incident using the classic environment actions with additional configurations.
-   you can link source records to major security incidents both from the classic environment and MSIM workspace.
-   Major Security Incident Management workspace linked record page displays the linked source table records.
 **Note:** If a record can be directly proposed/promoted as a Major Security Incident, then that record is a primary record. For example, in the Security Response task table configuration, the value of **Can Promote to MSI** is false as you can't directly promote Security Response task to Major Security Incident. Hence, it does not show up in the MSIM workspace linked record tab drop-down list.

</td></tr><tr><td>

MSI Field Mapping

</td><td>

Write a script to map the source record fields to a newly created major security incident when the source tables record is in the process of being proposed or promoted.This script executes only when **Can Promote to MSI** value is true.

</td></tr></tbody>
</table>    ![Order of the dropdown list](../image/linked-record-config-order.png "Image 1: Linked Records list view order")

    ![Can promote to MSI](../image/linked-can-promote-to-msi.png "Image 2: Can Promote to MSI")


**Parent Topic:**[Rollup Framework for MSIM](../concept/roll-up-framework-for-major-security-incident-management.md)

**Related topics**  


[Configure Rollup Records in Major Security Incident Management](../concept/roll-up-record-configuration-in-major-security-incident-management.md)

[Configure List Layout in Major Security Incident Management](../concept/list-layout-confguration.md)

[Rollup example use case implementation for a Security Case](../concept/use-case-for-a-security-case.md)

[Perform on demand atomic rollup](../concept/perform-on-demand-atomic-rollup.md)

