---
title: Create synthetic monitoring locations
description: Create a synthetic monitoring location to run a synthetic monitor. If you plan to run monitors from a ServiceNow hosted location, you can skip this procedure.
locale: en-US
release: yokohama
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring synthetic monitoring, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Create synthetic monitoring locations

Create a synthetic monitoring location to run a synthetic monitor. If you plan to run monitors from a ServiceNow hosted location, you can skip this procedure.

## Before you begin

You need at least one of the following:

-   A MID Server
-   One or more Agent Client Collector \(ACC\) agent that monitors the health and performance of the HTTP endpoints to be monitored using synthetic monitoring. If you plan to run tests only from the ServiceNow hosted location, you don't need to set up a location.

    **Note:**

    -   If your synthetic monitor is testing a private HTTP endpoint, your location must only include ACC agents that are within the same network boundaries as the HTTP endpoint.
    -   If your monitor is testing an HTTP endpoint from different datacenters, cloud providers, or geographic regions, a different location must be used for each.

Role required: sn\_sow\_synthetics.synthetics\_admin

## About this task

Synthetic monitors can be hosted from:

-   A MID Server
-   A cluster of Agent Client Collector agents
-   A ServiceNow hosted location, as long as all monitored endpoints are publicly available. You don't need to configure a local instance as a location. It's available by default.

You can create as many locations as needed, but you must have at least one location to create a synthetic monitor.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Navigate to **Synthetic monitoring setup** &gt; **Manage Locations**.

3.  Select **Create a new location**.

4.  Expand the Location details card and enter a unique name and an optional description for this location.

    The description should clearly state where the servers or agents in this location are running. For example, `US-1-east-cluster`.

5.  In the **Location type** field, select either **MID Server** or **Agent Client Collector**, depending on where you want the monitor to be hosted.

6.  Expand the **Select** card and select one or more MID Servers or ACC agents.

7.  Select **Save**.

    **Note:** You can delete locations from the Synthetic Locations menu, which you can navigate to by selecting **All** &gt; **Synthetic Monitoring** &gt; **Synthetic Locations**. However, you must first remove any monitors running on that location, either by editing the monitors to use a different location or deleting the monitors. See [Create and edit a synthetic monitor](create-synthetic-monitor.md) for more information.


## What to do next

[Create and edit a synthetic monitor](create-synthetic-monitor.md)

**Parent Topic:**[Configuring synthetic monitoring](../concept/configuring-synthetic-monitoring.md)

