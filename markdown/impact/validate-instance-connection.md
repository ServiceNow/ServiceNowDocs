---
title: Validate your instance connection
description: Validate the connection between registered instances to confirm that authentication and My SN Instances configuration are correct before enabling integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/validate-instance-connection.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Register your instance, Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Validate your instance connection

Validate the connection between registered instances to confirm that authentication and My SN Instances configuration are correct before enabling integrations.

## Before you begin

My SN Instances registration and authentication must be complete before validating. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md) and either [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-basic-auth-method.md) or [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md).

Role required: `sn_se.scan_engine_admin`

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** &gt; **My SN Instances**.

2.  Open the instance record to validate.

3.  Select **Validate Connection**.

    Connection Status updates to `Connection Valid`, and the **Validated** checkbox is selected.


## What to do next

If validation fails, resolve the root cause before retrying. Retrying without fixing the root cause can trigger the account lockout policy. Work through the following checks in order:

1.  The integration user password was set using `setDisplayValue()` on this instance.
2.  The authentication record password was re-entered in the UI on this instance.
3.  Both roles: `sn_se.scan_engine_admin` and `sn_se.internal_rest_integration`, are explicitly assigned to the integration user on this instance.
4.  The instance URL is exactly `https://instancename.service-now.com` with no `www.`, trailing slash, or path.
5.  Any pending Scan Engine scripting scope request in Key Management Framework access policies has been approved, and you have logged out and back in before retrying. Complete [Grant Key Management Framework access on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/complete-kmf-access.md) on this instance first.

If the account has been locked out, see [Recover from account lockout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/recover-from-account-lockout.md).

**Parent Topic:**[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md)

