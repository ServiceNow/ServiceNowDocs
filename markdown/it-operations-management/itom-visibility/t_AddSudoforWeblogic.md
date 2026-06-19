---
title: Add sudo access for the Weblogic - Find config.xml probe
description: If you are not using the Weblogic pattern, you can add sudo privileges to the Linux, the Weblogic - Find config.xml probe.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-visibility/t\_AddSudoforWeblogic.html
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-07-31"
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


**Parent Topic:**[WebLogic application server discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/c_DataCollDiscoWebLogicServers.md)

