---
title: CSDM shapes support in the Enterprise Modeling and Visualization
description: ServiceNow CSDM data model defines standardized relationships between service-related objects in the CMDB. It ensures consistency across ITSM, ITOM, and EA practices. In Enterprise Architecture Workspace, CSDM shapes represent these objects visually in diagrams, enabling architects to model business capabilities, applications, services, and technical components in alignment with the Now Platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Enterprise Modeling and Visualization in the EA Workspace, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# CSDM shapes support in the Enterprise Modeling and Visualization

ServiceNow CSDM data model defines standardized relationships between service-related objects in the CMDB. It ensures consistency across ITSM, ITOM, and EA practices. In Enterprise Architecture Workspace, CSDM shapes represent these objects visually in diagrams, enabling architects to model business capabilities, applications, services, and technical components in alignment with the Now Platform.

## CSDM domains and shapes

CSDM 5 introduces seven domains, each grouping related entities. Shapes in Enterprise Architecture Workspace diagrams correspond to these domains:

-   Foundation- Shapes in this domain represent core referential data like Company, Location, Groups, Products, and Contracts.
-   Ideation &amp; Strategy- Shapes in this domain capture early-stage planning and strategic objectives.
-   Design &amp; Planning- Shapes in this domain define an architecture blueprint and logical application portfolio.
-   Build &amp; Integration- Shapes in this domain represent development artifacts and integration points.
-   Service Delivery- Shapes in this domain represent an operational view of technology services and offerings.
-   Service Consumption- Shapes in this domain represent services consumed by end users.

|Shape|Domain|Purpose|Example|
|-----|------|-------|-------|
|Value Stream|Foundation|Represents a sequence of activities delivering business value|Customer Onboarding Value Stream|
|Value Stream Stage|Foundation|Defines phases within a value stream for process improvement|Payment Processing Stage|
|Business Process|Design &amp; Planning|Models operational workflows supporting business capabilities|Order-to-Cash Process|
|Contract Model|Foundation|Standardizes contractual agreements and compliance tracking|Software Licensing Agreement Template|
|Application Model|Foundation|Catalog entry for an application, including lifecycle and components|SAP ERP Application Model|
|Business Capability|Design &amp; Planning|High-level ability enabling business outcomes|Customer Relationship Management Capability|
|Business Application|Design &amp; Planning|Logical representation of an application supporting capabilities|Salesforce CRM|
|Information Object|Design &amp; Planning|Conceptual representation of data artifacts|Customer Profile|
|Portfolio|Build &amp; Integration|Groups services or products for investment and lifecycle management|IT Service Portfolio|
|Service Offering|Build &amp; Integration|Defines variations or tiers of a service|Gold Tier Support Offering|
|Service Instance|Build &amp; Integration|Represents deployed instance of a service|Payroll Application Service – Production|
|Technology Management Service|Build &amp; Integration|Technical service provided by IT for managing technology components|Database Management Service|
|Technology Management Service Offering|Build &amp; Integration|Specific variation of a technical service|24x7 Network Monitoring Offering|
|Business Service|Service Delivery|Customer-facing service delivering measurable business value|Employee Onboarding Service|
|Customer-Facing Service|Service Delivery|Service consumed directly by external customers|Online Banking Service|

|Shape|Domain|Purpose|Example|
|-----|------|-------|-------|
|AI Dataset Digital Asset|Build &amp; Integration|Represents datasets used for AI training and inference|Customer Interaction Dataset|
|AI Model Digital Asset|Build &amp; Integration|Represents AI models with metadata and lifecycle details|Large Language Model for HR Chatbot|
|AI Prompt Digital Asset|Build &amp; Integration|Represents reusable prompts for generative AI|Incident Resolution Prompt|
|AI System Digital Asset|Build &amp; Integration|Represents deployable AI systems integrating models and datasets|AI Recommendation Engine|

|Shape|Domain|Purpose|Example|
|-----|------|-------|-------|
|AI System Product Model|Foundation|Catalog entry for AI systems at product level|Conversational AI Platform|
|AI Model Product Model|Foundation|Defines AI model product specifications|Image Classification Model|
|AI Prompt Product Model|Foundation|Captures reusable prompt templates for governance|Customer Query Summarization Prompt|
|AI Dataset Product Model|Foundation|Defines dataset product specifications|Product Image Dataset|
|Software Component Model|Foundation|Represents modular software components|Authentication Module|
|Software Model|Foundation|Represents software product models for licensing and compliance|Windows 11 Enterprise Model|
|Software Product|Foundation|Represents actual software product offered or used|Microsoft Office Suite|
|Product Feature|Foundation|Represents specific capability or function of a product|Multi-factor Authentication feature|

**Parent Topic:**[Exploring Enterprise Modeling and Visualization in the EA Workspace](eaw-modeling.md)

**Related topics**  


[Common Service Data Model \(CSDM\) shapes](../../reference/eaw-reference/eaw-modeling-csdm-shapes.md)

