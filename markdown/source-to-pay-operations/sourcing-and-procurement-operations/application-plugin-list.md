---
title: Application plugin installation sequence in Sourcing and Procurement Operations
description: The following table lists the Sourcing and Procurement Operations \(SPO\) plugins, their installation sequence, high-level descriptions, and dependencies.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Install Sourcing and Procurement Operations, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Application plugin installation sequence in Sourcing and Procurement Operations

The following table lists the Sourcing and Procurement Operations \(SPO\) plugins, their installation sequence, high-level descriptions, and dependencies.

**Important:** Before installing a plugin listed in the Plugin name column, ensure that you install all corresponding dependencies listed in the Plugin dependencies column from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

<table id="table_mqm_3sr_hrb"><thead><tr><th>

Sequence

</th><th>

Plugin name

</th><th>

Description

</th><th>

Plugin dependencies

</th></tr></thead><tbody><tr><td>

1

</td><td>

Finance Common Architecture\[sn\_fin\]

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

</td><td>

-   Finance Applications – Common Dependencies
-   Fiscal Calendar
-   Scoped Application Restricted Caller Access
-   Scoped Application Restricted Caller Access
-   Insert Multiple web service
-   Document Templates

</td></tr><tr><td>

2

</td><td>

ERP Integration Framework\[sn\_fcms\_intg\]

</td><td>

Provides integration support between the Platform and common ERP systems.

</td><td>

-   Scope Application Restricted Caller Access
-   Insert Multiple Web Service

</td></tr><tr><td>

3

</td><td>

Common Service Delivery\[sn\_spend\_sdc\]

</td><td>

Contains Finance Case, Finance Case Line, Finance Task, and Playbook status tables, as well as other infrastructure that forms the basis of Finance and Supply Chain workflows products.

</td><td>

-   Process Automation Designer Core
-   Process Automation Designer for App Engine
-   Playbook Experience

</td></tr><tr><td>

4

</td><td>

Procurement Case Management\[sn\_spend\_psd\]

</td><td>

Enables all employees to request services from the procurement team, and the procurement team to manage those requests.

</td><td>

-   Common Service Delivery
-   Source-to-Pay Workspace

</td></tr><tr><td>

5

</td><td>

Source-to-Pay Workspace\[sn\_spend\_workspace\]

</td><td>

Provides a single environment for Procurement Specialists to work on purchase requisitions, sourcing requests, negotiations, procurement requests, and more.

</td><td>

None

</td></tr><tr><td>

6

</td><td>

Source-to-Pay Common Architecture\[sn\_shop\]

</td><td>

Provides an architecture to store purchase orders, requisitions, sourcing requests, and other objects that are commonly used across the source-to-pay business processes.

</td><td>

-   Procurement Case Management
-   Common Service Delivery
-   GraphQL Plugin
-   Finance Common Architecture
-   User Criteria Scoped API
-   Source-to-Pay Workspace
-   Employee Center

</td></tr><tr><td>

7

</td><td>

Sourcing and Purchasing Automation\[sn\_pr\]

</td><td>

Provides workflows and automation for sourcing requests, negotiations, and purchase requisitions.**Note:** If you want to leverage the demo data, you must repair the Sourcing and Purchasing Automation plugin. You can repair it now or after you have completed installing all the plugins.

</td><td>

-   Source-to-Pay Common Architecture
-   Supplier Common Architecture

</td></tr><tr><td>

8

</td><td>

Shopping Hub\[sn\_spend\_uib\]

</td><td>

Provides a streamlined, e-commerce like experience for employees to self-service requests, and source or purchase products and services through the procurement organization. This is an add-on experience to Employee Center.

</td><td>

-   Sourcing and Purchasing Automation
-   Common UIB Wrapper Components


</td></tr><tr><td>

9

</td><td>

Shopping Hub Mobile\[sn\_shop\_mobile\]

</td><td>

Enables Shopping Hub and other employee experiences for procurement within the Now Mobile application.

</td><td>

-   Sourcing and Purchasing Automation
-   Mobile Plugin
-   Mobile Agent Native Client

</td></tr><tr><td>

10

</td><td>

Playbooks for Sourcing and Procurement Operations\[sn\_spend\_cp\]

</td><td>

Provides a set of prebuilt playbooks, workflows, and experiences for employees, sourcing, and procurement to automate work that is typically managed through emails and spreadsheets.

</td><td>

-   Source-to-Pay Common Architecture
-   Sourcing and Purchasing Automation

</td></tr><tr><td>

11

</td><td>

Virtual Agent for Sourcing and Procurement Operations\[sn\_shop\_va\]

</td><td>

Provides preconfigured topics for sourcing and procurement within a conversational interface, for employees to raise requests, find knowledge, and complete tasks.

</td><td>

-   Source-to-Pay Common Architecture
-   Glide Virtual Agent

</td></tr><tr><td>

12

</td><td>

Natural Language Understanding Models for Sourcing and Procurement Operations\[sn\_spend\_nlu\]

</td><td>

Provides Natural Language Understanding \(NLU\) models to enhance the virtual agent conversation interface, using natural human utterances to detect the correct conversations intended by employees.

</td><td>

-   Source-to-Pay Common Architecture
-   Glide Virtual Agent
-   Virtual Agent for Sourcing and Procurement Operations

</td></tr><tr><td>

13

</td><td>

Source-to-Pay Integration Framework\[sn\_spend\_intg\]

</td><td>

Provides a set of staging tables, transform maps, and workflows to integrate sourcing, third-party catalogs, ordering, shipments, and invoicing with Sourcing and Procurement Operations.

</td><td>

Source-to-Pay Common Architecture

</td></tr><tr><td>

14

</td><td>

Procurement File Transfer Framework\[sn\_spend\_ftp\_intg\]

</td><td>

Extends the Source-to-Pay Integration Framework with Secure File Transfer Protocol \(SFTP\) and File Transfer Protocol \(FTP\) functionality, designed for integrating with systems that don’t support Representational State Transfer \(REST\) or Simple Object Access Protocol \(SOAP\) based integration methods.

</td><td>

-   Source-to-Pay Integration Framework
-   ServiceNow IntegrationHub Action Step – SSH
-   ServiceNow IntegrationHub Action Step - SFTP
-   ServiceNow IntegrationHub Flow Trigger - REST

</td></tr><tr><td>

15

</td><td>

Performance Analytics for Sourcing and Procurement Operations\[sn\_spend\_pa\]

</td><td>

Provides a set of preconfigured metrics and dashboards to assess spend, operational efficiency, and team performance across the Sourcing and Procurement Operations product.

</td><td>

-   Source-to-Pay Common Architecture
-   Sourcing and Purchasing Automation

</td></tr><tr><td>

16

</td><td>

Risk Assessments Integration for Sourcing and Procurement Operations\[sn\_spend\_vrm\]

</td><td>

Provides a set of capabilities to trigger risk assessments on a supplier during the sourcing or purchase requisition workflow using Third-party Risk Management.

</td><td>

-   Source-to-Pay Common Architecture
-   Vendor Risk Management

</td></tr><tr><td>

17

</td><td>

Project Costing for Sourcing and Procurement Operations\[sn\_spend\_ppm\]

</td><td>

Provides a set of capabilities to automate the calculation of planned versus actual cost by linking purchase orders to cost plans within Project Portfolio Management.

</td><td>

-   Source-to-Pay Common Architecture
-   Project Portfolio Suite with Financials

</td></tr><tr><td>

18

</td><td>

Source-to-Pay Operations with Contract Management Pro\[sn\_spend\_clm\]

</td><td>

Provides streamlined cross-team collaboration and enables legal professionals to run their contracting work within the sourcing and purchasing process.​ With this integration, procurement specialists can initiate contract requests manually throughout the sourcing and purchasing process.

</td><td>

-   Sourcing and Purchasing Automation
-   ServiceNow Contracts

</td></tr><tr><td>

19

</td><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)\[sn\_spend\_gen\_ai\]

</td><td>

Uses procurement-related topics to route requesters to the appropriate intake channels, and then through conversation, helps to submit their requests.

</td><td>

-   Now Assist for Platform
-   Sourcing and Purchasing Automation

</td></tr><tr><td>

20

</td><td>

Advanced Work Assignment for Source-to-Pay Operations\[sn\_spend\_awa\]

</td><td>

Provides configurations to support automatic routing, queuing, and assignment of procurement cases, emails, and live agent chat conversations.

</td><td>

-   Procurement Case Management
-   Advanced Work Assignment
-   Agent Chat

</td></tr><tr><td>

21

</td><td>

Process Mining for Source-to-Pay Operations\[sn\_s2p\_mining\]

</td><td>

Provides the ability to use Platform's Process Mining capabilities on the Source-to-Pay workflows to which customers are entitled to analyze and improve source-to-pay processes.

</td><td>

Source-to-Pay Common Architecture

</td></tr><tr><td>

22

</td><td>

Primary Data Integration with SAP\[sn\_sap\_data\_int\]

</td><td>

Provides the ability to fetch entity data like legal entity, cost center, material, supplier, and so on, from SAP ECC and SAP HANA into ServiceNow.

</td><td>

-   ServiceNow IntegrationHub Enterprise Pack Installer
-   ERP Integration Framework
-   SAP ECC IDoc Spoke
-   SAP S4 HANA RFC Spoke
-   Source-to-Pay Common Architecture
-   Utility Actions Spoke
-   SAP S4 HANA OData Spoke
-   SAP S4 HANA Cloud Spoke

</td></tr><tr><td>

23

</td><td>

Sourcing and Procurement Operations Integration with SAP\[sn\_psm\_sap\_int\]

</td><td>

Provides the ability to send purchase orders, receipts, and returns created in Sourcing and Procurement Operations to SAP ECC and SAP S4 HANA.

</td><td>

-   ERP Integration Framework
-   Source-to-Pay Common Architecture
-   SAP ECC IDoc Spoke
-   SAP S4 HANA RFC Spoke
-   Primary Data Integration with SAP

</td></tr><tr><td>

24

</td><td>

Procurement for Field Service Managementsn\_fsm\_psm\_mobile

</td><td>

Provides an integration with the Field Service Management application. With this integration, a field service agent can engage with procurement and place an order to purchase a required part from a vendor or supplier.**Note:** This application is owned by the Field Service Management team.

</td><td>

-   Field Service Management
-   Field Service Mobile
-   Shopping Hub Mobile

</td></tr></tbody>
</table>**Parent Topic:**[Install Sourcing and Procurement Operations](../task/activate-finance-spend-central.md)

**Related topics**  


[Install Sourcing and Procurement Operations](../task/activate-finance-spend-central.md)

[Components installed with Sourcing and Procurement Operations](installed-with-FSC.md)

[Components installed with ERP Integration Framework](installed-with-FSC-ERP.md)

[Components installed with Finance Common Architecture](installed-with-finance-common.md)

[Properties installed with Finance Common Architecture](properties-for-finance-common.md)

