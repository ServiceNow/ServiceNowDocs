---
title: Validate your instance connection
description: Validate the connection between registered instances to confirm that authentication and My SN Instances configuration are correct before enabling integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/validate-instance-connection.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Register your instance, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Validate your instance connection

Validate the connection between registered instances to confirm that authentication and My SN Instances configuration are correct before enabling integrations.

## Before you begin

My SN Instances registration and authentication must be complete before validating. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md) and either [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-basic-auth-method.md) or [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md).

Role required: `sn_se.scan_engine_admin`

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** &gt; **My SN Instances**.

2.  Open the instance record to validate.

3.  Select **Validate Connection**.

    Connection Status updates to `Connection valid`.


## What to do next

If validation fails, resolve the root cause before retrying. Retrying without fixing the root cause can trigger the account lockout policy. Work through the following checks in order:

1.  The integration user password was set using `setDisplayValue()` on this instance.
2.  The authentication record password was re-entered in the UI on this instance.
3.  Both roles — `sn_se.scan_engine_admin` and `sn_se.internal_rest_integration` — are explicitly assigned to the integration user on this instance.
4.  The instance URL is exactly `https://instancename.service-now.com` with no `www.`, trailing slash, or path.
5.  Any pending Scan Engine scripting scope request in Key Management Framework access policies has been approved, and you have logged out and back in before retrying.
    1.  Assign the system administrator role the Key Management admin role
    2.  Assign the sn\_kmf.cryptographic\_manager role to the system admin.
    3.  Navigate to **All** &gt; **Key Management** &gt; **Module Access Policies**.
    4.  Search for Scan Engine in the Script Table Target script: Script Include: ScanEngineApiUtil\[Omitted image "scan-engine-kmf-reject-map-fix.png"\] Alt text: Scan Engine in the Script Table Target script Script Include: ScanEngineApiUtil
    5.  Open the record and set the Result to **Track**.

If the account has been locked out, see [Recover from account lockout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/recover-from-account-lockout.md).

**Parent Topic:**[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md)

