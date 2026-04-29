---
title: Configure an external storage system for legal contracts
description: Configure an external storage system to store signed contract documents.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring external applications for legal contracts, Configure, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure an external storage system for legal contracts

Configure an external storage system to store signed contract documents.

## Before you begin

Ensure that the administrator has installed and set up spokes for the external storage system you want to configure.

-   **[Google Drive spoke](https://www.servicenow.com/docs/access?context=googledrive-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) v1.3.0 or later version**

    For more information on the setup and creating the Google Drive account, see [Set up Google Drive spoke](https://www.servicenow.com/docs/access?context=setup-gdrive&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **[Microsoft OneDrive spoke](https://www.servicenow.com/docs/access?context=onedrive-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) v2.1.0 or later version**

    For more information on the setup and creating the Microsoft OneDrive account, see [Set up Microsoft OneDrive spoke](https://www.servicenow.com/docs/access?context=setup-msonedrive&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) .


Role required: sn\_lg\_cnt.contract\_admin

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Integrations** &gt; **Integrations**.

2.  Create or modify an external app configuration.

    -   To create an external app configuration, click **New**.
    -   To modify an existing external app configuration, open the external app configuration from the list.
3.  On the Integration Type page, click the **External Storage** link.

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

Table in which the signed legal contracts information is stored.Select the **Legal Contract Request \[sn\_lg\_ops\_contract\_request\]** table.

**Note:** If you select a different table, you must associate a corresponding flow.

</td></tr><tr><td>

Condition

</td><td>

Filter conditions to determine which integration app to use.For example, say you've already set up the Google Drive external storage integration and want only NDA contracts to be stored there, you can define the condition as follows:

 **\[Category\]** **\[is\]** **\[NDA\]** and then select the Google Drive.

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
    The external storage configuration is saved.

6.  Click **Publish**.


## Result

The configuration for the external storage system is published and is ready to be used for storing contract documents.

**Parent Topic:**[Configuring external applications for legal contracts](../concept/snlc-set-legal-ext-app-config.md)

