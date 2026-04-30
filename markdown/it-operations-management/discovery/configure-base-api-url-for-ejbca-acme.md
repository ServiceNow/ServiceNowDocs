---
title: Configure your base API URL for EJBCA ACME
description: Configure your base API URL for EJBCA ACME to your organization's root URL address.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-09-25"
reading_time_minutes: 1
breadcrumb: [Set up the routing policy for ACME, Configuring ACME, Automated Certificate Management Environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure your base API URL for EJBCA ACME

Configure your base API URL for EJBCA ACME to your organization's root URL address.

## Before you begin

Role required: discovery\_admin, Public Key infrastructure \(PKI\) admin, admin

## Procedure

1.  Navigate to **All** &gt; **Certificate Authorities**.

2.  In the table of certificate authorities, select **EJBCA ACME**.

3.  Edit the text in one of the following ways:

    -   Select **edit** text.
    -   Double-click \(or use the keyboard shortcut\)" the **Base URL** field.
    **Note:** If a warning message appears, you might be in the “Global” application. Select the link that appears to edit the record.

4.  Paste your own API URL over the `[ejbca_url]` text inside the URL.

5.  Make sure that the ACME option is selected.

6.  Select **Save**.


## Result

The base API URL for your EJBCA ACME environment is configured to your systems.

