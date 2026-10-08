---
title: Automatic mitigations for known errors
description: Known errors with the Tier field set to Automatic are fixed without admin action when a Service Exchange connection goes down. Each fix changes specific records on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-auto-mitigation-known-errors.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [automatic mitigation, known error, automatic fix]
breadcrumb: [Reference, Service Exchange]
---

# Automatic mitigations for known errors

Known errors with the Tier field set to Automatic are fixed without admin action when a Service Exchange connection goes down. Each fix changes specific records on your instance.

<table id="table_auto_kecs"><thead><tr><th>

Known error

</th><th>

Detects

</th><th>

Fix

</th><th>

If the fix fails

</th></tr></thead><tbody><tr><td>

Inactive capture definitions

</td><td>

One or more Service Exchange capture definitions are inactive.

</td><td>

Activates the inactive capture definitions.

</td><td>

If a required capture definition is missing, the fix fails and the issue stays open.

</td></tr><tr><td>

Elevated privilege on RPS roles

</td><td>

Elevated privilege is turned on for one or more RPS roles.

</td><td>

Turns off elevated privilege on the RPS roles. **Note:** This fix changes role configuration without admin approval.

</td><td>

The issue stays open.

</td></tr><tr><td>

Inactive integration user

</td><td>

The integration user for the connection is inactive.

</td><td>

Reactivates the integration user. **Note:** This fix reactivates a user account without admin approval.

</td><td>

The issue stays open.

</td></tr><tr><td>

Integration user name doesn't start with sb\_user

</td><td>

The user name of the integration user for the connection doesn't start with `sb_user`.

</td><td>

Renames the integration user so that the user name starts with `sb_user`. **Note:** This fix changes a user account without admin approval.

</td><td>

The issue stays open.

</td></tr></tbody>
</table>Every fix is recorded in the work notes of the related issue. For details on when fixes run, see [Automatic mitigation for connection issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation.md).

**Related topics**  


[Automatic mitigation for connection issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation.md)

[Known error code form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-known-error-code-form.md)

[List of scan checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-list-of-scan-checks-in-sb.md)

