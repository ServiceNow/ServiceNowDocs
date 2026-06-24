---
title: Configure OAuth details
description: Edit OAuth field values, as required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/digital-end-user-experience-dex/configure-oauth-details.html
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 1
breadcrumb: [Setting up DEX Desktop Assistant, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Configure OAuth details

Edit OAuth field values, as required.

## Before you begin

Confirm you have set up the SSO provider and configure it in the instance to ensure its functionality.

Role required: sn\_dex\_desktop.admin

## Procedure

1.  In your instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  From the list, select **Desktop Assistant**.

    \[Omitted image "desktop-exp-application-registries.png"\] Alt text: Application Registries form where you can update OAuth details.

3.  On the form, edit the required fields.

    To learn about each field and the corresponding descriptions, see [Application Registries form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/digital-end-user-experience-dex/application-registries-form.md).

4.  Customize to avoid SSO Screen during logging in to DEX Desktop Assistant:

    1.  Include oauth\_login.do in the login\_url field.

    2.  Remove the client secret and save the page.

    **Note:** If the Login URL field doesn't appear on the form by default, select and hold \(or right-click\) the header, select **Configure** &gt; **Form Layout**, then add **Login URL**.

5.  Select **Update**.


## Result

The OAuth client application details are updated.

