---
title: IBM MQ discovery
description: The ServiceNow Discovery application uses the WMQ On Unix and WMQ On Windows patterns to find IBM MQ \(formerly IBM WebSphere MQ\) resources. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM MQ discovery

The ServiceNow Discovery application uses the WMQ On Unix and WMQ On Windows patterns to find IBM MQ \(formerly IBM WebSphere MQ\) resources. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Discovery uses the following patterns to perform horizontal discovery:

-   **WMQ On Unix**
-   **WMQ On Windows**

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery for IBM MQ

Discovery populates the data in the CMDB when running the WMQ patterns.

|Label|Field Name|
|-----|----------|
|Name|name|
|Version|version|
|Installation directory|install\_directory|
|Class|sys\_class\_name|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

