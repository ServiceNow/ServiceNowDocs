---
title: Known error code form
description: The known error code form defines a known Service Exchange error and controls whether the system fixes it automatically when a connection goes down.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-known-error-code-form.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [known error code, tier, automatic mitigation]
breadcrumb: [Reference, Service Exchange]
---

# Known error code form

The known error code form defines a known Service Exchange error and controls whether the system fixes it automatically when a connection goes down.

<table id="table_kec_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tier

</td><td>

Option that controls whether the system fixes the known error automatically when a connection goes down.-   **Automatic**: The system runs the validation script and, if the error is detected, the mitigation script without admin action.
-   **Supervised**: The system doesn't fix the known error automatically.

If the field is empty, the system doesn't fix the known error automatically. This field is read-only. For more information, see [Automatic mitigation for connection issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation.md).

</td></tr><tr><td>

Validation script

</td><td>

Script that checks whether the known error is present on a connection. This field is read-only.

</td></tr><tr><td>

Mitigation script

</td><td>

Script that fixes the known error. The system runs it once when the validation script detects the error. This field is read-only.

</td></tr></tbody>
</table>**Related topics**  


[Automatic mitigation for connection issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation.md)

[Automatic mitigations for known errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-auto-mitigation-known-errors.md)

