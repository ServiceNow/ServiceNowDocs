---
title: Register an instance for cloning
description: Register your target instance before requesting your clone. OAuth authentication is the recommended method and requires a one-time setup per target instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/configure-target-instance.html
release: australia
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 1
keywords: [register instance, clone target, OAuth setup, basic authentication]
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Register an instance for cloning

Register your target instance before requesting your clone. OAuth authentication is the recommended method and requires a one-time setup per target instance.

## Before you begin

Role required: clone\_admin

**Tip:**

For OAuth-based registration \(recommended\), the target instance must run an OAuth-capable version of the Clone Admin Console. OAuth clone target authentication requires Australia Patch 5 or later on both the source and target instances. This registration method does not require admin credentials for each clone request.

## About this task

You can register a target instance from the Clone Admin Console or during a clone request. Registration creates a connection profile that identifies the target instance for cloning.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Navigate to **Configuration** &gt; **Clone instances**.

3.  Select **New**.

4.  In the **Target Instance** field, enter the target instance URL and select **Continue**.

    The system runs a version compatibility check to determine which authentication method to use.

5.  Choose an authentication method:

    -   **OAuth \(recommended\):** Select **Setup OAuth on Target** and follow the OAuth setup workflow. See [Set up OAuth authentication for a clone target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/setup-clone-oauth.md) for detailed steps.
    -   **Basic authentication \(fallback\):** If the target instance does not support OAuth, enter credentials for a user account with the clone\_admin and soap roles. Ensure the user's identity\_type is set to machine on the user record.
6.  Select **Save** or **Add Target** \(depending on authentication method\).

    The target instance is registered and ready for clone operations.


## Result

The target instance is configured and registered for cloning.

## What to do next

To submit a clone request to the registered target, see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md).

