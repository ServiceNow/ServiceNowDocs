---
title: Configure email for feedback submission
description: Configure email settings in your instance and send an email to this id to create feedback.
locale: en-US
release: zurich
product: Product Feedback
classification: product-feedback
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Feedback, Strategic Planning, Strategic Portfolio Management]
---

# Configure email for feedback submission

Configure email settings in your instance and send an email to this id to create feedback.

## Before you begin

Role required: admin

## About this task

Configure email settings in your instance use it to send an email directly. With the **sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address** system property, you can configure email settings within your instance and submit feedback directly from your email account.

## Procedure

1.  Navigate to your instance.

2.  Navigate to **All** &gt; **System Properties** &gt; **Email Properties**.

3.  Update the email properties.

    1.  Set **Email sending enabled &amp; Email receiving enabled** to **Yes**.

    2.  Set **Automatically create users for incoming emails from trusted domains** to **Yes**.

        The default value for this field is **No**. You can select **Yes** to automatically create a user in the user table.

    3.  Select **Save**.

4.  Update the system properties list.

    1.  Navigate to **All** &gt; **System properties** &gt; **All properties** and search for **sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address** property.

    2.  Open the **sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address** property and enter your instance email id in the **Value** field.

        Any configured email account can be used.

5.  Select an existing email to forward as feedback or create feedback.

6.  Select **Send**.


**Parent Topic:**[Configuring Feedback application in Strategic Planning](../concept/configuring-product-feedback-in-sp.md)

