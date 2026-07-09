---
title: Source-to-Pay Integrations glossary
description: Learn about the terms and concepts used in Source-to-Pay \(S2P\) integrations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
---

# Source-to-Pay Integrations glossary

Learn about the terms and concepts used in Source-to-Pay \(S2P\) integrations.

Glossary terms are grouped alphabetically.

[A](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [D](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [E](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [I](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [M](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [P](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [R](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [S](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [T](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md) \| [W](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/source-to-pay-integrations-glossary.md)

## A

### Accounts Payable Operations \(APO\)

One of three Source-to-pay Integrations product areas; its staging tables hold invoice data before it moves to APO primary data tables or is exported to the ERP system for invoice generation.

### API \(Application Programming Interface\)

A set of rules that allows different software entities to communicate with each other.

### Asynchronous Integration

A type of integration where the systems involved communicate without waiting for an immediate response.

### Authentication profile

In Source-to-pay Integrations, an authentication configuration that stores an ERP integration username and password, associated with service maps, and used for web service integration with a third-party ERP system.

## B

### BAPI

An SAP function module or interface, such as ZSN\_BAPI\_PO\_CREATE, with a fixed set of attributes, used with RFC to communicate with SAP in Source-to-pay Integrations Hub Actions and RFC calls.

## C

### Catalog Management

The process of managing product and service information in a structured way.

### Cloud Contact Center

A cloud-based customer service solution that handles inbound and outbound communications.

### Connection alias

In Source-to-pay Integrations, a unique identifier for an ERP instance connection, holding its URL, username, and password, used to distinguish among multiple instances of the same ERP.

### contract management

The process of creating, managing, and executing legal sales contracts from completed quotes.

### Cost center

In Source-to-pay Integrations, a department or organizational segment managing its own budget to which purchase, invoice, or requisition costs are allocated; a primary data entity fetched from ERP systems via dedicated subflows.

## D

### Data Synchronization

The process of ensuring that data in two or more locations is updated consistently.

### Delta pull

In Source-to-pay Integrations, a configuration on an Integration Service record that fetches only incremental data \(new or changed records\) from the ERP system, as opposed to a full pull.

## E

### EDI \(Electronic Data Interchange\)

The electronic interchange of business information using a standardized format.

### ERP Integration Framework

The Source-to-pay Integrations plugin that provides the ERP Source Configuration page and subflows; a required dependency for Primary Data, Supplier Lifecycle, Sourcing/Procurement, and Accounts Payable Operations integrations.

### ERP source

A configured connection record in Source-to-pay Integrations representing a specific third-party ERP system instance; typically mapped to a legal entity and automatically identified from the legal entity on a transaction record. One default ERP source exists per supported ERP, with more creatable for additional instances.

### ERP User Mapping

In Source-to-pay Integrations, a table or related list mapping ERP user IDs to ServiceNow user IDs for active users who hold the procurement buyer role; used by the requisition assignment rule.

## F

### Flow / Subflow

In Source-to-pay Integrations, an automated process built in Workflow Studio or Flow Designer that can be manually triggered, copied, customized, and given a trigger condition; subflows are reusable building blocks that invoke Integration Hub Actions to connect to a third-party ERP via REST APIs.

### Full pull

In Source-to-pay Integrations, a job configuration option to pull the entire primary data set from the ERP system, as opposed to an incremental or delta pull.

## I

### IDoc

SAP's Intermediate Document mechanism or protocol for transferring business transaction data between SAP and other systems in Source-to-pay Integrations; some Integration Hub Actions and SAP ECC procurement transactions are based on it.

### Inbound integration error

In Source-to-pay Integrations, an error recorded when the inbound flow fails to fetch primary data from the target ERP source; the Error field in the inbound staging table is updated with the error message.

### Inbound staging table

In Source-to-pay Integrations, a table that temporarily stores data received from an external ERP system before it is transformed and sent to the primary data tables.

### Integration

A process by which the ServiceNow platform can be made to work with a third-party application or web service.

### Integration Hub Actions

Out-of-the-box actions, such as Create Purchase Order, Create Goods Receipt, and Create Invoice, that call underlying SAP BAPIs or connect to a third-party system via REST APIs, used as building blocks of a Source-to-pay Integrations flow or subflow.

### Integration Hub Spoke / Spoke

An installable Integration Hub component, with its associated actions, that lets customers communicate with an external system, such as SAP ECC, Coupa, or SAP Ariba, in Source-to-pay Integrations; automatically activated when the corresponding integration app is installed from the ServiceNow Store.

### Integration Service

In Source-to-pay Integrations, a record configured under ERP Source Configuration that defines how an entity's data is retrieved from the ERP system, including its subflow, properties, and active status; must be configured before jobs can look up primary data.

### Invoices

A document issued by a seller to a buyer, indicating the products, quantities, and agreed prices for products or services provided.

## L

### Legal entity

In Source-to-pay Integrations, an organizational entity, equivalent to a company code, that incurs the cost of or is responsible for a purchase order, invoice, or purchase requisition; used to determine the ERP source for a transaction.

## M

### MID Server

A ServiceNow server that must be installed and configured to connect to the ERP system server; required only for Source-to-pay Integrations ERP integrations that use SOAP services, not REST-based integrations.

### middleware

Software that acts as a bridge between different applications or services.

## O

### Outbound integration error

In Source-to-pay Integrations, an error recorded when an outbound staging record's target ERP source subflow fails; the Processing message field is updated, Integration status is set to error, and an error task is automatically created.

### Outbound staging table

In Source-to-pay Integrations, a table that stores data before it is exported to a third-party ERP system.

## P

### Primary data

Master and reference data \(legal entities, currencies, GL accounts, cost centers, FX rates, suppliers, purchase organizations, materials, and so on\) that Source-to-pay Integrations loads from, or synchronizes with, a third-party ERP system.

### Procurement

The process of finding, acquiring, and buying goods, services, or works from an external source.

### Purchase Requisition \(PR\)

In Source-to-pay Integrations, a formal request for goods or services that moves through approval and processing before becoming a purchase order; tracked using fields such as accounting period, assignment group, and requested delivery date.

## R

### Receipt

A document acknowledging that a specified amount of money, goods, or services has been received.

### Return

The process of sending back goods to the supplier due to various reasons such as defects or incorrect orders.

### RFC \(Remote Function Call\)

A protocol SAP supports for transferring data, typically used with BAPI to communicate with SAP systems in Source-to-pay Integrations; SAP JCo supports both inbound and outbound RFCs.

## S

### SAP ECC

An enterprise resource planning software developed by SAP SE, used for business process management.

### SAP S/4HANA

A next-generation enterprise resource planning suite from SAP, designed to run on the SAP HANA database.

### Source-to-Pay \(S2P\)

A process that encompasses all activities from sourcing goods and services to paying suppliers.

### Service Map

In Source-to-pay Integrations, a record or related list on an ERP source configuration that maps a service to an ERP source, defining SOAP or REST connection details, field mappings, and the linked authentication profile.

### Source-to-Pay Integration Framework

The Source-to-pay Integrations plugin that pulls tasks from a connected ERP system \(Oracle Financial Cloud, Oracle EBS, Coupa, or SAP Ariba\) into ServiceNow, providing an abstraction layer between Source-to-Pay and backend systems.

### Sourcing and Procurement Operations \(SPO\)

One of three Source-to-pay Integrations product areas; shares the error task table with the other two, has its own inbound and outbound staging tables, and is the source entity whose attributes transfer to SAP for purchase order and receipt generation.

### Staging table

In Source-to-pay Integrations, a general inbound or outbound table that temporarily stores data before it is processed into primary data tables or sent to or from the target ERP system.

### Supplier Lifecycle Management

The end-to-end process of managing a supplier's performance and relationship with the organization.

### Supplier Lifecycle Operations \(SLO\)

One of three Source-to-pay Integrations product areas; shares the error task table with the other two, has its own inbound and outbound staging tables, and is the source entity whose attributes transfer to SAP when creating a supplier.

### Supplier Portal

An online platform where suppliers can interact with the buying organization.

### synchronous integration

A type of integration where the systems involved communicate in real-time.

## T

### third-party application

An external software system that can be integrated with ServiceNow to extend its capabilities.

### Transform map

In Source-to-pay Integrations, a configuration that defines data relationships and mapping between a source staging table and a target table, used to move ERP data pulled into staging tables into primary or target tables.

### Transport Request

An SAP package of changes, containing COFILE and DATA files, added to the Import Queue and copied into the target client as part of setting up SAP for Source-to-pay Integrations.

### 3CLogic

A ServiceNow partner that provides native voice and SMS capabilities to complement ServiceNow’s digital channels.

## W

### workflow

Defined sequence of steps automating processes in Sales Customer Relationship Management.

