---
title: ERP Integration Framework
description: The Source-to-Pay \(S2P\) ERP Integration Framework enables seamless data exchange between ServiceNow and third-party Enterprise Resource Planning \(ERP\) systems. This framework supports comprehensive integration of primary data, transactional data \(purchase orders, receipts, invoices\), fixed assets, and tax information across multiple ERP instances.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# ERP Integration Framework

The Source-to-Pay \(S2P\) ERP Integration Framework enables seamless data exchange between ServiceNow and third-party Enterprise Resource Planning \(ERP\) systems. This framework supports comprehensive integration of primary data, transactional data \(purchase orders, receipts, invoices\), fixed assets, and tax information across multiple ERP instances.

## Key Features

-   User-defined primary data that can be customized to organizational needs.
-   Mapped to organizational legal entities for clear data governance.
-   Associated with target ERP systems for bidirectional data flow.
-   Flexible configuration enabling multiple sources for an organization.

## ERP Sources

An ERP Source represents a specific ERP instance from which data is imported and to which data is exported. Organizations typically maintain multiple ERP instances as systems of record, with each ERP source mapped to a legal entity within the organization.

## ERP Integration Requirements

-   At least one ERP source must be configured for each legal entity within every target instance.
-   Each ERP source should be associated with a specific target ERP system.
-   Organizations can create as many ERP sources as needed to support their structure.

The integration framework clearly defines the system of record responsibilities:

-   Third-party ERP: System of record for primary data entities
-   Source-to-Pay: System of record for purchase orders and receipts
-   Either system: Invoices can be created manually in Source-to-Pay or through external supplier portals

## Integration Architecture

The ERP Integration Framework application loads primary data into Source-to-Pay Operations, enabling various ServiceNow workflows. It also imports selected inbound transactional data objects such as purchase order data that are shared across all Source-to-Pay Operations products.

Both the ERP Integration Framework and Source-to-Pay Integration Framework applications provide an abstraction layer between the Source-to-Pay application and backend systems. This design shields Source-to-Pay workflows and data models from backend-specific integration components and data structures.

![Source-to-Pay Operations Integration Architecture](../image/s2p-data-architecture.png "Source-to-Pay Operations Integration Architecture")

**Required Applications**

The integration requires the Finance – ERP Integration store application to be installed.

## MID Server Requirement

A MID Server is required for ERP integrations using SOAP services. The MID Server must be installed and configured to connect to the ERP system server. See Installing the MID Server for details.

**Note:** MID Server integration is only required for SOAP-based integrations, not for REST-based integrations.

## User Roles and Permissions

The ERP Integration Framework supports the following roles and permissions:

<table id="table_d5y_ylk_4hc"><thead><tr><th>

Role name

</th><th>

Capabilities

</th></tr></thead><tbody><tr><td>

Administrator \(sn\_fcms\_intg.admin\)

</td><td>

-   Install integration applications
-   Configure system-wide settings
-   Manage all aspects of the integration infrastructure

</td></tr><tr><td>

Procurement Specialist \(sn\_shop.procurement\_specialist\)

</td><td>

-   Define and manage ERP sources
-   Configure ERP source parameters
-   Manage integration workflows

</td></tr><tr><td>

FCA Integration user \(sn\_fcms\_intg.integration\_user\)

</td><td>

-   Configure ERP source settings including web service authorization
-   Set up web services for Park and Post, Reverse operations
-   Manage user and role mappings
-   Access inbound and outbound staging tables
-   Configure and execute integration processes

</td></tr></tbody>
</table>**Additional roles for the FCA Integration user \(sn\_fcms\_intg.integration\_user\)**:

-   Import\_transformer: For data transformation operations
-   SOAP: For SOAP-based web service integrations

**Granular roles**

Users assigned the integration admin role \(`sn_fcms_intg.admin`\) are granted read and write permissions for these system properties. This access aligns with the granular role modifications as per the new directives.

|Property Name|Read role|Write role|
|-------------|---------|----------|
|sn\_fcms\_intg.status\_for\_purchase\_order|sn\_shop.shopper, sn\_shop.procurement\_common\_reader, sn\_fcms\_intg.admin|sn\_fcms\_intg.admin|
|sn\_fcms\_intg.status\_for\_invoice\_creation|sn\_fcms\_intg.admin, sn\_ap\_apm.accounts\_payable\_specialist|sn\_fcms\_intg.admin|
|sn\_fcms\_intg.status\_for\_goods\_receipt|sn\_shop.shopper, sn\_shop.procurement\_common\_reader, sn\_fcms\_intg.admin|sn\_fcms\_intg.admin|

