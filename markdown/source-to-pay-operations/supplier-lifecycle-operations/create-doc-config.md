---
title: Create a supplier document configuration
description: Create a supplier document configuration to define when to run the configuration, who can view the upload request and upload the documents, and whether to send notifications when documents are uploaded or have expired.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Supplier Document Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create a supplier document configuration

Create a supplier document configuration to define when to run the configuration, who can view the upload request and upload the documents, and whether to send notifications when documents are uploaded or have expired.

Create a supplier document configuration 

## Before you begin

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Do one of the following.

<table id="choicetable_ur2_ykv_dvb"><thead><tr><th align="left" id="d82569e70">

To

</th><th align="left" id="d82569e73">

Do This

</th></tr></thead><tbody><tr><td id="d82569e79">

**Create a document configuration from the Platform UI**

</td><td>

Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Administration** &gt; **Document Configuration**

</td></tr><tr><td id="d82569e103">

**Create a document configuration from the Source-to-Pay Workspace**

</td><td>

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.
2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\) and navigate to **Lists** &gt; **Administration** &gt; **Document Configuration**.


</td></tr></tbody>
</table>2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|The name you assign to the configuration.|
    |Application|The application containing this record. In this case, it displays the default application, which is Supplier Collaboration Portal.|
    |Order|The order in which you want this configuration to be displayed in the list of orders. Assign a numeric value in multiples of 100.|
    |Active|Option to decide if this configuration is in use.|
    |Description|A brief description of the configuration.|

4.  Select the **Run condition** tab and fill in the fields.![Selected Run condition tab.](../image/supplier-document-config-run-condition.png)

<table id="table_cy1_twr_z5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

When to run

</td><td>

When you want the configuration to run. The choices are:-   **On demand**: The configuration runs when you select **Execute Now** on the Supplier Document Configuration form.

You can use this option to run the configuration immediately without waiting for the other run conditions to be met. For more information, see [Manually run a supplier document configuration](run-doc-config.md).

-   **When supplier record inserted**: The configuration runs when a new supplier record is created.
-   **When supplier record updated**: The configuration runs when an existing supplier record is updated.
-   **When supplier record inserted/updated**: The configuration runs when a new record is created or an existing supplier record is updated.


</td></tr><tr><td>

Supplier condition

</td><td>

Specify when the configuration must run when specific conditions are met.

</td></tr><tr><td>

Advanced

</td><td>

Option to use a script to specify when the configuration is run.

</td></tr></tbody>
</table>5.  Select the **Upload preferences** tab and fill in the fields.![Selectd Upload preferences tab.](../image/supplier-document-config-upload-preferences.png)

<table id="table_wg2_5wr_z5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required from

</td><td>

Specify who must upload the document. The choices are:-   **Anyone**: Requires any one of the supplier contacts to upload the required document. With this option, the supplier contact can upload a document from the Document widget on the My Company page of the Supplier Collaboration Portal.

For more information, see [Manage documents from the Supplier Collaboration Portal](upload-doc-portal.md).

-   **Everyone**: Requires each supplier contact to upload the required document.

The **Generate task for** field becomes available if you select **Everyone** in the **Required from** field. Select **Yes** in the **Generate task for** field to generate the Upload Document task for each supplier contact.

With this option, the supplier contact can upload the document from either of these locations in the Supplier Collaboration Portal:

    -   ****Documents widget on the My Company page
    -   Upload Document task on the My To-dos page

For more information, see [Manage documents from the Supplier Collaboration Portal](upload-doc-portal.md).

</td></tr></tbody>
</table>6.  Select the **Manage access** tab and fill in the fields.![Selected Manage access tab.](../image/supplier-document-config-manage-access.png)

    |Field|Description|
    |-----|-----------|
    |View access|Users with this access can only read the document.|
    |Upload/Update access|Users with this access can update and upload the document.|
    |Admin access|Users with this access can read, update, and upload the document.|

    **Note:** On the **Manage access** tab, assign access to users or user groups based on the user criteria permissions.

7.  Select the **Notification** tab and fill in the fields.![Selected Notification tab.](../image/supplier-document-config-notification.png)

<table id="table_p13_ywr_z5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notify on upload

</td><td>

Controls whether a notification is sent when a document is uploaded. The options are:-   **Yes**
-   **No**


</td></tr><tr><td>

Whom to notify on upload

</td><td>

The user that you want to notify when the document is uploaded.This field becomes available only if you select **Yes** in the **Notify on upload** field. Search for the users using the search icon in the **Select target record** field.

</td></tr><tr><td>

Notify on expiry

</td><td>

Controls whether a notification is sent when a document expires. The options are:-   **Yes**
-   **No**


</td></tr><tr><td>

Whom to notify on expiration

</td><td>

The user that you want to notify when the document expires.This field becomes available only if you select **Yes** in the **Notify on expiry** field. Search for the users using the search icon in the **Select target record** field.

</td></tr></tbody>
</table>8.  Select **Save** to remain on the Supplier Document Configuration form.

    **Note:** The Suppliers related list displays all the suppliers for whom the supplier document configuration is applicable.

9.  In the Supplier Document Types related list, select **New**.

    **Note:** If you want to create a supplier document type from the Source-to-Pay Workspace, do the following:

    1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.
    2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\) and navigate to **Lists** &gt; **Administration** &gt; **Document Configuration**.
    3.  Open a supplier document configuration, select the **Supplier Document Types** tab, and then select **New**.
10. On the form, fill in the fields.

<table id="table_d2l_qgr_z5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name for the document type.

</td></tr><tr><td>

Type

</td><td>

The type of the document. The choices are:-   **Policy**
-   **Guideline**
-   **Procedure**
-   **Contract**


</td></tr><tr><td>

Document Configuration

</td><td>

The document configuration that you want to associate the document type with.

</td></tr><tr><td>

Order

</td><td>

The order in which you want the configuration to be displayed in the list of orders. Assign a numeric value in multiples of 100.

</td></tr><tr><td>

Days to expiry

</td><td>

Number of days before the document expires.**Note:** After a document expires, a notification is sent to the users stating that the document has expired and a new version of the document must be uploaded.

The notification is sent only if the **Notify on expiry** field is set to **Yes**. The notification is sent to the users you specify in the **Whom to notify on expiration** field.

After a document expires, it is marked as Expired in the Documents widget in the Supplier Collaboration Portal. The Expired marking is removed when you upload an updated version of that document.

</td></tr><tr><td>

Template

</td><td>

Option that enables you to attach a template that specifies the expected format of the document to upload.Select the Manage Attachments icon \(![Add attachments icon.](../image/attachments-icon.png)\) to attach a template.

</td></tr><tr><td>

Description

</td><td>

A brief description of the document type.

</td></tr></tbody>
</table>11. On the **Upload preferences**, **Manage access**, and **Notification** tabs, specify the values that you want the document type to use.

    **Note:** The field values that you set in these tabs override the field values that you set in the corresponding tabs for the document configuration you associate this document type with.

12. Select **Submit**.


**Parent Topic:**[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

**Related topics**  


[Manually run a supplier document configuration](run-doc-config.md)

[Uploading supplier documents](../concept/upload-doc-about.md)

[Manually run a supplier document configuration](run-doc-config.md)

[Uploading supplier documents](../concept/upload-doc-about.md)

