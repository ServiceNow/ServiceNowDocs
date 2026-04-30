---
title: Disable automated alarm closure for LogRhythm
description: Disable the automated alarm closure capability if you no longer want to view the security incident closure information on the LogRhythm Web Console. Once deactivated, the ServiceNow AI Platform no longer closes alarms within the LogRhythm Web Console. This process is optional.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional configurations, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Disable automated alarm closure for LogRhythm

Disable the automated alarm closure capability if you no longer want to view the security incident closure information on the LogRhythm Web Console. Once deactivated, the ServiceNow AI Platform no longer closes alarms within the LogRhythm Web Console. This process is optional.

## Before you begin

Role required: sn\_si.admin

## About this task

Once disabled, the status notes and other closure information on the security incident are no longer displayed on the LogRhythm Web Console.

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Business Rules** and select the **Business Rules** module.

2.  If not displayed in the **Business Rules** list, enter **LogRhythm Close Alarm On SI Closure** in the search field and press **Enter**.

    ![Business rule highlighted in search field.](../image/lr-bus-list-search.png)

3.  In the **Name** column, click the **LogRhythm Close Alarm On SI Closure** link to open the record.

4.  In the record that is displayed, clear the **Active** check box.

5.  Click **Update**.

    The automated alarm closure capability is now disabled.


**Parent Topic:**[Additional configurations for the LogRhythm integration](configure-system-and-troubleshooting-properties.md)

