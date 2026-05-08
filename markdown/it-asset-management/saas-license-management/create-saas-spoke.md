---
title: Create a custom spoke
description: To set up a custom integration in SaaS License Management, create a spoke to connect with a SaaS application.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a custom spoke

To set up a custom integration in SaaS License Management, create a spoke to connect with a SaaS application.

## Before you begin

Role required: admin

## About this task

-   Use ServiceNow® Studio to create a spoke. For more information about Studio, see ServiceNow Studio.
-   If a spoke exists for the SaaS application that you're integrating with, you can use the existing spoke instead of creating one. For a list of applications that have ServiceNow® Integration Hub spokes, see IntegrationHub available spokes.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**.

2.  Select **Create Application**.

3.  Give your app a name that includes the name of the SaaS application that you're integrating with and a description.

    Keep the auto-filled value for the **Scope** field.

4.  Select **Create**.

5.  Add the following roles and then select **Continue**.

    -   `admin`
    -   `sam_developer`
    -   `delegated_developer`
6.  Select the Classic format, then select **Continue**.

7.  Select **Done with tables**.

8.  To close the session and create your app, select **X**.

    **Tip:** Refresh the page to view the spoke app that you created in the list of apps.


## What to do next

As you continue building your custom integration, use the spoke to save the following items.

-   Connection &amp; Credential alias
-   Data stream actions to get users and user activity
-   Action to reclaim a user

If you’re publishing your custom spoke application on the ServiceNow Store, also use the spoke to save your subflows.

Create a custom integration profile to track software subscriptions and optimize stale licenses for any SaaS application. For more information, see [Create a custom integration profile](create-integration-custom.md).

