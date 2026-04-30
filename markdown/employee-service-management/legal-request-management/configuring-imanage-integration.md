---
title: Integrating Legal Service Delivery applications with iManage storage
description: Integrate iManage storage with Legal Service Delivery applications to provide more security to the files.
locale: en-US
release: xanadu
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure an external storage system for legal requests and legal matters, Setting up Legal Request Management, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Integrating Legal Service Delivery applications with iManage storage

Integrate iManage storage with Legal Service Delivery applications to provide more security to the files.

You can integrate iManage storage with Legal Service Delivery applications.

The three types of Integrations are:

-   Shared Workspace — To use an existing Workspace and folder to upload documents, use the Shared Workspace when needed. For example, you may want to organize the documents by Practice areas. So, you’d follow a shared Workspace scenario where the legal request or legal matter related folders are created inside the existing Workspace and the documents are uploaded to the folders.
-   Independent Workspace using a template — To track every request or matter separately and upload documents, use the Independent Workspace when needed. Using a pre-defined iManage template helps you maintain consistent names and folder structure for the Workspace in iManage. The documents are uploaded using the folder mentioned in the Folder\_path field.
-   Independent Workspace without a template — When you want to track every request or matter separately and upload documents respectively using the folder mentioned in the Folder\_path field, use the Independent Workspace.

## Shared Workspace

In Shared Workspace, workspaces are shared between the ServiceNow® users registered on iManage and iManage storage.

|Attribute|Optional/Mandatory|Sample Values \(Manual input\)|
|---------|------------------|------------------------------|
|Library|Optional|None|
|Workspace\_type|Mandatory|Shared|
|Template\_ID|Not applicable|Not applicable|
|Folder\_path|Not applicable|Not applicable|
|Shared\_workspace\_ID|Mandatory|Legal!123|

-   **Folder structure**: &lt;folder&gt;/$\{number\}.
-   **How it works**: When a document is uploaded, the application uses an existing Workspace \(Legal\) and reuses the primary folder. The application creates the folder under this folder hierarchy using the legal request or legal matter number and uploads the document in this path.

    The following example shows the document is uploaded in the specific folder.

    **Note:** If any of the folders don’t exist, then the application creates them first and subsequently uses them. In this example, it is $\{number\}.

    **Legal \(Workspace\) &gt; Folder &gt; LR001**.


## Independent Workspace using a template

|Attribute|Optional/Mandatory|Sample values|
|---------|------------------|-------------|
|Library|Optional|None|
|Workspace\_type|Mandatory|Independent|
|Template\_ID|Mandatory|LegalTemplate!120|
|Folder\_path|Mandatory|Documents|
|Shared\_workspace\_ID|Not applicable|Not applicable|

-   **Folder structure**: $\{number\}.
-   **How it works**: The application creates a Workspace using the value provided in the folder structure field as the workspace name and creates the folders as defined in the template. In this example, LegalTemplate!123 is the Template\_ID that is used as the template. Then use the folder path provided in the Folder\_path field to upload the document to the folder in the path. In this example, the document file is uploaded to the Documents folder.

    The following example shows the document is uploaded in the specific folder:

    **LR001 \(Workspace\) &gt; Documents \(Folder\)**.


## Independent Workspace without a template

|Attribute|Optional/Mandatory|Sample Values \(Manual input\)|
|---------|------------------|------------------------------|
|Library|Optional|None|
|Workspace\_type|Mandatory|Independent|
|Template\_ID|Not applicable|Not applicable|
|Folder\_path|Mandatory|Documents|
|Shared\_workspace\_ID|Not applicable|Not applicable|

-   **Folder structure**: $\{number\}.
-   **How it works**: The application creates a Workspace using the value provided in the folder structure field as the workspace name. The application then creates a folder using the Folder\_path field information and uploads the document to the last folder.

    The following example shows the document is uploaded in the specific folder:

    **LR001 \(Workspace\) &gt; Documents \(Folder\)**.


**Parent Topic:**[Configure an external storage system for legal requests and legal matters](../task/integrate-legal-ext-storage.md)

