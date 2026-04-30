---
title: External Content Connectors properties
description: A system property supports configuration of the Microsoft cloud service endpoint URL used by the Microsoft SharePoint Online and Microsoft Teams external content connectors.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-04-16"
reading_time_minutes: 1
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# External Content Connectors properties

A system property supports configuration of the Microsoft cloud service endpoint URL used by the Microsoft SharePoint Online and Microsoft Teams external content connectors.

This property is available for External Content Connectors.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_kvn_dgj_x2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ext\_conn\_admin.microsoft\_authority\_host

</td><td>

Microsoft cloud service endpoint URL used for integrations and API calls. This property affects the Microsoft SharePoint Online and Microsoft Teams external content connectors

 Set the value of this property to ensure that the system connects to the correct Microsoft cloud for your tenant.

-   Type: string
-   Default value: `https://login.microsoftonline.com/`
-   Supported values:

    -   `https://login.microsoftonline.com/`: Endpoint URL for the Microsoft 365 cloud.
    -   `https://login.microsoftonline.us/`: Endpoint URL for the Microsoft 365 GCC High and Microsoft 365 DoD clouds.
**Important:** The URL specified as the property value must include a trailing slash, as shown for the listed values.

-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure the Microsoft cloud service endpoint URL](../task/configure-ms-cloud-service-endpoint-url.md)

</td></tr></tbody>
</table>**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

