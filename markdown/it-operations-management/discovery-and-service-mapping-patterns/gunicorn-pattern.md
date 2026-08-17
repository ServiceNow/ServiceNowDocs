---
title: Gunicorn pattern-based discovery
description: Discovery and Service Mapping Patterns finds Gunicorn WSGI HTTP server instances running on Linux servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/gunicorn-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-16"
reading_time_minutes: 1
keywords: [Gunicorn, WSGI, Gunicorn discovery, Gunicorn patterns, Green Unicorn]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Gunicorn pattern-based discovery

Discovery and Service Mapping Patterns finds Gunicorn WSGI HTTP server instances running on Linux servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Verify Gunicorn is installed and running on the Linux server**

    Verify the Gunicorn software is installed and running on a Linux server. The Gunicorn process must be active at the time of discovery.

-   **Verify `sudo` access to run network commands**

    Verify the discovery credentials have permission to run the following command: `sudo netstat -tulnp`.

-   **Create SSH credentials**

    For more information, see [SSH credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/r_SSHCredentialsForm.md).

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the GUNICORN pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Gunicorn instance, in the format `gunicorn@<hostname>`.|
|Version \[version\]|Version of the Gunicorn server.|
|Installation directory \[install\_directory\]|Installation directory of the Python environment containing Gunicorn.|
|TCP port\(s\) \[tcp\_port\]|TCP port or ports on which the Gunicorn server is listening.|

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

