---
title: Define and register a badge reader device manually
description: Manually create a badge reader device for registration in your system. Registering your badge reader enables you to make it operational at your Walk-up Experience on-site queue.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Walk-up Experience Badge Reader Integration setup and configuration, Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Define and register a badge reader device manually

Manually create a badge reader device for registration in your system. Registering your badge reader enables you to make it operational at your Walk-up Experience on-site queue.

## Before you begin

Role required: sn\_badge.badge\_admin

## About this task

There are two ways to define and register a badge reader device:

-   Manually through the ServiceNow AI Platform®.
-   As an assisted method through the **Badge Reader Client**. Refer to [Define and register a badge reader device using the badge reader client](assisted-config-badge-read-settings.md) for details on this procedure.

## Procedure

1.  To manually register your badge reader device, navigate to **Badge Reader Integration** &gt; **Badge Readers**.

2.  Click **New**.

3.  In the **Name** field, specify a name for the badge reader.

    For example, `Building B Tech Lounge Badge Reader`.

    **Note:** The **Status** field is read-only. This field is set to New when configuring a new badge reader. The field is in the Activated state when a badge reader is approved for activation. If a badge reader is deactivated, the field is set to Deactivated.

4.  Select a **Badge Event Handler**.

    **Note:** If no badge event handlers are available to select, create a new Badge Event Handler record. For details about this process, refer to [Create or modify Badge Reader Integration event handlers](create-or-modify-badge-event-handlers.md).

5.  Specify the **Device Identifier**.

    The Device Identifier uniquely identifies the badge reader hardware. The client defaults to using the badge reader device serial number. The value entered must match the device serial number received from the client software application.

    **Note:** The **Secret Key** field is automatically populated when you create the badge reader record.

6.  Select **User Badge Configuration**.

    The badge reader uses this mapping configuration to retrieve the user ID from the badge ID when the requester scans their badge to check in to a location.

    **Note:** By default, a user badge configuration is available to select. For more information on defining a new user badge configuration, see [Define a user badge configuration](define-user-badge-configuration.md).

7.  Specify the non-mandatory **Short description** and **Location** form fields if desired.

8.  Register the badge reader by selecting **Submit**.


**Parent Topic:**[Walk-up Experience Badge Reader Integration setup and configuration](../concept/walkup-badge-read-integ-config.md)

