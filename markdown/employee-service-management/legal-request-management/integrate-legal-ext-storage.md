---
title: Configure an external storage system for legal requests and legal matters
description: Configure an external storage system to store documents attached to legal requests and legal matters.
locale: en-US
release: yokohama
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Configure an external storage system for legal requests and legal matters

Configure an external storage system to store documents attached to legal requests and legal matters.

## Before you begin

Ensure that the administrator has installed and set up spokes for the external storage system you want to configure for legal apps.

-   **[Box spoke](https://www.servicenow.com/docs/access?context=box-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) v3.1.0 or later version**

    For more information on the setup and creating the Box account, see [Set up Box spoke](https://www.servicenow.com/docs/access?context=setup-box-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[Google Drive spoke](https://www.servicenow.com/docs/access?context=googledrive-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) v1.3.0 or later version**

    For more information on the setup and creating the Google Drive account, see [Set up Google Drive spoke](https://www.servicenow.com/docs/access?context=setup-gdrive&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[Microsoft OneDrive spoke](https://www.servicenow.com/docs/access?context=onedrive-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) v2.1.0 or later version**

    For more information on the setup and creating the Microsoft OneDrive account, see [Set up Microsoft OneDrive spoke](https://www.servicenow.com/docs/access?context=setup-msonedrive&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[Microsoft SharePoint spoke](https://www.servicenow.com/docs/access?context=sharepoint-online-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) v2.2.0 or later version**

    For more information on setting up Microsoft SharePoint, see [Configure Microsoft SharePoint Online connection record](https://www.servicenow.com/docs/access?context=set-up-microsoft-sharepoint-online-and-connection-record&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

-   **[iManage Spoke](https://www.servicenow.com/docs/access?context=imanage-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) spoke v1.0.0**

    For more information on the setup and creating the iManage account, see [Set up iManage spoke](https://www.servicenow.com/docs/access?context=set-up-imanage-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

    **Important:** After setting up the spoke, give the iManage spoke user \[sn\_imanage\_spk.user\] role to users accessing iManage external storage.


Role required: sn\_lg\_ops.request\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Integrations** &gt; **Integrations**.

2.  Create or modify an external app configuration.

<table id="choicetable_tdc_kmg_dtb"><thead><tr><th align="left" id="d414638e203">

Option

</th><th align="left" id="d414638e206">

Steps

</th></tr></thead><tbody><tr><td id="d414638e212">

**To create an external app configuration**

</td><td>

1.  Select **New**.
2.  On the Integration Type page, select the **External Storage** link.


</td></tr><tr><td id="d414638e236">

**To modify an existing external app configuration**

</td><td>

Open the external app configuration from the list.

</td></tr></tbody>
</table>3.  On the form, fill in the fields.

<table id="table_contract_request_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the external app configuration.

</td></tr><tr><td>

Description

</td><td>

Description of the external app configuration.

</td></tr><tr><td>

Active

</td><td>

Option for marking the configuration for external storage as active.

</td></tr><tr><td>

Table

</td><td>

Table in which the legal requestor legal matterinformation is stored. For example,-   To store documents for a legal request, select the **Legal Request \[sn\_lg\_ops\_request\]** table.
-   To store documents for a legal matter, select the **Legal Matter \[sn\_lg\_matter\_matter\]** table.
-   To store documents for a contract request, select the **Legal Contract \[sn\_lg\_contracts\_repository\]** table.
The selected table determines the available variables in the **Select variables** field.

</td></tr><tr><td>

Condition

</td><td>

Filter conditions to determine saving documents for a specific request category.For example, say you've already configured the Box external storage integration and want only NDA contract documents to be stored there, you can define the condition as **\[Category\]** **\[is\]** **\[NDA\]**.

Then, select the external storage name in the **App** field.

</td></tr><tr><td>

Execution order

</td><td>

Order in which an external storage system is used for storing documents. When multiple external storage systems match the conditions, then the one with the lower-order value is chosen to store the documents.

</td></tr><tr><td>

App

</td><td>

External storage system on which the documents are stored.**Note:** The list only shows external storage systems for which spokes have been installed and configured.

</td></tr><tr><td>

Folder structure

</td><td>

Filepath to store documents attached to a legal request or legal matter in the external storage system.Define a folder structure using a combination of static text and dynamically generated text from the selected field variables in the **Select variables** list.

For example, in the folder structure `Legal/${company}/Contracts/${number}`,

-   `Legal` and `Contracts` are static texts
-   `${company}` and `${number}` are the field variables chosen from the **Select variables** list.

These field variables are dynamically replaced by the values in each field while saving a document in the external storage.

</td></tr><tr><td>

Select variables

</td><td>

List of variables that can be used in the folder structure. Variables pull information from the selected table to customize the folder structure.

</td></tr><tr><td>

Attributes

</td><td>

Additional configuration items based on your Microsoft SharePoint and iManage configuration. Add the following details:**Microsoft SharePoint**

-   **Tenant**: Add the sys\_id of the [Microsoft SharePoint tenant record](https://www.servicenow.com/docs/access?context=create-tenant&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
-   **Site\_Name**: Add the name of the site in the tenant.
-   **Document Library**: Add the document library set up in the site where all documents related to legal requests and legal matters are stored.
For more information on managing Microsoft SharePoint tenants, sites, and document libraries, see the Microsoft documentation.

These fields appear only when **SharePoint** is selected from the **App** field.

**iManage**

-   **Library**: When a value is specified, the application uploads documents using the designated library. This can also include the creation or using the Workspaces, folders, and so on. This attribute is optional, so if the library is not provided, the preferred library of the iManage service account user is used.
-   **Workspace\_type**: Captures the type of Workspace to support the various use cases. For example:
    -   **Shared**: Use an existing Workspace to upload documents.
    -   **Independent**: Create a separate Workspace for every request and matter. This helps in effectively organising and tracking the documents. Independent Workspace may or may not use a template.
-   **Template\_ID**: Unique identifier of the template from iManage. The application uses the identifier to create iManage objects such as Workspaces, folders, and subfolders using the template configurations while uploading the documents. This attribute is used when the Workspace\_type is Independent. You can use templates to maintain consistent names and folder structure for Workspaces created in iManage.
-   **Folder\_path**: Used to identify the folders or subfolders, in which the document is uploaded. This attribute is used when the Workspace\_type is Independent.
-   **Shared\_workspace\_ID**: Unique identifier of the Shared Workspace. This is used to identify the Workspace to upload the documents when Workspace type is Shared.
For more information on iManage, see [iManage](https://help.imanage.com/hc/en-us/sections/4715521414683-Getting-started) documentation.

**Note:** iManage login credentials are required to access the documentation.

</td></tr></tbody>
</table>4.  Save the external app configuration.

    -   Save a new external app configuration by selecting **Submit**.
    -   Save the changes to an existing external app configuration by selecting **Update**.
    The external storage configuration is saved.

5.  Select **Publish**.


## Result

The external storage system integration is published and is ready for storing documents attached to legal requests.

## What to do next

Add the **Enable External Storage for attachment** option in the intake forms so that the documents attached to those legal requestsor legal mattersare stored in the configured external storage. For more information, see [Add an intake form to a practice area](associate-categories-practice-area.md).

Configure the system properties for Legal Service Delivery apps to administer integration with the external storage provider. For more information, see [Legal Service Delivery properties](../reference/legal-properties.md).

-   **[Integrating Legal Service Delivery applications with iManage storage](../reference/configuring-imanage-integration.md)**  
Integrate iManage storage with Legal Service Delivery applications to provide more security to the files.
-   **[Create implementation in Scripted Extension Point](create-scripted-extension-point.md)**  
Create the implementation in the Scripted Extension Point, provided out-of-the-box, by placing it in the script include in the base application code.

**Parent Topic:**[Configuring Legal Request Management](../concept/legal-ops-administration.md)

