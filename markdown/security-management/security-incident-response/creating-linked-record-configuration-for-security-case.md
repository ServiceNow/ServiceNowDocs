---
title: Step 1. Create linked record configuration for a Security Case
description: Create a Linked Record configuration for a Security Case.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Rollup example use case implementation for a Security Case, Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Step 1. Create linked record configuration for a Security Case

Create a Linked Record configuration for a Security Case.

## Before you begin

Role required: admin and sn\_msi.workspace\_admin

**Note:** The system admin can create the record and MSI workspace admin can update it.

## Procedure

1.  Search for the Linked Record Configuration from the left navigation.

2.  Click **New**.

    ![New button](../image/linked-record-new.png)

3.  Fill the form with the required columns and write a field mapping script.

    ![Fill the form](../image/linked-record-fill-form.png)

4.  You have now created a linked record configuration for the Security Case by adding the values as described in the following table.

    ![Create](../image/linked-record-create.png)

<table id="table_qqw_h5d_35b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Table

</td><td>

Security Case \(sn\_ti\_case\). Here in this example, link/promote/propose a security case as MSI.

</td></tr><tr><td>

Order

</td><td>

Input value: 300**Note:** Lower the order takes precedence over higher orders. As a Security Case have a higher order than the Security Incident and Remediation Task, it will appear in the last sequence.

</td></tr><tr><td>

Can promote to MSI

</td><td>

True, select this check box to promote the security case to MSI.**Note:**

-   Link and Unlink security case records to major security incidents both from Major Security Incident Management workspace. Also, Unlink record functionality is visible only for the linked records.
    -   This will enable the link, promote, and propose to Security Case to Major Security Incident using classic environment actions, but those UI actions will not be available out of the box. Each UI action needs to be created manually. For more information, see [Step 3. Create UI actions for the Source Table for a Security Case](creating-ui-actions-for-source-table.md).
    -   Link/Promote/Propose UI action are available for Security Incident, Remediation Task, and Security Case out of the box.
-   MSIM workspace linked record page will show the linked Security Case records.
 Refer to the below image 1 to view the options available after selecting this check box.

</td></tr><tr><td>

Modal List View

</td><td>

msim\_sn\_ti\_case\_model\_view**Note:** This view contains fields and fields order shown in list view on the Link Record Modal in MSIM workspace. For more information, see [Step 2. Create a view for modal window for a Security Case](creating-a-view-for-modal-window-for-security-case.md)

 Refer to the below image 2 to view from the **Linked Records** page.

</td></tr><tr><td>

Field Mapping Script

</td><td>

This script describes the fields from source tables record will mapped to newly created major security incident when source tables record is getting proposed or promoted.which will receive inputs:

-   sourceGr: security case glide record object
-   msiGr: major security incident glide record object
 Script will read from the short description of the security case and copy it over as title to major security incident.

</td></tr></tbody>
</table>    ![Can promote to MSI](../image/can-promote-to-msi-step1.png "Image 1: Can Promote to MSI")

    ![Modal view](../image/modal-view-step1.png "Image 2. Modal View")


**Parent Topic:**[Rollup example use case implementation for a Security Case](../concept/use-case-for-a-security-case.md)

