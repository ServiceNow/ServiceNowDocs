---
title: Configure a default MID Server for Service Mapping for upgraded deployments
description: In deployments upgraded to Istanbul or earlier, Service Mapping uses the default MID Server when it cannot find a MID Server with the matching IP range. Configuring a default MID Server improves the discovery process.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID Server configuration for Service Mapping, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure a default MID Server for Service Mapping for upgraded deployments

In deployments upgraded to Istanbul or earlier, Service Mapping uses the default MID Server when it cannot find a MID Server with the matching IP range. Configuring a default MID Server improves the discovery process.

## Before you begin

Role required: service\_mapping\_admin

Perform this procedure only for deployments upgraded to Istanbul or earlier. For fresh installs, perform Configure a default MID Server for each application.

Ensure that you know the name of the MID Server you want to configure as the default MID Server for Service Mapping.

## About this task

In upgraded deployments, Service Mapping selects a MID Server using a legacy algorithm:

-   Service Mapping chooses the MID Server whose application criteria is set to **ServiceMapping** or to **ALL**.
-   By default, Service Mapping selects the MID Server whose IP range matches the IP in the discovery request.
-   If Service Mapping cannot find a MID Server with the matching IP range and matching application, it assigns the discovery request to the default MID Server.
-   If there is no default MID Server and none of the MID Servers have IP ranges configured for them, Service Mapping uses a random MID Server.
-   If there is no default MID Server and no IP range matches the IP in the discovery request, Service Mapping cannot start the discovery process.

## Procedure

1.  Navigate to System Properties by entering `sys_properties.list` in the navigation filter.

2.  Click **New**.

3.  Configure values for the new property as follows:

    |Property|Description|
    |--------|-----------|
    |Name|Enter `mid.server.sm_default`.|
    |Description|Enter a free text description of the use of this MID Server.|
    |Type|Select **string**.|
    |Value|Enter the name of the MID Server you want to configure as the default for Service Mapping.|

4.  Click **Update**.


**Parent Topic:**[MID Server configuration for Service Mapping](../concept/configure-mid-service-mapping.md)

**Related topics**  


[MID Server configuration for Service Mapping](../concept/configure-mid-service-mapping.md)

