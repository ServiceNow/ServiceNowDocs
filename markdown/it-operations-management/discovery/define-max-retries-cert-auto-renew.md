---
title: Define the maximum retries allowed for certificate auto-renewal
description: Use the system property sn\_disco\_certmgmt.auto\_renewal\_max\_retries to set the maximum retries your system enables for automatic certificate renewal.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-01-22"
reading_time_minutes: 1
breadcrumb: [Configuring automated certificate renewal, Automated Certificate Renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Define the maximum retries allowed for certificate auto-renewal

Use the system property sn\_disco\_certmgmt.auto\_renewal\_max\_retries to set the maximum retries your system enables for automatic certificate renewal.

## Before you begin

Role required: pki\_admin or admin

## About this task

If an automatic certificate renewal fails, the system will reattempt to renew the next day until it exhausts the maximum number of retries. Set this property to configure the maximum number of retries your system makes to renew your certificate.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for **auto\_renew**.

3.  Select**sn\_disco\_certmgmt.auto\_renewal\_max\_retries**

4.  Set the **Value** field to the maximum retries that you want.


