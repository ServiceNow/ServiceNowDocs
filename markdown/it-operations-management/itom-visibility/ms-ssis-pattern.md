---
title: Microsoft SQL Server Integration Services \(SSIS\) discovery
description: The Discovery and Service Mapping application uses the SSIS pattern to find SQL Server Integration Services \(SSIS\) on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Pattern, Discovery, SSIS, SQL, Server, Integration, Services]
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Microsoft SQL Server Integration Services \(SSIS\) discovery

The Discovery and Service Mapping application uses the SSIS pattern to find SQL Server Integration Services \(SSIS\) on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify the plugins setup**

    Discovery and Service Mapping Patterns

    CMDB CI Class Models

    Visibility Content

-   **Verify the configuration of credentials**

    On the ServiceNow AI Platform®, verify the configuration of the Windows credentials. For more information, see [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_WindowsCredentialsForm.md)


## Data collected during horizontal discovery

Discovery populates the following data when running the SSIS pattern.

|SQL Server Integration Services \[cmdb\_ci\_db\_mssql\_integration\_list\]|
|Label|Field|Description|
|--------------------------------------------------------------------------|
|-----|-----|-----------|
|Name|name|The SSIS on the Windows sever name|
|IP Address|ip\_address|The SSIS IP address|
|Version|version|The SSIS version|
|Edition|edition|The SSIS edition|
|Installation directory|install\_directory|The SSIS install directory|
|Instance Name|instance|The SSIS instance name|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

