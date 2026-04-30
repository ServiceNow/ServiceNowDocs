---
title: Create a custom spoke
description: To set up a custom integration in SaaS License Management, create a spoke to connect with a SaaS application.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SaaS License Connections, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Create a custom spoke

To set up a custom integration in SaaS License Management, create a spoke to connect with a SaaS application.

## Before you begin

Role required: admin

## About this task

If there's already a spoke for the SaaS application that you're integrating with, you can use the existing spoke instead of creating one. For a list of applications that have ServiceNow® Integration Hub spokes, see [IntegrationHub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

Use ServiceNow® Studio to create a spoke. For more information about Studio, see [ServiceNow Studio](https://www.servicenow.com/docs/access?context=c_ServiceNowStudio&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**.

2.  Click **Create Application**.

3.  Give your app a name that includes the name of the SaaS application that you're integrating with and a description.

    Keep the auto-filled value for the **Scope** field.

4.  Click **Create**.

5.  Add the roles `admin`, `sam_developer`, and `delegated_developer`, then click **Continue**.

6.  Select the Classic format, then click **Continue**.

7.  Click **Done with tables**.

8.  To close the session and create your app, click **X**.

    **Tip:** You may have to refresh the page to see your new spoke app in the list of apps.


## What to do next

As you continue building your custom integration, use the spoke to save the following items.

-   Connection &amp; Credential alias
-   Data stream actions to get users and user activity
-   Action to reclaim a user

If you are publishing your custom spoke application on the ServiceNow Store, also use the spoke to save your subflows.

**Parent Topic:**[SaaS License Connections](../concept/saas-license-connections.md)

**Previous topic:**[SaaS License Connections](../concept/saas-license-connections.md)

**Next topic:**[Create a custom integration profile](create-integration-custom.md)

