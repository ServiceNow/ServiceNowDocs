---
title: Configure an e-signature provider
description: Configure an electronic signature provider to enable users to sign contract documents electronically.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring external applications for Contract Management Pro, Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure an e-signature provider

Configure an electronic signature provider to enable users to sign contract documents electronically.

## Before you begin

Ensure that the administrator has installed and set up spokes in Integration Hub for the electronic signature providers that you want to configure.

-   **[Adobe Sign spoke](https://www.servicenow.com/docs/access?context=adobe-sign-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) v2.5.1 or later version**

    For more information on the setup and synchronizing the Adobe Acrobat Sign group, see [Synchronize Adobe Acrobat Sign group with ServiceNow](https://www.servicenow.com/docs/access?context=setup-adobe-sign&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **[DocuSign spoke](https://www.servicenow.com/docs/access?context=docusign-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) v3.3.0 or later version**

    For more information on the setup and creating the Docusign account, see [Set up Docusign eSignature spoke using authorization code grant](https://www.servicenow.com/docs/access?context=setup-docusign-authorization-code&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).


Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Integrations** &gt; **Integrations**.

2.  Create or modify an external app configuration.

    -   To create an external app configuration, click **New**.
    -   To modify an existing external app configuration, open the external app configuration from the list.
3.  On the Contract Integration Type page, click the **Electronic Signature** link.

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

Option for marking the external app configuration as active.

</td></tr><tr><td>

Table

</td><td>

Table configured to store the request details for your application. For example, if your application initiates a contract for incidents, select the table Incident \[incident\]. Similarly, select the Contract \[ast\_contract\] table for contract repository.

**Note:** If you select a different table, you must associate a corresponding flow.

</td></tr><tr><td>

Condition

</td><td>

Filter conditions to determine which integration account to use.For example, say you've already set up the Docusign electronic signature account and want only NDA contracts to use that account for signatures, you can define the condition as follows:

**\[Category\]** **\[is\]** **\[NDA\]** and then select the Docusign in the **Integration provider** and its associated account in **Account**.

</td></tr><tr><td>

Execution order

</td><td>

Order in which an integration account is used for electronic signature of contract documents. Integration account with the lower-order value is chosen first.

</td></tr><tr><td>

App

</td><td>

Electronic signature provider such as Adobe Acrobat Sign or Docusign.

</td></tr><tr><td>

Account

</td><td>

Account number associated with the electronic signature provider.This field appears only when **Docusign** is selected from **Integration provider**.

</td></tr><tr><td>

Group

</td><td>

Group associated with the electronic signature provider.This field appears only when **Adobe Acrobat Sign** is selected from **Integration provider**.

</td></tr><tr><td>

Attributes

</td><td>

Additional configuration items based on your electronic signature provider. Provide the following details:**Host Url**: Add the URL of the selected electronic signature provider that enables you to finalize or update the contract document before sending them to signatories. For example, use Web UI URL for **Adobe Acrobat Sign** or use **Docusign** UI for DocuSign.

</td></tr></tbody>
</table>5.  Save the external app configuration.

    -   Save a new external app configuration by clicking **Submit**.
    -   Save the changes to an existing external app configuration by clicking **Update**.

## Result

The configuration for the external storage system is ready to be used for storing contract documents.

**Note:** \(Optional\) You can view, edit, and delete the record.

**Parent Topic:**[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

