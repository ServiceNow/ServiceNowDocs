---
title: ColdFusion discovery
description: The ServiceNow Discovery application finds Adobe ColdFusion servers and the instances of ColdFusion applications running on them. Only the 2016 version of ColdFusion is supported. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# ColdFusion discovery

The ServiceNow Discovery application finds Adobe ColdFusion servers and the instances of ColdFusion applications running on them. Only the 2016 version of ColdFusion is supported. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Components

Discovery and Service Mapping use the **ColdFusion Application** and **ColdFusion Application Server** patterns to run horizontal and top-down discovery. The **ColdFusion Application Server** pattern is triggered from the ColdFusion Application Server process classifier for horizontal discovery.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Credentials**

    Configure the following credentials, depending on what type of host machine the ColdFusion server is installed on:

    -   Windows credentials
    -   SSH credentials \(for Linux machines\)
-   **File access**

    The pattern must be able to access these ColdFusion files:

<table id="table_vpz_wx2_rdb"><thead><tr><th>

File

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`neo-runtime.xml`

</td><td>

This file provides the mapping between the URL and the working directory path of the application.

</td></tr><tr><td>

``application.cfc` and `application.cfm``

</td><td>

These files provide application names.

</td></tr><tr><td>

`neo-datasource.xml`

</td><td>

This file provides the name of the datasource that is used in the configuration of the ColdFusion application. The datasource reference is configured in the `application.cfc` and `application.cfm` files.**Note:** The datasource is used for top-down discovery only.

</td></tr></tbody>
</table>-   **Entry point**

    For top-down discovery, use the full URL or IP address of the web application as the HTTP\(S\) endpoint. For example: `https://my-website-on-coldfusion/path` or `https:10.120.255.2555:8500/path`


## Data collected during horizontal discovery

<table id="table_qxf_nsd_rdb"><thead><tr><th>

Table and Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Cold Fusion Server \[cmdb\_ci\_coldfusion\_server\]

</td></tr><tr><td>

Installation directory \[installation\_directory\]

</td><td rowspan="3">

The name and version of the ColdFusion server, and the directory where it is installed.

</td></tr><tr><td>

Name \[name\]

</td></tr><tr><td>

Version \[version\]

</td></tr><tr><td>

Installation directory \[installation\_directory\]

</td><td rowspan="2">

The name of the application and the directory where it is installed.

</td></tr><tr><td>

Name \[name\]

</td></tr></tbody>
</table>**Note:** Cold Fusion applications \[cmdb\_ci\_cf\_application\] are custom applications that this pattern does not discover.

## CI relationships

<table id="table_vkt_ywd_rdb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_cf\_application

</td><td>

Contains::Contained by

</td><td>

cmdb\_ci\_coldfusion\_server

</td></tr><tr><td>

cmdb\_ci\_coldfusion\_server

</td><td>

Runs on::Runs

</td><td>

cmdb\_ci\_linux\_server

 cmdb\_ci\_win\_server

 cmdb\_ci\_osx\_server

</td></tr></tbody>
</table>## Connections discovered by Service Mapping during the top-down discovery

Service Mapping performs the top-down discovery of the Adobe ColdFusion in the context of application services. Service Mapping discovers the outgoing datasource connections from ColdFusion servers to instances of database.

## Example

In this example, the application service map shows the results of a top-down discovery of the ColdFusion Web application service. The application service is comprised of three CIs:

-   The ColdFusion application server is named **cfusion**.
-   The ColdFusion application **hdStreetOracle**.
-   A database named **XE**, which the ColdFusion application connects to.

![ColdFusion service map](../image/cold-fusion-service-map.png "ColdFusion service map")

**Parent Topic:**[Available discovery patterns](available-patterns.md)

