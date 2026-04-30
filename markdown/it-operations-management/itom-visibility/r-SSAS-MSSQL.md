---
title: SQL Server Analysis Services \(SSAS\) discovery
description: The Discovery and Service Mapping application uses the SSAS pattern to find SQL Server Analysis Services \(SSAS\) on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store..
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Patterns, SQL, SSAS, Discovery, Server]
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# SQL Server Analysis Services \(SSAS\) discovery

The Discovery and Service Mapping application uses the SSAS pattern to find SQL Server Analysis Services \(SSAS\) on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store..

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify the applications are up to date.**

    Discovery and Service Mapping Patterns

    CMDB CI Class Models

    Visibility Content

-   **Verify the configuration of credentials**

    On the ServiceNow AI Platform®, verify the configuration of the Windows credentials. For more information, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)


## Data collected during horizontal discovery

Discovery populates the following data when running the SSAS pattern.

|SQL Server Analysis Services \[cmdb\_ci\_db\_mssql\_analysis\]|
|Label|Field|Description|
|--------------------------------------------------------------|
|-----|-----|-----------|
|Name|name|The SSAS on the Windows sever name|
|IP Address|ip\_address|The SSAS IP address|
|Version|version|The SSAS version|
|Edition|edition|The SSAS edition|
|Installation directory|install\_directory|The SSAS install directory|
|Instance Name|instance|The SSAS instance name|
|TCP port\(s\)|tcp\_port|The SSAS TCP port|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

