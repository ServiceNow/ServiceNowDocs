---
title: Updating the syslog settings
description: Update the Syslog settings as needed to configure the syslog server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/edit-syslog-settings.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Settings page, Using the Discovery Console, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Updating the syslog settings

Update the Syslog settings as needed to configure the syslog server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **Settings** page and open the **Syslog** tab.

2.  Select **Edit**.

3.  On the form, edit the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Host|IP address of the syslog host|
    |Port|Port that the host listens on. Typically port 514 for syslog.|
    |Transport|Transport protocol used by the host. Typically, UDP.|
    |Facility|Descriptor used to indicate which process on the machine created the syslog event.|
    |Level|Desired syslog severity level that's pushed to the receiving server.|
    |Audit Log Messages|If toggled on, enables Audit Log Messages.|

4.  Select **Save**.

    **Important:** Be sure to adjust any network firewall rules to open the specified syslog port and protocol. Otherwise, traffic from the Discovery Console for OT can't reach the receiver application.


