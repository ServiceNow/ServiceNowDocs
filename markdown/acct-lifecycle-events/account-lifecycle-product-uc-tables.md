---
title: Supported use case table
description: The supported use case table \(sn\_prod\_cap\_core\_sup\_use\_case\) is the default implementation of the use case catalog. It extends the base use case table and adds classifies the industry verticals and business model segments relevant to the use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-product-uc-tables.html
release: australia
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [Reference, Customer Success Management]
---

# Supported use case table

The supported use case table \(`sn_prod_cap_core_sup_use_case`\) is the default implementation of the use case catalog. It extends the base use case table and adds classifies the industry verticals and business model segments relevant to the use case.

The supported use case table contains the following fields.

<table><thead><tr><th>

Field label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identifier with prefix SUC. Read-only.

</td></tr><tr><td>

Short description

</td><td>

Brief summary of the use case.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the use case.

</td></tr><tr><td>

Process flow

</td><td>

Rich-text description of the operational workflow.

</td></tr><tr><td>

Complexity

</td><td>

Implementation complexity.-   Very High
-   High
-   Medium
-   Low

</td></tr><tr><td>

Owner

</td><td>

User responsible for this use case. Defaults to the user creating the record.

</td></tr><tr><td>

Industry

</td><td>

Industry vertical. -   All
-   Manufacturing
-   Healthcare
-   Technology Services
-   Banking
-   Bio-Technology

This is a mandatory field.

</td></tr><tr><td>

Audience type

</td><td>

Business model segment. -   B2B
-   B2C
-   B2B2C
-   All

</td></tr><tr><td>

State

</td><td>

Current state.-   Draft
-   Retired
-   Cancelled

</td></tr><tr><td>

Active

</td><td>

System-managed. True when state is Published, false otherwise. Read-only.

</td></tr><tr><td>

Domain

</td><td>

Domain for multi-domain deployments.

</td></tr><tr><td>

Domain path

</td><td>

Domain path for multi-domain deployments.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Success Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-reference.md)

**Related topics**  


[Product use case catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-product-use-case.md)

[Customer Discovery Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-customer-discovery-hub.md)

