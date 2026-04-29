---
title: Enable Zoom chat integration
description: Enable the Zoom Team Chat feature on your ServiceNow instance by setting the related system properties.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Collaboration services for Zoom, ServiceNow for Zoom, Unified Employee Experience, Employee Service Management]
---

# Enable Zoom chat integration

Enable the Zoom Team Chat feature on your ServiceNow® instance by setting the related system properties.

## Before you begin

Ensure you have installed and set up the latest version of the Zoom spoke \(Zoom spoke v 4.0.3 or a higher version\) application and Collaboration services plugin \(sn\_tcm\_collab\_hook\) \(Collaboration services v 3.7.0 or a higher version\). 

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the Name search field of the System Properties \[sys\_properties\] table, enter `sn_tcm_collab_hook.enable_zoom_chat_integration`.

3.  Select the system property **sn\_tcm\_collab\_hook.enable\_zoom\_chat\_integration**.

4.  In the Value field, enter **true**.

    **Note:**

    The Value field entry is false by default.

5.  Set the Read roles value to **admin**.

6.  Select **Update**.


## Result

The Zoom Team Chat feature on the ServiceNow instance is enabled.

**Parent Topic:**[Configuring Collaboration services for Zoom](../concept/configure-sn-zoom.md)

