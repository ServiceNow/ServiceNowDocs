---
title: Configure an e-signature provider
description: Configure an electronic signature provider to enable users to sign contract documents electronically.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure external applications, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure an e-signature provider

Configure an electronic signature provider to enable users to sign contract documents electronically.

## About this task

The following video walks you through the process of configuring your e-signature provider for Contract Management Pro.Video explaining how to configure e-signature provider for Contract Management Pro, approximately two minutes long. 

## Before you begin

Ensure that the administrator has installed and set up spokes in Integration Hub for the electronic signature providers that you want to configure.

-   **Adobe Sign spoke v2.8.0 or later version**

    For more information on the setup and synchronizing the Adobe Acrobat Sign group, see Synchronize Adobe Acrobat Sign group with ServiceNow.

-   **DocuSign spoke v4.1.x or later version**

    For more information on the setup and creating the Docusign account, see Set up Docusign eSignature spoke using authorization code grant.


Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Integrations** &gt; **Integrations**.

2.  Create or modify an external app configuration.

    -   To create an external app configuration, click **New**.
    -   To modify an existing external app configuration, open the external app configuration from the list.
3.  On the Contract Integration Type page, click the **Electronic Signature** link.

    ![Electronic signature form](../image/cmpro-electronic-signature.png "E-signature configuration form")

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

Table configured to store the request details for your application. All documents attached to records created in the selected table uses the configured electronic signature provider for signing. For example, if you configure Docusign as the electronic signature provider, and select the Contract Request table \[sn\_cm\_core\_contract\_request\], then all the contract documents attached to contract requests created in the Contract Request table will follow the Docusign e-signature flow for signing.

 **Note:** The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure a different table to configure electronic signature provider.

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

Account associated with the Docusign integration for Contract Management Pro.A Docusign account is used to manage users, templates, and documents. Organizations can configure separate accounts for different departments such as Legal or Procurement to manage their own signing workflows and permissions independently.

This field appears only when Docusign is selected in the **App** field.

</td></tr><tr><td>

Group

</td><td>

Group associated with the Adobe Acrobat Sign integration for Contract Management Pro. Adobe Acrobat Sign groups are used to organize users and their documents based on teams or departments like Legal or Procurement so that each group can manage its own signing workflows and permissions separately.

This field appears only when Adobe Acrobat Sign is selected in the **App** field.

</td></tr><tr><td>

Attributes

</td><td>

Additional configuration items based on your electronic signature provider. Provide the following details:**Host Url**: Add the URL of the selected electronic signature provider that enables you to finalize or update the contract document before sending them to signatories. For example, use Web UI URL for **Adobe Acrobat Sign** or use **Docusign** UI for DocuSign.

</td></tr></tbody>
</table>5.  Save the external app configuration.

    -   Save a new external app configuration by clicking **Submit**.
    -   Save the changes to an existing external app configuration by clicking **Update**.

## Result

The conﬁguration for the electronic signature is ready to be used for signing contract documents.

**Note:** \(Optional\) You can view, edit, and delete the record.

For information on configuring external storage, see [Configure an external storage system](cncore-integrate-ext-storage.md).

**Parent Topic:**[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

**Related topics**  


[Configure an external storage system](cncore-integrate-ext-storage.md)

