---
title: Activate Proactive Customer Service Operations with Event Management
description: Activate the Proactive Customer Service Operations with Event Management plugin to use Proactive Customer Service Operations with Event Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/activate-proactive-EM.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Proactive Customer Service, Extend capabilities, Configure, Customer Service Management]
---

# Activate Proactive Customer Service Operations with Event Management

Activate the Proactive Customer Service Operations with Event Management plugin to use Proactive Customer Service Operations with Event Management.

## Before you begin

Role required: admin

## About this task

Proactive Customer Service Operations with Event Management is only available for customers who are licensed for the Customer Service Management application.

To activate Proactive Customer Service Operations with Event Management, activate the Proactive Customer Service with Event Management plugin \(com.snc.proactive\_cs\_itom\). This plugin is not active by default.

Event management operators on new Customer Service Management installations now have a dedicated role \(sn\_pro\_cs\_ops.csm\_evt\_mgmt\_stakeholder\) to maintain access, gain visibility into cases, install base items, and customer contacts.

**Note:** Existing customers need not make any changes, this change only affects new setups.

**Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Activating this plugin also activates the Proactive Customer Service Operations \(com.snc.proactive\_cs\_ops\) and Event Management \(com.glideapp.itom.snac\) plugins.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the plugin com.snc.proactive\_cs\_itom.

3.  Click **Activate**.


