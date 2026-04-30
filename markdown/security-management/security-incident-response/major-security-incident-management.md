---
title: Major Security Incident Management
description: Track and manage various activities that are typically part of resolving a major security incident through Major Security Incident Management. Through an intuitive workspace, incident managers and those working on an incident can propose and promote incidents to major incidents, track major security incident activities, and easily collaborate with colleagues.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Major Security Incident Management

Track and manage various activities that are typically part of resolving a major security incident through Major Security Incident Management. Through an intuitive workspace, incident managers and those working on an incident can propose and promote incidents to major incidents, track major security incident activities, and easily collaborate with colleagues.

## Overview

The major security incident management capabilities work in conjunction with the existing security incident response product capabilities. This includes an ability for a security analyst to escalate a standard security incident to a major security incident, so that the new product capabilities are available to support the remediation process.

After you install on your ServiceNow instance, a security incident analyst can:

-   Propose a security incident to major security incident candidate to initiate a review process on the need to create a major security incident.
-   Directly promote a security incident to a major security incident without the need for an additional review process.
-   Reject a security incident that is proposed as a major security incident \(MSI\).
-   Link a security incident as a child incident to the major security incident \(MSI\) so that all security incidents can be worked.

## Key features

Major Security Incident Management \(MSIM\) improves the major security incident remediation process with the following features:

-   Dedicated workspace for managing major security incidents designed for the major security incident manager user role.
-   Organize response tasks across multiple 'child' security incidents.
-   Automate creation of collaboration folders and chat communication channels after a major security incident is created, as well as archival as part of incident closure.
-   File explorer component to organize and track the collection of artifacts \(files\) related to the major security incident via a Microsoft SharePoint integration.
-   Chat channel manager and activity stream components to manage communications across multiple security, IT, and functional groups via a Microsoft Teams integration.

## Workspace Components

The Major Security Incident Management product contains several new workspace components and user interface pages that deliver the key features functionality:

-   Dedicated workspace for managing major security incidents specifically designed for the major Security Incident Manager user role.
-   Organize response tasks across multiple child security incidents.
-   Automate creation of collaboration folders and chat communication channels after a major security incident is created, as well as archival as part of incident closure.
-   File explorer component to organize and track the collection of artifacts \(files\) related to the major security incident via a Microsoft SharePoint integration.
-   Chat channel manager and activity stream components to manage communications across multiple security, IT, and functional groups via a Microsoft Teams integration.

## Supported Major Security Incident Management versions

Major Security Incident Management \(MSIM\) requires ServiceNow AI Platform® Rome version.

This feature supports Microsoft Teams, which is a chat-centered workspace in the Microsoft Office 365 suite. Earlier Microsoft Teams was a separate installation from Microsoft Office 365 applications.

## Supported ServiceNow AI Platform versions

This feature is supported on Rome and later releases.

The following Security Operations applications are the standard Security Incident Response plugins that will likely be installed for most of the users if they’re using already Security Incident Response \(SIR\). If not installed, you must install and activate from ServiceNow Store. Install and then activate one application at a time in the order mentioned to ensure a smooth installation:

1.  Security Incident Response: com.snc.si\_dep is the dependent plugin. Installing this plugin activates the other Security Operations applications.
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Common Orchestration

**Parent Topic:**[Exploring Major Security Incident Management](../reference/exploring-major-security-incident-management.md)

**Related topics**  


[Get started with MSIM](../reference/get-started-with-msim.md)

[Checklist for MSIM setup](../../security-incident-response/reference/msim-checklist.md)

[Major Security Incident Management roles](../reference/msi-roles.md)

