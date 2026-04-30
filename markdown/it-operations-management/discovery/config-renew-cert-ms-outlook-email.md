---
title: Configure for MS Outlook email notification certificate renewal
description: Set up email notification so when your certificates are about to expire, you will receive an email enabling you to automatically renew straight from the email.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-23"
reading_time_minutes: 1
breadcrumb: [Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure for MS Outlook email notification certificate renewal

Set up email notification so when your certificates are about to expire, you will receive an email enabling you to automatically renew straight from the email.

## Before you begin

Role required: pki\_admin or admin

## Procedure

1.  Navigate to **System Properties** &gt; **Email Properties**.

2.  Complete the forms for **Outbound Email Configuration** and **Inbound Email Configuration**.

    **Note:** For outbound email configuration, the **Email sending enabled** field must be clicked **Yes**. For the inbound email configuration, the **Email receiving enabled** field must be clicked **Yes**.

3.  Select **Update**

4.  Navigate to **All** &gt; **sys\_user.LIST**.

5.  Select **New**

6.  Complete the **Certificate Administrator** field.

    **Note:** For the **Active** field, make sure it’s selected.

7.  Select **Update**


## Result

Email notifications will go to the certificate adminstrator.

