---
title: Configure an external storage system
description: As a contract configurator, configure an external storage system to store signed contract documents.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure external applications, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure an external storage system

As a contract configurator, configure an external storage system to store signed contract documents.

## About this task

The following video walks you through the process of configuring external storage for Contract Management Pro.Video explaining how to configure external storage for Contract Management Pro, approximately two minutes long. 

## Before you begin

Ensure that the administrator has installed and set up spokes for the external storage system you want to configure.

-   **[Google Drive spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/googledrive-spoke.md) v1.3.0 or later version**

    For more information on the setup and creating the Google Drive account, see [Set up Google Drive spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-gdrive.md).

    **Note:** Word \(.docx\) files edited directly from Google Drive using Google Docs may become incompatible with Contract Management Pro causing failures during processing, signature operations, and document updates. To avoid these issues, download the .docx file from the Google Drive, edit it in Microsoft Word \(desktop or online\), and upload it into the system using the Create Revision option.

-   **[Microsoft OneDrive spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/onedrive-spoke.md) v2.1.0 or later version**

    For more information on the setup and creating the Microsoft OneDrive account, see [Set up Microsoft OneDrive spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-msonedrive.md).


Role required: sn\_cm\_core.contract\_config

## About this task

On configuring external storage, access permissions are granted to users associated with the contract request depending on the contract request state and contract document status.

All user roles automatically have Read permission.

Write permission is granted to the following user roles when the contract request state is Work in progress or New and the contract document status is not Preparing for signature:

-   Assigned To
-   Assignment Group Manager
-   Collaborator

Access permissions set on the parent request folder are automatically inherited by all sub folders and documents within it.

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Integrations** &gt; **Integrations**.

2.  Create or modify an external app configuration.

    -   To create an external app configuration, click **New**.
    -   To modify an existing external app configuration, open the existing external app configuration from the list.
3.  On the Contract Integration Type page, click the **External Storage** link.

    ![External storage form](../image/cmpro-external-storage.png "External storage configuration form")

4.  On the form, fill in the fields.

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

Table configured to store the request details for your application. All the documents attached to the records created in the selected table are stored in the external storage you are configuring.For example, if you configure Google Drive as the external storage and select Contract Request table \[sn\_cm\_core\_contract\_request\], then all the documents attached to the records created in the Contract Request table will be automatically stored in Google Drive.

**Note:** The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure a different table to configure external storage.

**Note:** If you select a different table, you must associate a corresponding flow.

</td></tr><tr><td>

Condition

</td><td>

Filter conditions to determine which integration app to use.For example, say you've already set up the Google Drive external storage integration and want to store only NDA contracts there, you can define the condition as follows:

**\[Category\]** **\[is\]** **\[NDA\]** and then select the Google Drive.

Similarly, you can define conditions based on region, for example, **\[Location\]** **\[is\]** **\[United States\]** and then select the Google Drive or **\[Location\]** **\[is\]** **\[India\]** and select the Microsoft OneDrive for better discovery.

</td></tr><tr><td>

Execution order

</td><td>

Order in which an external storage system is used for storing contract documents. The system with the lower-order value is chosen first.

</td></tr><tr><td>

App

</td><td>

External storage system such as Google Drive or Microsoft OneDrive.

</td></tr><tr><td>

Folder structure

</td><td>

Filepath to store the signed contract documents in the external storage system.Define a folder structure using a combination of static text and dynamically generated text from the selected fields. For example, the folder structure `Legal/${company}/Contracts/${number}`, where,

-   `Legal` and `Contracts` are the static texts
-   `${company}` and `${number}` are the fields chosen from the **Select variables** list.

These field variables are dynamically replaced by the values in each field while saving a document.

</td></tr></tbody>
</table>5.  Save the external app configuration.

    -   Save a new external app configuration by clicking **Submit**.
    -   Save the changes to an existing external app configuration by clicking **Update**.

## Result

The external storage system is configured and ready to be used for storing contract documents.

**Note:** \(Optional\) You can view, edit, and delete the record.

For information on configuring electronic signature provider, see [Configure an e-signature provider](cncore-integrate-esign.md).

**Parent Topic:**[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

**Related topics**  


[Configure an e-signature provider](cncore-integrate-esign.md)

