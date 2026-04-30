---
title: Rollup Framework for MSIM
description: Extends the capability of linking the source records from Major Security Incident Management workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Rollup Framework for MSIM

Extends the capability of linking the source records from Major Security Incident Management workspace.

## Overview

Rollup Framework makes the rollup flow configurable and extendable. Use this framework model to configure the information, which can be rolled up to a Major Security Incident.

Earlier, sn\_msi.workspace\_manager was able to link the security incidents and vulnerable items which were proposed or promoted as MSI. After linking the security incident or vulnerable item, the information was then rolled up to a major security incident. The type of information needed to be rolled up was hard-coded in the scripts.

You can use the framework model to configure the rollup flow, which supports the following features and also addresses the existing issues in the application:

The rollup framework model enables the sn\_msi.workspace\_manager with the following benefits to:

-   Add or remove the linking, propose, or promote MSI record capabilities on any table, which extends the task table.
-   Control the type of information to be rolled up to MSI while performing actions such as link/propose/promote on the incident records.
-   Support linking, propose, or promote for Security Incidents, Remediation tasks, and Security Cases Out of the box \(OOTB\) both from the classic environment and Major Security Incident Management workspace.

Rollup framework exhibit the configurations as explained in the following table.

|Name|Description|
|----|-----------|
|Linked Record Configuration|Stores the information of task tables which can be used to link/promote/propose to Major Security Incident.|
|Rollup Record Configuration|Captures the information which can be rolled up from task table when link/promote/propose actions are performed.|
|List Layout Configuration|Controls the labels and list layout for various tables as shown in the Major Security Incident Management workspace tabs such as Incident Impact, Linked Records, and Threat Intelligence.|

-   **[Configure Linked Records in Major Security Incident Management](../task/configuring-linked-records-in-major-security-incident-management.md)**  
Use Linked Records Configuration to store the information of task tables that can be used to link/promote/propose to Major Security Incident.
-   **[Configure Rollup Records in Major Security Incident Management](roll-up-record-configuration-in-major-security-incident-management.md)**  
Configure Roll up records in Major Security Incident Management to control the information, which will be rolled up when the source record is linked/proposed/promoted as Major Security Incidents.
-   **[Configure List Layout in Major Security Incident Management](list-layout-confguration.md)**  
Configure list layout to customize the layout and labels used in Major Security Incident Management workspace such as Incident Impact, Linked Records, and Threat Intelligence tabs.
-   **[Rollup example use case implementation for a Security Case](use-case-for-a-security-case.md)**  
The following steps explain an example use case on how to add support to link/propose/promote to Major Security Incident for a Security Case table.
-   **[Perform on demand atomic rollup](perform-on-demand-atomic-rollup.md)**  
Rollup framework cannot handle updates to the existing linked records. In such cases, on demand atomic rollup should happen for linked records, which can be achieved via business rules.

**Parent Topic:**[Major Security Incident Management](../reference/major-security-incident-management-landing-page.md)

