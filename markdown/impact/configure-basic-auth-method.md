---
title: Configure the Basic authentication method
description: Confirm an integration user, create a Basic authentication record, then connect your instances using basic authentication. Basic authentication is supported but OAuth is recommended for production environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-basic-auth-method.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Register your instance, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure the Basic authentication method

Confirm an integration user, create a Basic authentication record, then connect your instances using basic authentication. Basic authentication is supported but OAuth is recommended for production environments.

## About this task

**Important:**

Authentication record passwords use Key Management Framework \(KMF\) encryption, which is instance-specific. Any authentication record imported from another instance must have its password manually re-entered on the target instance. Neither `sn_se.scan_engine_admin` nor `sn_se.internal_rest_integration` is inherited by the platform admin role and both must be explicitly assigned on every instance.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Confirm the integration user account
2.  Confirm that the integration user account exists on all participating instances, has the `sn_se.internal_rest_integration` and `sn_se.scan_engine_admin` roles assigned, and that the account password is recorded in a secure location.

    If the account has not been created yet, complete [Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/task-create-integration-user.md) before continuing.

3.  Set the password using `setDisplayValue()` in a background script.

    **Note:** The Set Password UI modal does not support typing or pasting. Use the following script in **ALL** &gt; **System Definition** &gt; **Scripts - Background**:

    ```
    var gr = new GlideRecord('sys_user');
    gr.get('user_name', 'scan_engine_integration');
    gr.user_password.setDisplayValue('YourPassword');
    gr.update();
    ```

4.  Create a Basic authentication record
5.  Navigate to `sys_auth_profile_basic.list` and select **New**.

6.  Enter the same username and password as the integration user.

7.  Set **Application** to `Scan Engine` and save.

8.  Connect your instances
9.  Export the integration user record and basic auth record from the source instance, then import both into every target instance.

10. On each target instance, assign role `sn_se.internal_rest_integration` to the imported user.

    Role assignments are not included in record exports and must be added manually.

11. On each target instance, reset the integration user password using `setDisplayValue()` \(see script above\).

12. On each target instance, open the imported basic auth record and manually re-enter the password in the UI.

13. Create or import My SN Instances records and validate connections.

    See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md).


**Parent Topic:**[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md)

