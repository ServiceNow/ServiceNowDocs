---
title: Installing Proactive Triggers
description: Enable Proactive Triggers so that you can begin working with the feature.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Installing Proactive Triggers

Enable Proactive Triggers so that you can begin working with the feature.

## Before you begin

The Proactive Triggers feature \[sn\_pt\] is available as an app and must be installed from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). This feature is only available after you've installed and updated the Omni-Experience Standard Feature Set to the latest version through the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Role required: admin

## About this task

The following steps provide a high-level overview of how to enable Proactive Triggers.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **General**.

2.  Under Proactive triggers, select the [Enable Proactive Triggers](enable-proactive-triggers.md) field toggle switch to enable the feature.

3.  Set the com.glide.cs.advanced-chat-popover system property to **true** in the System Properties \[sys\_properties\] table.

    This system property is only applicable to the requester persona.


