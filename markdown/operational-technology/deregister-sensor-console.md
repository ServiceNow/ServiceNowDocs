---
title: Deregister a Discovery Sensor for OT
description: Deregister a Discovery Sensor for OT from the Discovery Console for OT that is no longer available on your system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/deregister-sensor-console.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Discovery Sensor for OT, Discovery Sensor for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Deregister a Discovery Sensor for OT

Deregister a Discovery Sensor for OT from the Discovery Console for OT that is no longer available on your system.

## Before you begin

Role required: admin

## Procedure

1.  In the Console, navigate to the Appliances page.

2.  From the list, select the Sensor that you want to deregister.

    The Sensor record opens.

3.  In the record, select the Actions icon.

4.  Select **Deregister** from the menu.

    When the Sensor is associated to a Site, you get a prompt.\[Omitted image "image.deregister-warning"\] Alt text: Deregistering

5.  If you select Continue in this window, you receive a prompt:

    \[Omitted image "image.second-deregister-warning"\] Alt text: Deregister Sensor?

6.  If you still intend to deregister the Sensor, select the **Deregister** button in this window.


## Result

The Sensor is deregistered, and the Sensor is reset to the default network configuration, which is the DHCP with the link-local fallback.

For removing a lost Sensor, see [Remove a lost Sensor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/remove-lost-sensor-console.md).

