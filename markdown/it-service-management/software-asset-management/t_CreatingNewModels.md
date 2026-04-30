---
title: Create new models using the legacy Software Asset Management plugin
description: If the automatically generated software model is not correct or if the system cannot find a match from existing models, you can create a new model using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software discovery models in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create new models using the legacy Software Asset Management plugin

If the automatically generated software model is not correct or if the system cannot find a match from existing models, you can create a new model using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Discovery models** and open a model.

2.  Clear the **Software model** field.

3.  Save the record.

    Two related links appear for creating software models.

4.  Select one of these related links to create a new model, which are available only if no **Software model** is specified.

    -   **Create Software Model**: Creates a new software model for this record if a suitable one does not already exist. You can create a new software model for multiple records in the Discovery Models list view. Select one or more records and then click the link in the **Actions** choice list.
    -   **Create Software Model and Counter**: Creates a new software model and a new software counter for this record. The system creates the software model automatically using the value in the **Display name** field, and then opens a new Software Counter form. In the Discovery Model list view, you can select multiple records and choose this option from the **Actions** choice list.
5.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Display name|\[Read-only\] Name of the discovery model as it appears in record lists.|
    |Publisher|\[Read-only\] Publisher of the software.|
    |Version|\[Read-only\] Specific version of the software.|
    |Revision|\[Read-only\] Revision number of the software.|
    |Software model|Software product model to which the discovery model maps. Click the reference lookup icon and use the lookup list to find the software model to associate with this software discovery model.|
    |Prod id|\[Read-only\] Product ID code for the software, as reported through the discovery process.|
    |Automatically matched|\[Read-only\] Check box that indicates whether the discovery tool used the **Display Name**, **Publisher**, and **Version** fields to determine the **Software model**.|
    |Approved|Check box that indicates whether the mapping to software model has been reviewed and approved.|
    |Low confidence|\[Read-only\] Check box that indicates whether the automatically matched software model is not a close match. If selected, and if after reviewing the item it is determined that it's the correct software model, click **Confirm Mapping** to match the discovery model to the software model.|

6.  Select **Approved**.

    ![SAM match model](../image/SAMMatchModel.png "SAM match model")

7.  Click **Submit**.


**Parent Topic:**[Software discovery models in the legacy Software Asset Management plugin](../concept/c_UsingSoftwareDiscoveryModels.md)

