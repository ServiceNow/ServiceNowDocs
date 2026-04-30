---
title: IBM App Connect Enterprise and HTTP listener discovery
description: Discovery and Service Mapping Patterns application uses the WMB patterns to discover Integration Bus \(formerly WebSphere Message Broker and IBM Integration Bus\) and HTTP listeners running on both Linux and Windows. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [WMB, IBM WMB, IBM WebSphere Message Broker, HTTP listener, IBM WebSphere Message Broker HTTP listener, IBM Integration Bus, IIB, IBM App Connect Enterprise, IBM ACE]
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# IBM App Connect Enterprise and HTTP listener discovery

Discovery and Service Mapping Patterns application uses the WMB patterns to discover Integration Bus \(formerly WebSphere Message Broker and IBM Integration Bus\) and HTTP listeners running on both Linux and Windows. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

By default, Discovery uses the following patterns to perform the discovery:

-   WMB On UNIX
-   WMB On Windows
-   WMB HTTP Listener On UNIX
-   WMB HTTP Listener On Windows

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

To learn about IBM WebSphere Message Broker \(WMB\) and WMB HTTP Listener components and versions that you can discover, see [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md).

## Prerequisites

-   **Verify the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content

## Data collected by Discovery during horizontal discovery

-   **Resources discovered by the WMB On UNIX pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the message broker|
    |Installation directory \[install\_directory\]|Install directory of the message broker|
    |Version \[version\]|Version of the message broker|

-   **Resources discovered by the WMB On Windows pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the message broker|
    |Installation directory \[install\_directory\]|Install directory of the message broker|
    |Version \[version\]|Version of the message broker|

-   **Resources discovered by the WMB HTTP Listener On UNIX pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the HTTP listener|
    |Installation directory \[install\_directory\]|Install directory of the HTTP listener|

-   **Resources discovered by the WMB HTTP Listener On Windows pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the HTTP listener|
    |Installation directory \[install\_directory\]|Install directory of the HTTP listener|


**Parent Topic:**[Software discovery](../concept/c_Software.md)

