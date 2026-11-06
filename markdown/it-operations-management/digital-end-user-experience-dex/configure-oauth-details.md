---
title: Configure Open Authorization details
description: Edit the Open Authorization \(OAuth\) field values to update OAuth client application details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/configure-oauth-details.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Setting up Desktop Assistant, Configure, Digital End-User Experience, IT Operations Management]
---

# Configure Open Authorization details

Edit the Open Authorization \(OAuth\) field values to update OAuth client application details.

## Before you begin

The SSO provider must be set up and configured in the instance.

Role required: sn\_dex\_desktop.admin

## Procedure

1.  In your instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  From the list, select **Desktop Assistant**.

3.  On the Application Registries form, edit the required fields.

    For a description of the field values, see [Application Registries form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/application-registries-form.md).

4.  Customize the registry to skip the SSO screen when you log in to DEX Desktop Assistant:

    1.  Include `oauth_login.do` in the **Login URL** field.

    2.  Remove the client secret and save the page.

    **Note:** If the Login URL field doesn't appear on the form by default, select and hold \(or right-click\) the header, select **Configure** &gt; **Form Layout**, then add **Login URL**.

5.  Select **Update**.


