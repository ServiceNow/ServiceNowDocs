---
title: Choose MID Server selection algorithm
description: Service Mapping supports the new and the legacy algorithms for selecting a MID Server for a discovery request. Depending on your organization needs, you can choose which algorithm to enable.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Server configuration for Service Mapping, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Choose MID Server selection algorithm

Service Mapping supports the new and the legacy algorithms for selecting a MID Server for a discovery request. Depending on your organization needs, you can choose which algorithm to enable.

## Before you begin

Role required: admin or service\_mapping\_admin

## About this task

Service Mapping selects a MID Server using the following algorithm:

-   Service Mapping chooses the MID Server whose selection criteria best match the parameters of the discovery request.
-   If there are no MID Servers with matching selection criteria, Service Mapping chooses the default MID Server.
-   If there are no MID Servers with matching selection criteria or default MID Server, Service Mapping cannot start the discovery process.

By default, Service Mapping uses this algorithm in all fresh installs and deployments upgraded from Istanbul or Jakarta.

In upgraded deployments, Service Mapping selects a MID Server using a legacy algorithm:

-   Service Mapping chooses the MID Server whose application criteria is set to **ServiceMapping** or to **ALL**.
-   By default, Service Mapping selects the MID Server whose IP range matches the IP in the discovery request.
-   If Service Mapping cannot find a MID Server with the matching IP range and matching application, it assigns the discovery request to the default MID Server.
-   If there is no default MID Server and none of the MID Servers have IP ranges configured for them, Service Mapping uses a random MID Server.
-   If there is no default MID Server and no IP range matches the IP in the discovery request, Service Mapping cannot start the discovery process.

By default, Service Mapping uses the legacy algorithm in all deployments upgraded to Istanbul and earlier.

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Properties**.

2.  To enable the new algorithm for deployments upgraded to Istanbul and earlier:

    1.  Clear the **Enable Legacy MID selection algorithm** check box.

    2.  Click **Save**.

    3.  Configure MID Server selection criteria as described in [MID Server configuration for Service Mapping](../concept/configure-mid-service-mapping.md).

3.  To enable the legacy algorithm for the Australia deployment:

    1.  Select the **Enable Legacy MID selection algorithm** check box.

    2.  Click **Save**.

    3.  Configure MID Server selection criteria as described in [MID Server configuration for Service Mapping in upgraded deployments](../concept/MID-selection-criteria-upgrade.md).


**Parent Topic:**[MID Server configuration for Service Mapping](../concept/configure-mid-service-mapping.md)

