---
title: Validate your EJBCA ACME base API URL
description: Validate that your base API URL for EJBCA ACME has been updated to your organization's root URL address.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACME integration with KeyFactor EJBCA, Automated Certificate Management Environment, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Validate your EJBCA ACME base API URL

Validate that your base API URL for EJBCA ACME has been updated to your organization's root URL address.

## Before you begin

Role required: discovery\_admin, Public Key infrastructure \(PKI\) admin, admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Certificate Management**.

2.  Select the **Certificate Records** tab.

3.  Select **Certificate Authority API URL**.

4.  Select **EJBCA ACME** in the table.


## Result

The UI is redirected to the certificate field and its Base URL.

## What to do next

Review the URL and confirm that it's not the standard default settings.

To connect with EJBCA, you must change the default URL to your specific environment \(env\) URL. If you still see the default setting, reconfigure your base API URL. For more information, see [Configure your base API URL for EJBCA ACME](configure-base-api-url-for-ejbca-acme.md).

