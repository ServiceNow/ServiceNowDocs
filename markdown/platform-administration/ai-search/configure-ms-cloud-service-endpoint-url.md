---
title: Configure the Microsoft cloud service endpoint URL
description: Specify the proper cloud service endpoint URL to use for external content connectors that crawl your Microsoft cloud application tenants.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 1
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the Microsoft cloud service endpoint URL

Specify the proper cloud service endpoint URL to use for external content connectors that crawl your Microsoft cloud application tenants.

## Before you begin

Role required: ais\_admin or admin

## About this task

Integrations and API calls for the Microsoft SharePoint Online and Microsoft Teams external content connectors rely on a Microsoft cloud service endpoint URL that's specified as the value of the **sn\_ext\_conn\_admin.microsoft\_authority\_host** system property.

By default, this property's value is `https://login.microsoftonline.com`, the endpoint URL for the Microsoft 365 cloud. If your organization's Microsoft application tenants are in a different cloud, you need to update the system property's value to specify the appropriate endpoint URL.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Open the record for the **sn\_ext\_conn\_admin.microsoft\_authority\_host** system property by selecting it from the list.

    If the system prompts you to change the application scope so that you can edit the record, select the provided link.

3.  In the system property's **Value** field, change the existing URL to the cloud service endpoint URL for your Microsoft cloud.

    As an example, if your Microsoft application tenants are in the Microsoft 365 GCC High cloud or the Microsoft 365 DoD cloud, enter `https://login.microsoftonline.us/` as the URL.

    **Important:** The URL specified as the property value must end with a trailing slash. Entering a URL without a trailing slash may cause connectivity failures in the Microsoft SharePoint Online and Microsoft Teams external content connectors.

4.  Select **Update**.


**Parent Topic:**[Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md)

