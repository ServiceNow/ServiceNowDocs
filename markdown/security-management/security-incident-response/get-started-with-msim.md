---
title: Get started with MSIM
description: Review the following information before you start working with Major Security Incident Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/get-started-with-msim.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with MSIM

Review the following information before you start working with Major Security Incident Management.

Role required: sn\_msi.workspace\_admin.

For an easy installation and configuration of the Major Security Incident Management application, you may have to verify if the following plugins are activated.

<table id="table_k5l_nk1_rpb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Before you begin with the application, ensure that you have the required dependent plugins.

</td><td>

Install:-   [ServiceNow IntegrationHub Installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/request-ih-overview.md) \(com.glide.hub.integrations\)
-   ServiceNow® Integration Hub Runtime \(com.glide.hub.integration.runtime\).
-   ServiceNow® Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow® Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow® Integration Hub Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** If you don't have the necessary privileges for any of the listed ServiceNow® Integration Hub plugins, then raise a support ticket to install those prerequisite applications.

</td></tr><tr><td>

Verify that you have required access to install Microsoft SharePoint Spoke and Microsoft Teams Graph Spoke.**Note:** The above listed are the primary dependent applications to get started with Major Security Incident Management.

</td><td>

Before you install Microsoft SharePoint Spoke and Microsoft Teams Graph Spoke, make sure you have required access to the ServiceNow Integration Hub applications.**Note:** Microsoft SharePoint Spoke and Microsoft Teams Graph spoke are dependent applications to ServiceNow® Integration Hub applications.

Microsoft SharePoint Spoke version 1.1.2 is required for Graph and REST connections.

</td></tr></tbody>
</table>**Important:** After you install the Major Security Incident Management application, import the update set to integrate Microsoft SharePoint and Microsoft Teams with ServiceNow using certificate credentials. For more information, see [KB1289784](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1289784).

**Parent Topic:**[Exploring Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/exploring-major-security-incident-management.md)

**Related topics**  


[Major Security Incident Management]()

[Checklist for MSIM setup]()

[Major Security Incident Management roles]()

[Environment reference for MSIM setup]()

