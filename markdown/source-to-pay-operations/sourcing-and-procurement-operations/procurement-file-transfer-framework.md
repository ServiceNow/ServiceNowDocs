---
title: Procurement File Transfer Framework
description: Procurement File Transfer Framework \(PFTF\) helps you transfer information between the ServiceNow database and a third-party reseller through a File Transfer Protocol \(FTP\). You can set up an FTP server for access and transfer of reseller data without any spoke development by the third-party reseller.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/procurement-file-transfer-framework.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
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

Your suppliers can upload the files with the recommended [folder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/data-sources-info.md) structure and format on the server. ServiceNow imports and exports all the details automatically through scheduled data imports and exports.

-   **[Third‑party registration for PIF and PFTF integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/third-party-registration-for-pif-pftf.md)**  
Third‑party registration enables you to configure supplier integrations for Source-to-Pay Integration Framework \(PIF\) and Procurement File Transfer Framework \(PFTF\).
-   **[Import data using FTP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/ftp-data-import.md)**  
Import a file from a local source, a remote network server, or another instance by providing a path and authentication information. Transfer and manage procurement data in a principled structure that administrators can use for various data management operations.
-   **[Perform export steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/validate-errors.md)**  
Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.
-   **[Data source table information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/data-sources-info.md)**  
The following information can help you with the FTP import and export data.

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with IT Asset Management]()

[Sourcing and Procurement Operations integration with Employee Center]()

[Sourcing and Procurement Operations integration with third-party sourcing solutions]()

[Sourcing and Procurement Operations integration with Third-party Risk Management]()

[Sourcing and Procurement Operations integration with Project Management]()

[Sourcing and Procurement Operations integration with Celonis]()

[Sourcing and Procurement Operations integration with Field Service Management]()

[Source-to-Pay Operations integration with Contract Management Pro]()

[ERP source validation on Sourcing and Procurement Operations objects]()

[SpendInt APIs]()

