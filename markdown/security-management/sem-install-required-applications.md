---
title: Download and activate applications
description: Download the required Security Exposure Management Workspace applications from the ServiceNow Store into your ServiceNow AI Platform and activate them to upgrade.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Installing Security Exposure Management Workspace applications, Implement, Unified Security Exposure Management, Security Operations]
---

# Download and activate applications

Download the required Security Exposure Management Workspace applications from the ServiceNow® Store into your ServiceNow AI Platform® and activate them to upgrade.

## Before you begin

-   Download core products and applications.
    -   A product contains one or more applications. For example, Vulnerability Response is a product.
    -   An application is a standalone piece of code that implements a collection of features.
    -   A plugin is a set of customizations that extends the functionality of the ServiceNow AI Platform® and any apps already installed on your instance. Some plugins are pre-activated in your instance, while others might need to be activated manually by you or by ServiceNow® personnel.
-   Some applications have dependencies that you must download and install separately.

For more information about downloading and activating applications see [Download an application from the ServiceNow Store for the first time](../../security-incident-response/reference/download-app-first-time.md).

**Note:** If you're downloading applications to sub-production or development instances, it's not necessary to get entitlements.

Role required: admin for download, installation, and activation of all applications.

## Procedure

1.  Click the link provided to you in the email you received to access the required applications in the ServiceNow Store.

    Select the **Dependencies** link to view the dependencies for an application on the application's listing page in the ServiceNow Store.

2.  After you have downloaded the applications into your ServiceNow AI Platform, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  To activate the applications you downloaded along with any of their dependencies and plugins in the order listed in the following table, locate the cards for the applications and select **Install**.

    Any dependency applications are typically installed automatically along with an application and are displayed in the Application installation dialog. However, if you are prompted to install dependency plugins during the installation, follow the prompts provided.

    A dialog is displayed after an application is successfully activated.

    |Application name|App id and version|Description|
    |----------------|------------------|-----------|
    |Vulnerability Response dependencies|com.snc.vul\_dep|Installs all the dependent plugins required to support the Vulnerability Response application.|
    |Security Integration Framework|sn\_sec\_int|Common functionality for Security Operations integrations. Dependency for Vulnerability Response.|
    |Security Support Common|sn\_sec\_cmn|Provides the necessary functionality to support Security Operations applications, includingVulnerability Response. This application supports integrations, email processing, filter groups, security tags, workflows, and so on.|
    |Security Support Orchestration|sn\_sec\_cmn\_orch|Dependency for the Vulnerability Response application.|
    |Vulnerability Response Common|sn\_vul\_cmn|Enables core functionality used by Vulnerability Response applications.|
    |Risk Scoring for Security Exposure Management|app-sec-calculator|Calculate and roll-up risk scores across all Security Exposure Management applications.|
    |Administration for Security Exposure Management|app-sec-workflow|Manage configuration for all Security Exposure Management applications from a centralized admin console.|
    |Remediation for Security Exposure Management|app-sec-rem|Group and manage findings into Remediation Tasks across all Security Exposure Management applications.|
    |Vulnerability Response Common Workspace|sn\_vul\_cmn\_ws|Vulnerability Response Common Workspace is a framework that supports and provides common resources for the Vulnerability Response Workspaces.|
    |Security Exposure Management|app-vul-uasm|Manage security exposure across your organization from within a single workspace for all personas.|
    |Exception Management for Unified Security Exposure Management|app-sec-exception|Align approvers and security and remediation teams to efficiently manage exceptions and false positives through configurable approval workflows.|
    |Vulnerability Response|sn\_vul|Connects the workflow and automation capabilities of the ServiceNow AI Platform with imported vulnerability scan data from leading vendors.|
    |Configuration Compliance dependencies|com.snc.vulc\_dep|Plugin that provides dependencies for the Configuration Compliance application.|
    |Configuration Compliance|com.snc.vulc|Exposes configuration-related security vulnerabilities.|
    |Vulnerability Response and Configuration Compliance for Containers|sn\_vul\_container|Imports vulnerability scan data from leading container security vendors.|

    [Security Exposure Management Workspace Roles](../reference/sem-new-roles-installed.md)


