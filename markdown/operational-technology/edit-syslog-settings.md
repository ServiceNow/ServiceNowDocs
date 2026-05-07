---
title: Edit Syslog settings
description: Edit the Syslog settings as needed to configure the Syslog server.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Settings page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Edit Syslog settings

Edit the Syslog settings as needed to configure the Syslog server.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the Settings page.

2.  Open the **Syslog** tab.

3.  Select **Edit**.

4.  On the form, edit the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Host|IP address of the Syslog host|
    |Port|Port that the host listens on. Typically port 514 for Syslog.|
    |Transport|Transport protocol used by the host. Typically, UDP.|
    |Facility|Descriptor used to indicate which process on the machine created for the Syslog event.|
    |Level|Desired Syslog severity level that's pushed to the receiving server.|
    |Audit Log Messages|If toggled on, enable Audit Log Messages.|

5.  Select **Save**.

    **Important:** Be sure to adjust any network firewall rules to open the specified Syslog port and protocol. Otherwise, traffic from the Discovery Console for OT can't reach the receiver application.


