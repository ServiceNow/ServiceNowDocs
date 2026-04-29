---
title: Add sudo access for the Weblogic - Find config.xml probe
description: If you are not using the Weblogic pattern, you can add sudo privileges to the Linux, the Weblogic - Find config.xml probe.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [WebLogic application server, Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Add sudo access for the Weblogic - Find config.xml probe

If you are not using the Weblogic pattern, you can add sudo privileges to the Linux, the Weblogic - Find config.xml probe.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Probes**.

2.  Search for and select the **Linux - Weblogic - Find config.xml** probe.

3.  In the **Probe Parameters** related list, click**New**

4.  Use the following information to complete the form

    |Probe|Commands|
    |-----|--------|
    |Name|must\_sudo|
    |Value|true|

5.  Click **Submit**


**Parent Topic:**[WebLogic application server discovery](../concept/c_DataCollDiscoWebLogicServers.md)

