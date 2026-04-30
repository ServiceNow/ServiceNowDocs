---
title: Procurement File Transfer Framework
description: Procurement File Transfer Framework \(PFTF\) helps you transfer information between the ServiceNow database and a third-party reseller through a File Transfer Protocol \(FTP\). You can set up an FTP server for access and transfer of reseller data without any spoke development by the third-party reseller.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Procurement File Transfer Framework

Procurement File Transfer Framework \(PFTF\) helps you transfer information between the ServiceNow database and a third-party reseller through a File Transfer Protocol \(FTP\). You can set up an FTP server for access and transfer of reseller data without any spoke development by the third-party reseller.

When the PFTF application is installed, the following applications from the ServiceNow IntegrationHub Professional Pack Installer must be auto-installed. This is a prerequisite.

-   ServiceNow IntegrationHub Action Step - SSH
-   ServiceNow IntegrationHub Action Step - SFTP
-   ServiceNow IntegrationHub Flow Trigger - REST

FTP integration helps when you intend to transfer files between ServiceNow and your resellers.

Use Procurement File Transfer Framework for the following activities:

-   Support the FTP-based integration for suppliers.
-   Standardize the file structure, formats, and naming conventions for each supplier.
-   Manage large-scale data through FTP import and export.
-   Simplify the import and export operations with mid server and flow designer.
-   Use the file transfer workflows to control the data operations.

Currently, the following integrations are supported:

**Imports**:

-   Catalog import
-   Order acknowledgment import
-   Shipment import
-   Invoice import

**Exports**: Order export

Your suppliers can upload the files with the recommended [folder](../reference/data-sources-info.md) structure and format on the server. ServiceNow imports and exports all the details automatically through scheduled data imports and exports.

-   **[Import data using FTP server](../task/ftp-data-import.md)**  
Import a file from a local source, a remote network server, or another instance by providing a path and authentication information. Transfer and manage procurement data in a principled structure that administrators can use for various data management operations.
-   **[Perform export steps](../task/validate-errors.md)**  
Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.
-   **[Data source table information](../reference/data-sources-info.md)**  
The following information can help you with the FTP import and export data.

**Parent Topic:**[Integrating Sourcing and Procurement Operations with other applications](integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../reference/erp-source-val-spo-objects.md)

[Spendint API](../../../integrate/inbound-rest/concept/spendint-api.md)

