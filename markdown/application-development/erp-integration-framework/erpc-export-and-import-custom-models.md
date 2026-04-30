---
title: Export and import custom models in Zero Copy Connector for ERP
description: Move a custom ERP model from one instance to another by exporting and importing a remote update set.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Building and managing ERP models to work with ERP data, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Export and import custom models in Zero Copy Connector for ERP

Move a custom ERP model from one instance to another by exporting and importing a remote update set.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Confirm that the application scope for the custom model exists on the instance to which you're importing.

The glide.attachment.extensions system property restricts the file types that can be downloaded. This property is empty by default. Check that the xml file extension has not been added to this property. For more information, see [Restrict attachment file extensions](https://www.servicenow.com/docs/access?context=t_DisablingTheDragAndDropFeature&version=yokohama&pubname=yokohama-platform-administration&section=t_RestrictingFileExtensions&ft:locale=en-US).

## About this task

You may need to move a custom ERP model from one instance to another. For example, after creating a custom ERP model in a non-production instance, you need to move the model to production or another non-production instance. Export the custom ERP model and all of its related files, such as entities and operations, into an XML file within a remote update set. Then, import the remote update set into another instance.

The XML file contains:

-   Operations
-   Entities
-   Input fields
-   Output fields

Note the following when exporting and importing custom ERP models:

-   Internal models can't be exported and imported.
-   The system value isn't imported.
-   One model can be exported at a time.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  On the **Models** page, select the custom model to export.

3.  Select **Export**.

    ![Model record with export button highlighted.](../image/erpc-export-model1.png)

4.  Specify a location for the downloaded file \(by default in the Chrome and Safari browsers, this location is the Downloads folder\).

    The export process may take a few minutes depending on the size of the model.

5.  Navigate to the download location and confirm that the XML file is there.

    The file name should look similar to **sys\_remote\_update\_set\_f08252b6c3da16106f44d1af050131d0.xml**.

6.  Open the instance to which you're importing the custom model.

    The following sub steps use update sets. For general information, see [System update sets](../../system-update-sets/concept/system-update-sets.md).

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  In **Related Links**, select **Import Update Set from XML**.

    3.  Select **Choose File**, navigate to the XML file you exported, select the file, and select **Open**.

    4.  Select **Upload**.

        The file is imported and displayed in the retrieved update sets list with the **State** set to **Loaded**. If the import fails, check that the application scope for the custom model exists on the instance to which you're importing.

        ![Retrieved update sets list with imported update set shown with a state of loaded.](../image/erpc-export-model2.png)

    5.  Select the file.

    6.  Select **Preview Update Set** and check for any errors, such as a collision.

        For detailed information about previewing and resolving any issues, see [Preview a remote update set](../../system-update-sets/task/t_PreviewARemoteUpdateSet.md#).

    7.  When you're finished previewing and have resolved any errors, select **Close**.

    8.  Select **Commit update set** to create a local copy.

        For detailed information about the update set commit process, see [Commit an update set](../../system-update-sets/task/t_CommitAnUpdateSet.md).

    9.  When the local copy is created, select **Close**.

7.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

8.  On the **ERP Models** page, find and open the model you imported.

9.  Confirm that you are in the correct application scope.

10. Specify an **ERP system**.

11. Make any other necessary changes to the model.

    For detailed information about editing and managing models, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).


**Parent Topic:**[Building and managing ERP models to work with ERP data](../concept/work-with-erp-data-models.md)

