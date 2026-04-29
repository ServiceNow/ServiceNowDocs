---
title: Set Alert Sources
description: Select Alert Sources to map corresponding incidents to a security incident. Alert Sources are refreshed every time a profile is opened and new rules are available for selection. The Cortex XSIAM integration supports multiple profiles.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set Alert Sources

Select Alert Sources to map corresponding incidents to a security incident. Alert Sources are refreshed every time a profile is opened and new rules are available for selection. The Cortex XSIAM integration supports multiple profiles.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you are not continuing from the previous section of the incident profile definition process, access the profile you are defining.

    1.  Navigate to **All** &gt; **Palo Alto Networks XSIAM** &gt; **XSIAM Profile**.

    2.  Select the profile you are continuing to define.

    3.  Select **Alert Sources** in the progress bar.

2.  Clear the **All Alert Sources** check box to select specific Alert Sources.

    Selecting this check box will retrieve all active Alert Sources from XSIAM.

3.  In the Alert Sources List search field, enter the Alert Source name created in the XSIAM portal.

4.  Select the Alert Source.

5.  Use the right arrow **\( &gt;\)** to move the rule from **Available** to **Selected** column.

    ![Set Alert Sources](../image/xsiam-alert-sources.png)

6.  Select **Continue**.


## What to do next

[Map incident fields](pan-cortex-xsiam-mapping.md)

