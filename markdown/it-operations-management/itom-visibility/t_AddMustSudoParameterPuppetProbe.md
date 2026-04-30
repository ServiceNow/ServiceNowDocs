---
title: Add the must\_sudo parameter to the Puppet probe
description: To use the Puppet probe with sudo, you must add the must\_sudo parameter to each probe that requires it.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Puppet automation software, Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Add the must\_sudo parameter to the Puppet probe

To use the Puppet probe with sudo, you must add the **must\_sudo** parameter to each probe that requires it.

## Before you begin

Role required: admin

## About this task

You add the must\_sudo parameter for each Puppet probe.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Probes**.

2.  In the **Search** field, search on the name **Puppet**.

3.  Click the name of the probe.

    For example, **Puppet Master - Info**.

4.  In the **Related Links** pane, select the **Probe parameters** tab.

5.  Click **New**.

6.  In the **Name** field, enter `must_sudo`

7.  In the **Value** field, enter `true`.

8.  Click **Submit**.


**Parent Topic:**[Puppet automation software discovery](../concept/c_PuppetAutomationSoftwareDiscovery.md)

