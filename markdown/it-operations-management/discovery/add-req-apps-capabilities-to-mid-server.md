---
title: Add the required applications and capabilities to your MID Server
description: Enable your MID Server to auto-renew your certificates by adding the Certificate Inventory and Management and GenerateCSR applications.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring automated certificate renewal, Automated Certificate Renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Add the required applications and capabilities to your MID Server

Enable your MID Server to auto-renew your certificates by adding the Certificate Inventory and Management and GenerateCSR applications.

## Before you begin

Check that you have completed the task [Configure your MID Server for automatic certificate renewal](configure-mid-server-automatic-cert-renewal.md).

Role required: pki\_admin or admin

## About this task

Move the applications Certificate Inventory and Management and GenerateCSR from your collection list to your supported applications list.

## Procedure

1.  Navigate to **All** &gt; **Mid Servers**.

2.  Select the MID Server that you want to configure.

    **Note:** The MID Server must be the same MID Server that you configured for automated certificate renewal.

3.  Modify the MID Server

    1.  Select **Supported Applications**.

    2.  Select **Edit**.

    3.  Move **Certificate Inventory and Management** to the **Supported Applications List**.

    4.  Select **Save**.

    You’re redirected to the MID Server page.

4.  Add MID Server Capabilities

    1.  Select **Capabilities**.

    2.  Select **Edit**.

    3.  Move **GenerateCSR** from the **Collections List** to the **Supported Applications List**.

    4.  Select **Save**.

    You’re redirected to the MID Server page.


## Result

Your MID Server supports the Certificate Inventory and Management and GenerateCSR applications, fulfilling a requirement to enable automatic certificate renewal.

## What to do next

[Configure System Properties for automatic certificate renewal](config-sys-props-for-auto-cert-renewal.md), to complete the configuration for automatic certificate renewal.

