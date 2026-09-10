---
title: Red Hat JBoss EAP Server pattern-based discovery on UNIX
description: Discovery and Service Mapping Patterns uses the Red Hat - JBoss Enterprise App Platform Server on Unix pattern to find JBoss Enterprise Application Platform \(JBoss EAP\) Server instances running on UNIX servers. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/red-hat-jboss-eap-server-unix-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-07-26"
reading_time_minutes: 2
keywords: [JBoss, Red Hat, JBoss Enterprise Application Platform, application pattern]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Red Hat JBoss EAP Server pattern-based discovery on UNIX

Discovery and Service Mapping Patterns uses the Red Hat - JBoss Enterprise App Platform Server on Unix pattern to find JBoss Enterprise Application Platform \(JBoss EAP\) Server instances running on UNIX servers. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify that the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
    -   ITOM Content Service
-   **Create SSH credentials**

    For more information, see [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_SSHCredentialsForm.md).

-   **Verify read access to the version file**

    Verify you have permission for the following command: `cat {process.currentDir}/version.txt`.

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Red Hat - JBoss Enterprise App Platform Server on Unix pattern.

If you have the Software Asset Management Core \(com.snc.sam.core\) or Software Asset Management \(com.snc.software\_asset\_management\) plugins, Discovery also populates the Software Installation \[cmdb\_sam\_sw\_install\] table.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the application in the following format: **Red Hat JBoss Enterprise Application Platform Server@\{hostname\}**.|
|Product \[product\]|Product name. The value is set to **JBoss Enterprise Application Platform**.|
|Publisher \[publisher\]|Publisher of the application. The value is set to **Red Hat**.|
|Component \[component\]|Component of the application. The value is set to **Server**.|
|Installation directory \[install\_directory\]|Installation directory of the application.|
|Version \[version\]|Version of the application.|
|Software Install \[software\_install\]\*|References the Software Installation \[cmdb\_sam\_sw\_install\] table.|

\* Populated only when a Software Asset Management plugin is activated.

## CI relationships and references

The Red Hat - JBoss Enterprise App Platform Server on Unix pattern creates the following relationships and references to support Red Hat JBoss EAP Server discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Application \[cmdb\_ci\_appl\]|Runs on::Runs|Linux Server \[cmdb\_ci\_linux\_server\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Application \[cmdb\_ci\_appl\]|Software Install \[software\_install\]|Software Installation \[cmdb\_sam\_sw\_install\]\*|

\* Populated only when a Software Asset Management plugin is activated.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

