---
title: Recover from account lockout
description: Unlock the integration user account and clear the password reset flag after repeated failed validation attempts trigger the account lockout policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/recover-from-account-lockout.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [Register your instance, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Recover from account lockout

Unlock the integration user account and clear the password reset flag after repeated failed validation attempts trigger the account lockout policy.

## Before you begin

Role required: admin

## About this task

Repeated failed connection validation attempts can lock the integration user account. Two fields must be cleared to restore access — `locked_out` and `password_needs_reset`. Clearing only one field is insufficient; `password_needs_reset` can independently block authentication even when `locked_out` is false.

## Procedure

1.  Navigate to **ALL** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Run the following script, replacing `scan_engine_integration` with your integration user's user name if different.

    ```
    var gr = new GlideRecord('sys_user');
    gr.get('user_name', 'scan_engine_integration');
    gr.setValue('locked_out', false);
    gr.setValue('password_needs_reset', false);
    gr.update();
    ```


## Result

The integration user account is unlocked and the password reset flag is cleared.

## What to do next

Before retrying validation, resolve the root cause of the failed attempts. See [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/validate-instance-connection.md) for the full validation troubleshooting checklist.

**Parent Topic:**[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md)

