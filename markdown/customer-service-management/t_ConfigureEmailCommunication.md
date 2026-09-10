---
title: Configure an email address for a product
description: Configure an email address that creates a case for a specific product.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/t\_ConfigureEmailCommunication.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Email to case, Configure Email, Configure omnichannel, Configure, Customer Service Management]
---

# Configure an email address for a product

Configure an email address that creates a case for a specific product.

## Before you begin

Role required: admin

## About this task

Create a configuration that links a product to a specific email address. This configuration is created in the Channel Configuration \(sn\_customerservice\_channel\_config\) table.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Channels**.

2.  Select **New**.

3.  On the Channel Configurations form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the email configuration.|
    |Channel Type|Configuration type for this email address. Always **Email**.|
    |Product|Product model associated with this email configuration.|
    |Active|Option to activate the email configuration.|
    |Email address|One of the incoming email addresses created earlier in the Email Accounts application.|

4.  Select **Submit**.


