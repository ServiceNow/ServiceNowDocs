---
title: Configure Open Authorization details
description: Edit the Open Authorization \(OAuth\) field values to update OAuth client application details.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Configure Open Authorization details

Edit the Open Authorization \(OAuth\) field values to update OAuth client application details.

## Before you begin

Verify that you have set up the SSO provider and configure it in the instance to ensure its functionality.

Role required: sn\_dex\_desktop.admin

## Procedure

1.  In your instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  From the list, select **Desktop Assistant**.

3.  On the Application Registries form, edit the required fields.

    For a description of the field values, see [Application Registries form](../reference/application-registries-form.md).

4.  Customize to avoid SSO Screen when logging in to DEX Desktop Assistant:

    1.  Include oauth\_login.do in the login\_url field.

    2.  Remove the client secret and save the page.

    **Note:** If the Login URL field doesn't appear on the form by default, select and hold \(or right-click\) the header, select **Configure** &gt; **Form Layout**, then add **Login URL**.

5.  Select **Update**.


