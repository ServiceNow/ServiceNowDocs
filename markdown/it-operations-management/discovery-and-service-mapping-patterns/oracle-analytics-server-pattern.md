---
title: Oracle Analytics Server pattern-based discovery
description: Discovery and Service Mapping Patterns finds Oracle Analytics Server \(formerly Oracle Business Intelligence Enterprise Edition\) components on Windows and Linux servers in your environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-08"
reading_time_minutes: 3
keywords: [Oracle Analytics Server, Oracle BI Server, Oracle BI Presentation Service, Oracle BI Scheduler, Oracle Analytics Server discovery, Oracle Analytics Server patterns, Oracle Business Intelligence Enterprise Edition]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Oracle Analytics Server pattern-based discovery

Discovery and Service Mapping Patterns finds Oracle Analytics Server \(formerly Oracle Business Intelligence Enterprise Edition\) components on Windows and Linux servers in your environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Oracle Analytics Server consists of integrated components that provide business intelligence capabilities. The Discovery patterns discover three core components:

-   Oracle BI Server: Core analytics engine that processes queries and manages metadata
-   Oracle BI Presentation Service: Web-based user interface component that delivers visualizations and dashboards
-   Oracle BI Scheduler: Component that manages scheduled report generation and distribution

## Prerequisites

-   **Verify that the applications are up to date**

    Verify that the following applications are up to date:

    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Verify that the Oracle Analytics Server processes are running on target systems**

    Verify that the following Oracle Analytics Server processes are active on target systems:

    -   Windows:
        -   `sawserver.exe`
        -   `NQScheduler.exe`
        -   `nqsserver.exe`
    -   Linux:
        -   `sawserver`
        -   `nqscheduler`
        -   `nqsserver`
-   **Verify file system access permissions**

    Verify that the credentials used for discovery have read access to the following locations:

    -   Oracle BI installation directories
    -   `BI_ORACLE_HOME` environment variable location
    -   `bifoundation/version.txt` file within the Oracle BI installation
-   **Create credentials on the ServiceNow AI Platform**
    -   Windows: Configure Windows credentials. For more information, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
    -   Linux: Configure SSH credentials. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle Analytics Server patterns.

-   **Resources discovered by the Oracle BI Server pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Oracle BI Server instance.|
    |Version \[version\]|Version of the Oracle BI Server software.|
    |Installation directory \[install\_directory\]|File system path where the Oracle BI Server is installed.|

-   **Resources discovered by the Oracle BI Presentation Service pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Oracle BI Presentation Service instance.|
    |Version \[version\]|Version of the Oracle BI Presentation Service software.|
    |Installation directory \[install\_directory\]|File system path where the Oracle BI Presentation Service is installed.|

-   **Resources discovered by the Oracle BI Scheduler pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Oracle BI Scheduler instance.|
    |Version \[version\]|Version of the Oracle BI Scheduler software.|
    |Installation directory \[install\_directory\]|File system path where the Oracle BI Scheduler is installed.|


## CI relationships

The Oracle Analytics Server patterns create these relationships to support Oracle Analytics Server discovery.

-   **Relationship created by the Oracle BI Server pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Oracle BI Server \[cmdb\_ci\_oracle\_bi\_server\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\] or Linux Server \[cmdb\_ci\_linux\_server\]|

-   **Relationships created by the Oracle BI Presentation Service pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Oracle BI Presentation Service \[cmdb\_ci\_oracle\_bi\_presentation\_service\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\] or Linux Server \[cmdb\_ci\_linux\_server\]|

-   **Relationships created by the Oracle BI Scheduler pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Oracle BI Scheduler \[cmdb\_ci\_oracle\_bi\_scheduler\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\] or Linux Server \[cmdb\_ci\_linux\_server\]|


**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

