---
title: Create an integration user account
description: Create a dedicated integration user account and assign the required roles so that the Scan Engine can authenticate and communicate between your ServiceNow instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/task-create-integration-user.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Create an integration user account

Create a dedicated integration user account and assign the required roles so that the Scan Engine can authenticate and communicate between your ServiceNow instances.

## Before you begin

Complete this procedure in every environment where the Scan Engine will run, for example, development, QA, and production.

Role required: admin \(to create users and assign roles\)

## About this task

The Scan Engine requires a dedicated integration user in each instance. The user's password is reused in several credential fields during integration setup, therefore, choose a value to store in a secure location before you begin.

**Tip:** To display the **Password** field on the user form, set the system property `glide.user.show.password.field` to `true` temporarily. You can revert this setting after setup is complete.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select **New**.

3.  In the **User ID** field, enter a name for the account \(for example, `integration.account`\).

    Fill in the remaining fields as your organization requires. The user ID and password are the only values that directly affect Scan Engine connectivity.

4.  Set a password that you can retrieve later.

    You will enter this same password as the integration client secret and in the integration user profile. Record it in a secure location before proceeding.

5.  Select **Save**.

6.  On the user record, scroll down to the **Roles** related list and select **Edit**.

7.  Search for `sn_se` and add both of the following roles to the user:

    -   `sn_se.internal_rest_integration` – Internal REST Integration
    -   `sn_se.scan_engine_admin` – Scan Engine Admin
8.  Select **Save**.

9.  Repeat this procedure in each additional instance, QA, production, etc., using the same user ID and password.

    Optional: Set the user **Type** to **Machine** or enable **Internal Integration User**. These settings do not affect Scan Engine connectivity but may align with your organization's security policies.


## Result

The integration user account exists in all required instances with the `sn_se.internal_rest_integration` and `sn_se.scan_engine_admin` roles assigned. You are ready to set up the integration authentication.

## What to do next

Proceed to [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md)

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md)

