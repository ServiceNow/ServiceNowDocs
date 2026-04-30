---
title: Configure an email address for a product
description: Users with the system administrator role can configure an email address that creates a case for a specific product.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the email channel, Configure communication channels, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure an email address for a product

Users with the system administrator role can configure an email address that creates a case for a specific product.

## Before you begin

Role required: admin

## About this task

Create a configuration that links a product to a specific email address. This configuration is created in the Channel Configuration \(sn\_customerservice\_channel\_config\) table.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Channels**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the email configuration.|
    |Channel Type|This field displays the **Email** configuration type.|
    |Product|The product model associated with this email configuration.|
    |Active|The check box to activate the email configuration.|
    |Email address|The email address for this configuration. Enter one of the incoming email addresses that the system administrator created using the Email Accounts application.|

4.  Click **Submit**.


