---
title: Oracle HTTP Server pattern-based discovery
description: Discovery and Service Mapping Patterns uses the Oracle - HTTP Server pattern to find Oracle HTTP Server instances running on Windows servers. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/oracle-http-server-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-08-05"
reading_time_minutes: 1
keywords: [Oracle HTTP Server, application pattern, pattern-based discovery]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle HTTP Server pattern-based discovery

Discovery and Service Mapping Patterns uses the Oracle - HTTP Server pattern to find Oracle HTTP Server instances running on Windows servers. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify that the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
    -   ITOM Content Service
-   **Create Windows credentials**

    For more information, see [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/r_WindowsCredentialsForm.md).

-   **Verify read access to the application executable**

    Verify you have permission for the following command: `powershell -Command "Select-String -Path '{executablePath}' -Pattern 'Server version' -SimpleMatch"`.

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle - HTTP Server pattern.

If you have the Software Asset Management Core \(com.snc.sam.core\) or Software Asset Management \(com.snc.software\_asset\_management\) plugins, Discovery also populates the Software Installation \[cmdb\_sam\_sw\_install\] table.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the application in the following format: **Oracle HTTP Server@\{hostname\}**.|
|Product \[product\]|Product name. The value is set to **HTTP Server**.|
|Publisher \[publisher\]|Publisher of the application. The value is set to **Oracle**.|
|Installation directory \[install\_directory\]|Installation directory of the application.|
|Version \[version\]|Version of the application.|
|Software Install \[software\_install\]\*|References the Software Installation \[cmdb\_sam\_sw\_install\] table.|

\* Populated only when a Software Asset Management plugin is activated.

## CI relationships and references

The Oracle - HTTP Server pattern creates the following relationships and references to support Oracle HTTP Server discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Application \[cmdb\_ci\_appl\]|Software Install \[software\_install\]|Software Installation \[cmdb\_sam\_sw\_install\]\*|

\* Populated only when a Software Asset Management plugin is activated.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

