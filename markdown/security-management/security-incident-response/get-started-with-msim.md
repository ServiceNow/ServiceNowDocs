---
title: Get started with MSIM
description: Review the following information before you start working with Major Security Incident Management.
locale: en-US
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

**Important:** An update set \([KB1289784](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1289784)\) is available within the Major Security Incident Management Quick Start Guide to help users with an easy configuration set up, you need to import the update set after you complete the application installation. Follow the procedure detailed in the Quick Start Guide \(Step 2\) under the Supporting documents section within the MSIM application, which is on ServiceNow Store.

<table id="table_k5l_nk1_rpb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Before you begin with the application, ensure that you have the required dependent plugins.

</td><td>

As a first step, install:-   [ServiceNow IntegrationHub Installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/request-ih-overview.md) \(com.glide.hub.integrations\)
-   ServiceNow® Integration Hub Runtime \(com.glide.hub.integration.runtime\).
-   ServiceNow® Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow® Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow® Integration Hub Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** If you don't have the necessary privileges for any of the listed ServiceNow® Integration Hub plugins, then raise a support ticket to install those prerequisite applications.

</td></tr><tr><td>

Verify that you have required access to install Microsoft SharePoint Spoke and Microsoft Teams Graph Spoke.**Note:** The above listed are the primary dependent applications to get started with Major Security Incident Management.

</td><td>

Before you install Microsoft SharePoint Spoke and Microsoft Teams Graph Spoke, make sure you have required access to the ServiceNow Integration Hub applications.**Note:** Microsoft SharePoint Spoke and Microsoft Teams Graph spoke are dependent applications to ServiceNow® Integration Hub applications.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Major Security Incident Management](exploring-major-security-incident-management.md)

**Related topics**  


[Major Security Incident Management](../concept/major-security-incident-management.md)

[Checklist for MSIM setup](../../security-incident-response/reference/msim-checklist.md)

[Major Security Incident Management roles](msi-roles.md)

