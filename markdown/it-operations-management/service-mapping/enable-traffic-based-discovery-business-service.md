---
title: Enable traffic-based discovery for an application service
description: Make Service Mapping use traffic-based connections to discover CIs making up an application service.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Enable traffic-based discovery for an application service

Make Service Mapping use traffic-based connections to discover CIs making up an application service.

## Before you begin

Role required: service\_mapping\_admin

## About this task

Service Mapping can discover and map configuration items \(CIs\) following their traffic-based connections. This method is referred to as traffic-based mapping and complements pattern-based mapping. For more information about how Service Mapping performs traffic-based discovery, see [Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md).

## Procedure

1.  In the classic environment, perform the following steps:

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home**.

        The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

    2.  Click **View Your Services** on the **Completed** tile.

    3.  Select the relevant application service.

    4.  Click **Additional Info**.

    5.  Click the **Traffic based discovery** check box.

    6.  Click **Update**.

2.  Alternatively, perform the following steps in the Agent Workspace UI:

    1.  Navigate to **Agent Workspace** &gt; **Agent Workspace Home**.

    2.  Click **Lists** in the left pane.

    3.  Navigate to **Services** &gt; **All Services**.

        The list of services displays services in Operational status.

    4.  Select the relevant application service.

    5.  Click the **Open Preview** icon.

        ![Open Preview icon next to the selected application service.](../image/workspace-all-services-open-preview.png)

        The Details pane opens on the right.

    6.  Click the **Traffic based discovery** check box in the Details pane.

    7.  Click **Update**.


**Parent Topic:**[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

