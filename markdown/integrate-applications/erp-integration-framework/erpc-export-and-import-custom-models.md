---
title: Export and import custom models in Zero Copy Connector for ERP
description: Move a custom ERP \(Enterprise Resource Planning\) model from one instance to another by exporting and importing a remote update set.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, export, import, move, model, instance, update, set]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Export and import custom models in Zero Copy Connector for ERP

Move a custom ERP \(Enterprise Resource Planning\) model from one instance to another by exporting and importing a remote update set.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Confirm that the application scope for the custom model exists on the instance to which you're importing it.

The **glide.attachment.extensions** system property restricts the file types that can be downloaded. This property is empty by default. Check that the XML file extension hasn't been added to this property. For more information, see [Security settings properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_GeneralSecuritySettings.md).

## About this task

You might need to move a custom ERP model from one instance to another. For example, after creating a custom ERP model in a non-production instance, you need to move the model to a production or another non-production instance. Export the custom ERP model and all of its related files, such as entities and operations, into an XML file within a remote update set. Then, import the remote update set into another instance.

The XML file contains:

-   Operations
-   Entities
-   Input fields
-   Output fields

Note the following rules when exporting and importing custom ERP models:

-   Internal models can't be exported and imported.
-   The system value isn't imported.
-   Only one model can be exported at a time.

**Note:** A new version of the model is created when you export a model. For more information, see [Using model versioning](erp-use-model-versioning.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  On the **Models** page, select the custom model to export.

3.  Select **Export**.

    ![Model record with export button highlighted.](../image/erpc-export-model1.png)

4.  Specify a location for the downloaded file.

    By default, this location is the downloads folder for Google Chrome and Safari browsers. The export process might take a few minutes depending on the size of the model.

5.  Navigate to the download location and confirm that the XML file is there.

    The file name should look similar to **sys\_remote\_update\_set\_f08252b6c3da16106f44d1af050131d0.xml**.

6.  Open the instance to which you're importing the custom model.

    The following steps use update sets. For general information, see [Exploring System Update Sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/exploring-system-update-sets.md).

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  In **Related Links**, select **Import Update Set from XML**.

    3.  Select **Choose File**, navigate to the XML file you exported, select the file, and select **Open**.

    4.  Select **Upload**.

        The file is imported and displayed in the retrieved update sets list with the **State** set to **Loaded**. If the import fails, check that the application scope for the custom model exists on the instance to which you're importing it.

        ![Retrieved update sets list with imported update set shown with a state of loaded.](../image/erpc-export-model2.png)

    5.  Select the file.

    6.  Select **Preview Update Set** and check for any errors, such as a collision.

        For detailed information about previewing and resolving issues, see [Preview a remote update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_PreviewARemoteUpdateSet.md) .

    7.  When you're finished previewing and have resolved any errors, select **Close**.

    8.  Select **Commit update set** to create a local copy.

        For detailed information about the update set commit process, see [Commit an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/t_CommitAnUpdateSet.md) .

    9.  When the local copy is created, select **Close**.

7.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

8.  On the **ERP Models** page, find and open the model you imported.

9.  Confirm that you're in the correct application scope.

10. Specify an **ERP system**.

11. Make any other necessary changes to the model.

    For detailed information about editing and managing models, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).


**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

