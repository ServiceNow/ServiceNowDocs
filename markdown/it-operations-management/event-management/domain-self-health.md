---
title: Monitor self-health with domain separation
description: Use domain separation to enable self-health to display Event Management health issues that are based on data, rules, and settings from the logged in user domain. The selected domain must not contain any child domains.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Self-health monitors for Event Management, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Monitor self-health with domain separation

Use domain separation to enable self-health to display Event Management health issues that are based on data, rules, and settings from the logged in user domain. The selected domain must not contain any child domains.

## Before you begin

Ensure that the Domain Support — Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) plugin is activated and that the MID Server you’re connecting to is configured for Event Management.

Role required: evt\_mgmt\_admin

## About this task

Self-health monitoring is domain aware. If the Domain Support — Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) plugin has been activated, then self-health displays health issues based on data, rules, and settings from the logged in user domain. If rules and settings aren’t defined for a child domain, then the settings of the parent are applied, recursively.

**Note:** To generate self-health monitoring events in the domain-separated instance, you must specify the domain of these generated events. This is done by specifying the `sys_id` of the required domain in the **evt\_mgmt.domain\_self\_monitoring** property.

When the Domain Support — Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) plugin isn’t activated, adding, or removing a connector or MID Server is immediately reflected in the map.

When the Domain Support — Domain Extension Installer \(com.glide.domain.msp\_extensions.installer\) plugin is activated, updates are done periodically according to the interval specifications of the Event Management — Insert Health Monitor scheduled job.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  In the **Schedule** list, locate and select the Event Management — Insert Health Monitor job.

3.  In the Event Management — Insert Health Monitor job, under Related Links, select **Configure Job Definition**.

4.  Set the required periodic update time in the **Repeat Interval** field by specifying the required values.

    The default interval is one hour.

    ![Self-health repeat interval](../image/self-health-repeat-interval.png)

5.  Select **Update**.


## Result

Further configuration is required for CI creation, receipt of events, and alert generation. The `sys_id` of the domain must be specified in the **Value** field of the **evt\_mgmt.domain\_self\_monitoring** property.

1.  Navigate to **System Properties** **All Properties**.
2.  Locate and select the **evt\_mgmt.domain\_self\_monitoring** property.

    ![Domain property sys_id value](../image/domain-sysid-value.png)

3.  In the **Value** field, specify the `sys_id` of the domain.
4.  Select **Update**.

**Parent Topic:**[Self-health monitors for Event Management](../concept/self-monitoring.md)

**Related topics**  


[Domain separation setup and basic administration](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

