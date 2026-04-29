---
title: Operational Technology Manager use case
description: The Operational Technology Manager use cases are described in this section.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Implementing the CSDM framework for Operational Technology, Configure, Operational Technology Manager, Operational Technology]
---

# Operational Technology Manager use case

The Operational Technology Manager use cases are described in this section.

## Operational Technology Manager use case

The Operational Technology Manager application creates the foundational data and relationships that enable your enterprise to use the Operational Technology solution. It supports the use of the Configuration Management Database \(CMDB\), Service Graph Connectors, and Discovery applications in the ServiceNow AI Platform.

The OT Visibility dashboard in the Industrial Workspace summarizes your OT device inventory. For more information about the dashboard, see [Operational Technology Visibility dashboard](../../../mftg-manufacturing-oper-tech-mgr/concept/ot-manager-dashboard.md).

**Key features**

-   Operational Technology Manager uses OT configuration item \(CI\) extension classes that extend the CMDB class hierarchy.
-   IT Discovery for OT Networks is restricted to OT specific roles and OT related meta data can be added to an OT discovery schedule.
-   The Service Graph connector \(Excel\) imports OT data from a populated Microsoft Excel flat-file spreadsheet. This data is validated and then transformed into the appropriate table records and relationships to represent OT device details in the CMDB.

**Results**

With the Operational Technology Manager use case, you can:

-   Visualize dependencies of OT devices in the industrial environment.
-   Manage the life cycle of OT devices on a site-by-site basis with site specific RBAC
-   Create a solid data foundation and define critical levels of infrastructure.

## Industrial Process Manager use case

Use the Industrial Process Manager application to create the ISA-95 equipment model data foundation that is required for the Operational Technology solution.

**Key features**

You can perform the following operations in the Industrial Process Manager workspace:

-   Use ISA-95 models to describe the production process at each site in the industrial environment.
-   Manage equipment model entities and their relationships with each other and with OT devices.
-   Automatically map the relationship of all OT devices to the equipment model entity it automates using the OT subnet to equipment model entity relationship.

**Results**

The Industrial Process Manager enables you to create a custom version of the equipment models in each of your sites.

## Operational Technology Vulnerability Response use case

Operational Technology Vulnerability Response enables you to effectively prioritize and remediate OT device vulnerabilities at the site level.

**Key features**

-   Remediation owner workspace maps vulnerable items \(VITs\) with the production process.
-   Risk calculation for OT VITs can be based on criticality of the equipment model entity automated by the OT device.
-   Automatic assignment of VITs to remediation owners based on the site assigned to the OT device with the VIT.

**Results**

By leveraging the CMDB relationships of OT devices, you can prioritize vulnerable devices or items based on the criticality of the production process they automate.

As an OT engineer or OT vulnerability manager, Operational Technology Vulnerability Response enables you to find answers to questions such as:

-   What are my OT device vulnerabilities?​
-   How can I prioritize vulnerability remediation using OT specific risk?
-   What progress are we making toward remediation of OT vulnerabilities?

The OTVR \(PA\) dashboard and the OT Vulnerability Risk Management dashboard in the Industrial Workspace summarize the vulnerabilities in your system. For more information about the OTVR \(PA\) dashboard, see [Operational Technology Vulnerability Response \(PA\) dashboard](../../../mftg-manufacturing-ot-vulnerability-response/concept/operational-technology-vulnerability-response-dashboard.md). For more information about the OT Vulnerability Risk Management dashboard, see [Operational Technology Risk Management dashboard](../../concept/otvr-risk-management-dashboard.md).

## Operational Technology Incident Management use case

OT incidents occur when there is a disruption in service that is provided by an OT device on an OT network. Sometimes, the OT device may not be known when the incident is first created. Operational Technology Incident Management enables engineers to quickly resolve OT device and production process issues.

**Key features**

When a user creates an OT incident from the Industrial Workspace, the incident is automatically assigned a Network Type of OT to distinguish an OT incident from an IT incident. The field is not displayed by default.

**Results**

Operational Technology Incident Management enables engineers to quickly resolve OT device and production process issues. It enables you to manage OT incidents separately from IT incidents.

## Operational Technology Change Management use case

Operational Technology Change Management enables your team members to work collaboratively on changes to OT devices or industrial equipment configurations.

**Key features**

-   Digitized change workflow that connects all stakeholders.
-   Sites that have different change management processes \(workflows\).
-   Separated IT Change Management and Operational Technology Change Management, but ability to be combined if necessary.
-   Integrated Operational Technology Change Management workflow with the Operational Technology Incident Management and Operational Technology Vulnerability Response applications.
-   Aligned factory floor changes for the equipment model entities with downtime schedules.

**Results**

The following examples show how to apply Operational Technology Change Management to your organization:

-   An OT remediation owner, who's responsible for fixing vulnerabilities on OT devices, wants to initiate a change to fix a group of vulnerabilities.
-   An OT technician, who's responsible for OT configurations and plant engineering activities, wants to execute a change to fix a malfunctioned robotic arm on the industrial floor.
-   A plant head, who's responsible for overall production activity, wants to review and approve a change requested by the engineering team.

## Operational Technology Knowledge Management use case

Operational Technology Knowledge Management helps you to capture information about your Operational Technology \(OT\) system in knowledge articles that are related to OT incidents. Your organization can then use these knowledge articles to help your users to access the right information and prevent miscommunication with your users.

**Key features**

-   Ability to use the existing Knowledge Management ServiceNow AI Platform capabilities with the Operational Technology Management solution.
-   Ability to browse all knowledge base articles that are related to an OT incident and to create knowledge articles directly from an incident record.
-   Ability to configure an OT knowledge base for knowledge managers and knowledge users.
-   Ability to create knowledge articles in the Industrial Workspace.
-   Ability to request approvals to publish, edit, retire, or delete a knowledge article.
-   Ability to edit existing knowledge articles with updated information.

**Results**

The following examples show how to apply  Operational Technology Knowledge Management to your team:

-   An OT engineer with several years of experience wants to capture their OT device knowledge in one place for guide workers and junior technicians.
-   Front-line workers and technicians responsible for production process operations have noticed an issue on the factory floor and need a knowledge article that explains remediation.

## Operational Technology Request Management use case

Operational Technology Request Management enables you to access the OT Service Catalog to request OT catalog items and fulfill them based on the defined flows. OT workers can then create and submit an OT request from a catalog item, which helps provide a consistent experience and facilitates cross-functional requests.

**Key features**

-   Provides a single view to efficiently manage multiple catalog requests​.
-   Encourages transparency, expedites request processes, and minimizes delays with automatic notifications and approvals.
-   Maintains the products and services menu that you can use to create and update catalog requests.

**Results**

The following examples show how to apply  Operational Technology Request Management to your team:

-   OT engineers can file and manage OT requests for various OT products and services in a one place.
-   A plant head or supervisor can engage with the correct team to remediate an incident reported on the factory floor.​

**Parent Topic:**[Implementing the CSDM framework for Operational Technology](ot-use-case-product-view.md)

