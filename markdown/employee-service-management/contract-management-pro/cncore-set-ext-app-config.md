---
title: External applications for Contract Management Pro
description: External applications provide services such as electronically signing contract documents and saving signed contracts or the documents related to requests in an external storage system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-set-ext-app-config.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# External applications for Contract Management Pro

External applications provide services such as electronically signing contract documents and saving signed contracts or the documents related to requests in an external storage system.

The Contract Management Pro application use spokes from Integration Hub to integrate with external applications. The contract configurator \(sn\_cm\_core.contract\_config\) can complete configuring these external apps after the administrator completes installation and configuration of these spokes.

## Integration with external storage systems

-   **Configure external storage provider spokes**

    The administrator can use the Integration Hub to install and configure the following external storage provider spokes for saving documents attached to contract requests and signed contract documents:

    -   [Google Drive spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/googledrive-spoke.md)

        **Note:** Word \(.docx\) files edited directly from Google Drive using Google Docs may become incompatible with Contract Management Pro causing failures during processing, signature operations, and document updates. To avoid these issues, download the .docx file from the Google Drive, edit it in Microsoft Word \(desktop or online\), and upload it into the system using the Create Revision option.

    -   [Microsoft OneDrive spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/onedrive-spoke.md)
-   **Configure an external storage provider**

    The contract configurator can set up the external storage app integrations from **Contract Integrations**. For more information, see [Configure an external storage system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-integrate-ext-storage.md).

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

    -   [Adobe Acrobat Sign spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/adobe-sign-spoke.md)
    -   [Docusign spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/docusign-spoke.md)
-   **Set up the electronic signature provider app**

    The configurator can set up the electronic signature app integrations from **Contract Integrations**. For more information, see [Configure an e-signature provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-integrate-esign.md).


-   **[Configure an external storage system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-integrate-ext-storage.md)**  
As a contract configurator, configure an external storage system to store signed contract documents.
-   **[Configure an e-signature provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-integrate-esign.md)**  
Configure an electronic signature provider to enable users to sign contract documents electronically.

**Parent Topic:**[Configuring Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-config-cmpro.md)

