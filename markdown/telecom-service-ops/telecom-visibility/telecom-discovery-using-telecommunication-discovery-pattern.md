---
title: Telecom Discovery using Telecommunications Discovery Patterns
description: The new Telecommunication Discovery Patterns \(also known as TSOM Patterns\) include patterns for discovering standalone xNFs, enabling the discovery of standalone network elements without a management system, using SNMP, CLI, and NETCONF \(roadmap\) protocols.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Telecom Discovery using Telecommunications Discovery Patterns

The new Telecommunication Discovery Patterns \(also known as TSOM Patterns\) include patterns for discovering standalone xNFs, enabling the discovery of standalone network elements without a management system, using SNMP, CLI, and NETCONF \(roadmap\) protocols.

## Architecture using Horizontal Discovery and Telecommunications Discovery Patterns

This is an example of the implementation for standalone SNMP or/and CLI xNFs.![discovery and telecommunications discovery pattern.](../images/telecom-discovery-reconciliation-pattern.png)

## Horizontal Discovery Application

The Horizontal Discovery application in ServiceNow is a versatile and highly scalable discovery engine designed to operate effectively across network, IT, and cloud environments, collecting data across multiple layers to provide a holistic view of the infrastructure.

For more information, see [Horizontal discovery process flow with patterns](https://www.servicenow.com/docs/access?context=disco-process-flow-patterns&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## Telecommunications Discovery Patterns \(TSOM Patterns\)

A pattern is a sequence of commands designed to detect attributes of a configuration item \(CI\) and its outbound connections. Telecom Discovery provides a set of preconfigured Patterns that cover a wide range of network elements. The TSOM Discovery Patterns fall under the infrastructure category, which are used by Horizontal Discovery to generate lists and resource structure of xNFs.

This plugin introduces Patterns for discovering standalone xNFs, such as telecom routers and switches \(with support for other device types planned in the future\) that don’t rely on a management system or require direct discovery by bypassing their management systems. Additionally, custom patterns are included for verifying various network devices. This is a customer-visible plugin.

## MID Server

MID Server is a Java application that runs as a Windows service or UNIX daemon on a server within your local network. The ServiceNow® MID Server facilitates communication and data transfer between a ServiceNow instance and external applications, data sources, and services.

For more information, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Identification &amp; Reconciliation Engine \(IRE\)

IRE offers a centralized framework for identifying and reconciling data from multiple sources. It verifies the integrity of the CMDB and some non-CMDB tables when various data sources are used to create or update CI records.

For more information, see [Telecom Discrepancy Identification and Reconciliation](telecom-reconciliation.md).

## CMDB Compliance Certification Audits for Telecom Discrepancy Identification &amp; Reconciliation

CMDB Compliance is a toolset that enables administrators to certify CMDB data for accuracy and resolve any discrepancies found. In Telecom Discrepancy Identification &amp; Reconciliation, we use the Certification Audits feature to discover and analyze discrepancies in the CMDB, generate Certification Follow-on Tasks, and enable remediation workflows.

For more information on how it’s used for Discrepancy Identification &amp; Reconciliation, see [Telecom Discrepancy Identification and Reconciliation](telecom-reconciliation.md).

## ITOM vs TSOM Discovery Behavior for Stand-alone SNMP or/and CLI xNFs

|ITOM Discovery|TSOM Discovery \(Telecom\)|
|--------------|--------------------------|
|Based on Horizontal Discovery Patterns.|Based on Horizontal Discovery Patterns \(for Telecommunications\).|
|Discover basic equipment flat information which is primarily used for the IT purposes.|Discover more attributes and a deeper CI hierarchy based on equipment type.|
|Only standard MIBs are supported.|Both standard and vendor proprietary MIBs are supported.|
|No discrepancy detection and remediation available OOB.|Discrepancy detection and automatic or manual remediation available OOB.|

-   Telecom Discovery is built on the ITOM Discovery application, leveraging the Nebula Discovery Language \(NDL\).
-   The solution includes a set of telecom-specific patterns and system properties.
-   Users can choose whether to run TSOM or ITOM patterns.
-   Customers can extend TSOM patterns or create their own if necessary.
-   There’s no dependency between TSOM Visibility and Telecom Network Inventory \(TNI\).

## Logic added to Telecom Discovery

Users can define whether they want to use Telecommunications Discovery Patterns \(also known as TSOM patterns\) with ITOM patterns for execution. By default, all patterns created in TSOM/Telecom Discovery execute the original ITOM pattern \(for example, the 'Telco Router' pattern also executes the 'Router' pattern\). However, customers have the option to choose whether they want to execute only the TSOM pattern and exclude the ITOM pattern.

This parameter affects only the patterns developed as part of the TSOM Patterns application for Telco customers. If the property is set to true \(default\), the TSOM pattern will also execute specific ITOM shared libraries from the TSOM pattern.

This logic is controlled via the system property: sn\_tsom\_patterns.itom\_pattern\_enabled.

**Follows the TNI model** – Telecommunications Discovery Patterns always follow the TNI data model. This means that if Telecom Discovery identifies a card-on-card scenario, it doesn’t insert it as a card-on-card. Instead, it modifies the structure by synthesizing a subslot on the parent card and inserting the child card into that subslot.

**TNI entity creation logic** – Whenever the system identifies that the customer has TNI installed, it will automatically create a TNI entity record for all network data discovered. If TNI is installed, a payload like the one below will be added to the IRE payload for each item. As a result, the discovered CI is in both the cmdb\_ci and tni\_entity tables.

-   **[Telecom Router Pattern](telecom-router-pattern.md#)**  
The ServiceNow® Telecom Discovery application uses the Telecom Router discovery pattern to find SNMP-based routers in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow Store.
-   **[Telecom Cisco 7613 Router Pattern](telecom-cisco7613-router-pattern.md#)**  
The ServiceNow Telecom Discovery application uses the Telecom Cisco 7613 Router discovery pattern to find SNMP-based Cisco 7613 in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow Store.
-   **[Telecom Juniper MX SSH Router Pattern](telecom-juniper-mx-ssh-router-pattern.md#)**  
The ServiceNow® Telecom Discovery application uses the Telecom Juniper MX SSHRouter discovery pattern to find SNMP and CLI -based Juniper MX Series routers in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow® store.
-   **[Telecom Cisco Switch Pattern](telecom-cisco-switch-pattern.md#)**  
The ServiceNow® Telecom Discovery application uses the Telecom Cisco Switch discovery pattern to find SNMP-based Cisco switches in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow® Store.
-   **[Telecom Switch Pattern](telecom-switch-pattern.md#)**  
The ServiceNow® Telecom Discovery application uses the Telecom Switch discovery pattern to find SNMP-based Telecom switches in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow® Store.
-   **[Configure Telecommunications Discovery \(TSOM\) Patterns](configuring-telecommunications-discovery-patterns.md#)**  
This document outlines the dependencies, requirements, and installation steps necessary for setting up Telecommunications Discovery Patterns \(also known as TSOM Patterns\) in TSOM Visibility in ServiceNow®.

**Parent Topic:**[Exploring Telecom Discovery](exploring-telecom-discovery.md)

