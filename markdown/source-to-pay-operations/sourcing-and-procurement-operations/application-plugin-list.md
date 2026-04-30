---
title: Application plugin installation sequence
description: The following table provides the consolidated list of plugins for Sourcing and Procurement Operations, a high-level description of each plugin, and the dependencies that are required before installing each plugin.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Sourcing and Procurement Operations reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Application plugin installation sequence

The following table provides the consolidated list of plugins for Sourcing and Procurement Operations, a high-level description of each plugin, and the dependencies that are required before installing each plugin.

<table id="table_mqm_3sr_hrb"><thead><tr><th>

Plugin name

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Finance Common Architecture\[com.sn\_fin\]

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

</td><td>

Finance Applications – Common Dependencies

 Fiscal Calendar

 Scoped Application Restricted Caller Access

 Insert Multiple Web Service

</td></tr><tr><td>

ERP Integration Framework\[com.sn\_fcms\_intg\]

</td><td>

Provides integration support between the Platform and common ERP systems.

</td><td>

Scope Application Restricted Caller Access

 Insert Multiple Web Service

</td></tr><tr><td>

Common Service Delivery\[com.sn\_spend\_sdc\]

</td><td>

Contains Service Task and Service Request tables, as well as other infrastructure that forms the basis of Finance and Supply Chain workflows products.

</td><td>

Process Automation Designer Core

 Process Automation Designer for App Engine

 Playbook Experience

</td></tr><tr><td>

Procurement Case Management\[com.sn\_spend\_psd\]

</td><td>

Enables all employees to request services from the procurement team, and the procurement team to manage those requests.

</td><td>

Common Service Delivery

 Source-to-Pay Workspace

</td></tr><tr><td>

Source-to-Pay Workspace\[com.sn\_spend\_workspace\]

</td><td>

Provides a single environment for Procurement Specialists to work on purchase requisitions, sourcing requests, negotiations, procurement requests, and more.

</td><td>

None

</td></tr><tr><td>

Source-to-Pay Common Architecture\[com.snc.sn\_shop\]

</td><td>

Provides an architecture to store purchase orders, requisitions, sourcing requests, and other objects that are commonly used across the source-to-pay business processes.

</td><td>

Procurement Case Management

 Common Service Delivery

 GraphQL Plugin

 Finance Common Architecture

 User Criteria Scoped API

 Source-to-Pay Workspace

 Employee Center

</td></tr><tr><td>

Sourcing and Purchasing Automation\[com.snc.sn\_pr\]

</td><td>

Provides workflows and automation for sourcing requests, negotiations, and purchase requisitions.

</td><td>

Source-to-Pay Common Architecture

 Supplier Common Architecture

</td></tr><tr><td>

Shopping Hub\[com.snc.sn\_spend\_uib\]

</td><td>

Provides a streamlined, e-commerce like experience for employees to self-service requests, and source or purchase products and services through the procurement organization. This is an add-on experience to Employee Center.

</td><td>

Sourcing and Purchasing Automation

 Common UIB Wrapper Components

</td></tr><tr><td>

Shopping Hub Mobile\[com.sn\_shop\_mobile\]

</td><td>

Enables Shopping Hub and other employee experiences for procurement within the Now Mobile application.

</td><td>

Sourcing and Purchasing Automation

 Mobile Plugin

 Mobile Agent Native Client

</td></tr><tr><td>

Playbooks for Sourcing and Procurement Operations\[com.sn\_spend\_cp\]

</td><td>

Provides a set of prebuilt playbooks, workflows, and experiences for employees, sourcing, and procurement to automate work that is typically managed through emails and spreadsheets.

</td><td>

Source-to-Pay Common Architecture

 Sourcing and Purchasing Automation

</td></tr><tr><td>

Virtual Agent for Sourcing and Procurement Operations\[com.sn\_shop\_va\]

</td><td>

Provides preconfigured topics for sourcing and procurement within a conversational interface, for employees to raise requests, find knowledge, and complete tasks.

</td><td>

Source-to-Pay Common Architecture

 Glide Virtual Agent

</td></tr><tr><td>

Natural Language Understanding Models for Sourcing and Procurement Operations\[com.sn\_spend\_nlu\]

</td><td>

Provides Natural Language Understanding \(NLU\) models to enhance the virtual agent conversation interface, using natural human utterances to detect the correct conversations intended by employees.

</td><td>

Source-to-Pay Common Architecture

 Glide Virtual Agent

 Virtual Agent for Sourcing and Procurement Operations

</td></tr><tr><td>

Source-to-Pay Integration Framework\[com.sn\_spend\_intg\]

</td><td>

Provides a set of staging tables, transform maps, and workflows to integrate sourcing, third-party catalogs, ordering, shipments, and invoicing with Sourcing and Procurement Operations.

</td><td>

Source-to-Pay Common Architecture

</td></tr><tr><td>

Procurement File Transfer Framework\[com.sn\_spend\_ftp\_intg\]

</td><td>

Extends the Source-to-Pay Integration Framework with Secure File Transfer Protocol \(SFTP\) and File Transfer Protocol \(FTP\) functionality, designed for integrating with systems that don’t support Representational State Transfer \(REST\) or Simple Object Access Protocol \(SOAP\) based integration methods.

</td><td>

Source-to-Pay Integration Framework

 ServiceNow IntegrationHub Action Step – SSH

 ServiceNow IntegrationHub Action Step - SFTP

 ServiceNow IntegrationHub Flow Trigger - REST

</td></tr><tr><td>

Performance Analytics for Sourcing and Procurement Operations\[com.sn\_spend\_pa\]

</td><td>

Provides a set of preconfigured metrics and dashboards to assess spend, operational efficiency, and team performance across the Sourcing and Procurement Operations product.

</td><td>

Source-to-Pay Common Architecture

 Sourcing and Purchasing Automation

</td></tr><tr><td>

Risk Assessments Integration for Sourcing and Procurement Operations\[com.sn\_spend\_vrm\]

</td><td>

Provides a set of capabilities to trigger risk assessments on a supplier during the sourcing or purchase requisition workflow using Third-party Risk Management.

</td><td>

Source-to-Pay Common Architecture

 Vendor Risk Management

</td></tr><tr><td>

Project Costing for Sourcing and Procurement Operations\[com.sn\_spend\_ppm\]

</td><td>

Provides a set of capabilities to automate the calculation of planned versus actual cost by linking purchase orders to cost plans within Project Portfolio Management.

</td><td>

Source-to-Pay Common Architecture

 Project Portfolio Suite with Financials

</td></tr><tr><td>

Source-to-Pay Operations with Contract Management Pro\[com.snc.sn\_spend\_clm\]

</td><td>

Provides streamlined cross-team collaboration and enables legal professionals to run their contracting work within the sourcing and purchasing process.​ With this integration, procurement specialists can initiate contract requests manually throughout the sourcing and purchasing process.

</td><td>

com.snc.sn\_pr

 com.sn\_cm\_word\_addin

</td></tr><tr><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)\[com.sn\_spend\_gen\_ai\]

</td><td>

Uses procurement-related topics to route requesters to the appropriate intake channels, and then through conversation, helps to submit their requests.

</td><td>

Now Assist for Platform

 Sourcing and Purchasing Automation

</td></tr><tr><td>

Process Mining for Source-to-Pay Operations\[com.sn\_s2p\_mining\]

</td><td>

Provides the ability to use Platform's Process Mining capabilities on the Source-to-Pay workflows to which customers are entitled to analyze and improve source-to-pay processes.

</td><td>

Source-to-Pay Common Architecture

</td></tr><tr><td>

Advanced Work Assignment for Source-to-Pay Operations\[com.snc.sn\_spend\_awa\]

</td><td>

Provides configurations to support automatic routing, queuing, and assignment of procurement cases, emails, and live agent chat conversations.

</td><td>

Procurement Case Management

 Advanced Work Assignment

 Agent Chat

</td></tr><tr><td>

Primary Data Integration with SAP\[com.sn\_sap\_data\_int\]

</td><td>

Provides the ability to fetch entity data like legal entity, cost center, material, supplier, and so on, from SAP ECC and SAP HANA into ServiceNow.

</td><td>

com.glide.hub.integrations.enterprise

 com.sn\_fcms\_intg

 com.sn\_sap\_ecc\_idoc\_sp

 com.sn\_sap\_s4\_hana\_rfc

 com.sn\_shop

 com.sn\_utility\_spoke

</td></tr><tr><td>

Sourcing and Procurement Operations Integration with SAP\[com.sn\_psm\_sap\_int\]

</td><td>

Provides the ability to send purchase orders, receipts, and returns created in Sourcing and Procurement Operations to SAP ECC and SAP S4 HANA.

</td><td>

com.sn\_fcms\_intg

 com.sn\_shop

 com.sn\_sap\_ecc\_idoc\_sp

 com.sn\_sap\_s4\_hana\_rfc

 com.sn\_sap\_data\_int

</td></tr></tbody>
</table>## Installation sequence

It is recommended that you install the plugins in the following sequence to avoid incomplete demo data and other installation issues:

1.  Finance Common Architecture \[com.sn\_fin\]
2.  ERP Integration Framework \[com.sn\_fcms\_intg\]
3.  Common Service Delivery \[com.sn\_spend\_sdc\]
4.  Procurement Case Management \[com.sn\_spend\_psd\]

    **Note:** You must use the November 2023 version of the Document Template plugin \[sn\_doc\] for using the November 2023 versions of the Procurement Case Management and Playbooks for Sourcing and Procurement Operations plugins.

5.  Source-to-Pay Workspace \[com.sn\_spend\_workspace\]
6.  Source-to-Pay Common Architecture \[com.snc.sn\_shop\]
7.  Sourcing and Purchasing Automation \[com.snc.sn\_pr\]

    **Note:** If you want to leverage the demo data, you must repair the Sourcing and Purchasing Automation plugin. You can repair it now or after you have completed installing all the plugins.

8.  Shopping Hub \[com.snc.sn\_spend\_uib\]
9.  Shopping Hub Mobile \[com.sn\_shop\_mobile\]
10. Playbooks for Sourcing and Procurement Operations \[com.sn\_spend\_cp\]
11. Virtual Agent for Sourcing and Procurement Operations \[com.sn\_shop\_va\]
12. Natural Language Understanding Models for Sourcing and Procurement Operations \[com.sn\_spend\_nlu\]
13. Source-to-Pay Integration Framework \[com.sn\_spend\_intg\]
14. Procurement File Transfer Framework \[com.sn\_spend\_ftp\_intg\]
15. Performance Analytics for Sourcing and Procurement Operations \[com.sn\_spend\_pa\]
16. Risk Assessments Integration for Sourcing and Procurement Operations \[com.sn\_spend\_vrm\]
17. Project Costing for Sourcing and Procurement Operations \[com.sn\_spend\_ppm\]
18. Source-to-Pay Operations with Contract Management Pro \[com.snc.sn\_spend\_clm\]
19. Now Assist for Sourcing and Procurement Operations \(SPO\) \[com.sn\_spend\_gen\_ai\]
20. Advanced Work Assignment for Source-to-Pay Operations \[com.snc.sn\_spend\_awa\]
21. Process Mining for Source-to-Pay Operations \[com.sn\_s2p\_mining\]
22. Primary Data Integration with SAP \[com.sn\_sap\_data\_int\]
23. Sourcing and Procurement Operations Integration with SAP \[com.sn\_psm\_sap\_int\]
24. Procurement for Field Service Management

    **Note:** This application is owned by the Field Service Management team.


**Parent Topic:**[Sourcing and Procurement Operations reference](spo-reference.md)

**Related topics**  


[Components installed with Sourcing and Procurement Operations](installed-with-FSC.md)

[Components installed with ERP Integration Framework for Sourcing and Procurement Operations](installed-with-FSC-ERP.md)

[Components installed with Finance Common Architecture](installed-with-finance-common.md)

[Properties installed with Finance Common Architecture](properties-for-finance-common.md)

[Domain separation and Sourcing and Procurement Operations](../concept/psm-domain-separation.md)

[Sourcing and Procurement Operations glossary](../concept/spo-glossary.md#)

[Install Sourcing and Procurement Operations](../task/activate-finance-spend-central.md)

[Components installed with Sourcing and Procurement Operations](installed-with-FSC.md)

[Components installed with ERP Integration Framework for Sourcing and Procurement Operations](installed-with-FSC-ERP.md)

[Components installed with Finance Common Architecture](installed-with-finance-common.md)

[Properties installed with Finance Common Architecture](properties-for-finance-common.md)

