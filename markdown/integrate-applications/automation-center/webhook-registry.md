---
title: Create UiPath webhook registry
description: Create UiPath webhook registries to establish a connection between UiPath and Automation Center.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring UiPath, Configure, Automation Center, Workflow Data Fabric]
---

# Create UiPath webhook registry

Create UiPath webhook registries to establish a connection between UiPath and Automation Center.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **UiPath** &gt; **UiPath Webhook Registries**.

2.  On the UiPath Webhook Registries form, select **New**.

3.  On the form, fill in the fields.

4.  Select **Submit**.

    The record is created.

5.  Open the record, select **Generate Callback URL** and **Secret**.

6.  Copy the URL and secret and paste it in the Webhook section of the UiPath Orchestrator.

7.  In the UiPath Orchestrator interface, select the events that you want to track.

    Currently, only **Job**, **Robot**, and **Process** events are supported.

8.  Select **Submit**.


## Result

The connection is set between UiPath and Automation Center. Whenever you send UiPath data to the instance, it happens via the URL provided. UiPath spoke validates the secret and accepts the data.

**Parent Topic:**[Configuring UiPath with Automation Center](../concept/uipath-config.md)

