---
title: Configuring external applications for Contract Management Pro
description: Set up external applications that provide services such as electronically signing contract documents and saving signed contracts or the documents related to requests in an external storage system.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configuring external applications for Contract Management Pro

Set up external applications that provide services such as electronically signing contract documents and saving signed contracts or the documents related to requests in an external storage system.

The Contract Management Pro application use spokes from Integration Hub to integrate with external applications. The contract configurator \(sn\_cm\_core.contract\_config\) can complete configuring these external apps after the administrator completes installation and configuration of these spokes.

## Integration with external storage systems

-   **Configure external storage provider spokes**

    The administrator can use the Integration Hub to install and configure the following external storage provider spokes for saving documents attached to contract requests and signed contract documents:

    -   [Google Drive spoke](https://www.servicenow.com/docs/access?context=googledrive-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)
    -   [Microsoft OneDrive spoke](https://www.servicenow.com/docs/access?context=onedrive-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)
-   **Configure an external storage provider**

    The contract configurator can set up the external storage app integrations from **Contract Integrations**. For more information, see [Configure an external storage system](../task/cncore-integrate-ext-storage.md).

-   **External storage permissions**

    The permissions are granted at request level. All document folders and documents within the request folder inherit the permissions from the parent folder.

    All user roles automatically have Read permission.

    Write permission is granted to the following user roles when the contract request state is Work in progress or New \(except if the contract document statues is also New\):

    -   Assigned To
    -   Assignment Group Manager
    -   Collaborator

## Integration with e-signature providers

-   **Configure electronic signature provider spokes**

    The administrator can use the Integration Hub to install and configure the following electronic signature provider spokes for contract documents:

    -   [Adobe Acrobat Sign spoke](https://www.servicenow.com/docs/access?context=adobe-sign-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)
    -   [Docusign spoke](https://www.servicenow.com/docs/access?context=docusign-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)
-   **Set up the electronic signature provider app**

    The configurator can set up the electronic signature app integrations from **Contract Integrations**. For more information, see [Configure an e-signature provider](../task/cncore-integrate-esign.md).


-   **[Configure an external storage system](../task/cncore-integrate-ext-storage.md)**  
As a contract configurator, configure an external storage system to store signed contract documents.
-   **[Configure an e-signature provider](../task/cncore-integrate-esign.md)**  
Configure an electronic signature provider to enable users to sign contract documents electronically.

**Parent Topic:**[Set up Contracts Core](cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](../task/cncore-create-contract-type.md)

[Create document template categories](../task/cncore-create-doc-tmplt-cat.md)

[Enable users to view email details in activity stream](../task/cncore-enbl-user-email-astream.md)

[Activate a system property to generate a certificate of completion](../task/cncore-config-system-prop-COC.md)

[Configure reminders for expiring contracts](../task/cncore-config-rem-exp-cont.md)

[Configure extension point for notifications](../task/cmpro-configure-action-extension-point-email-notification-admin.md)

[Use default email notifications](../task/cmpro-send-receive-email-notification-admin.md)

[Auto-populate the start date and end date for contract requests](../task/cncore-conf-start-end-date-for-cntrcts.md)

