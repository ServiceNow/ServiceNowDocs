---
title: Gunicorn pattern-based discovery
description: Discovery and Service Mapping Patterns finds Gunicorn WSGI HTTP server instances running on Linux servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
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

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

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

    For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md#).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the GUNICORN pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Gunicorn instance, in the format `gunicorn@<hostname>`.|
|Version \[version\]|Version of the Gunicorn server.|
|Installation directory \[install\_directory\]|Installation directory of the Python environment containing Gunicorn.|
|TCP port\(s\) \[tcp\_port\]|TCP port or ports on which the Gunicorn server is listening.|

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

