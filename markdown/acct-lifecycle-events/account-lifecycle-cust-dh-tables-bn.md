---
title: Customer business need
description: The customer business need table \(sn\_cust\_disc\_hb\_business\_need\) is the central record in Customer Discovery Hub. It captures the strategic problem a customer needs to solve and groups related challenges, expectations, and use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-cust-dh-tables-bn.html
release: australia
topic_type: reference
last_updated: "2026-06-29"
reading_time_minutes: 1
breadcrumb: [Customer Discovery Hub tables, Reference, Customer Success Management]
---

# Customer business need

The customer business need table \(`sn_cust_disc_hb_business_need`\) is the central record in Customer Discovery Hub. It captures the strategic problem a customer needs to solve and groups related challenges, expectations, and use cases.

The customer business need table contains the following fields:

<table id="table_icm_njf_tjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifier for this record. This field is automatically set with the prefix `CBNE`.

</td></tr><tr><td>

Account

</td><td>

Customer account associated with this record. Auto-derived from lead, opportunity, or engagement.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the business need.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the business need.

</td></tr><tr><td>

Lead

</td><td>

Lead record associated with this business need. At least one lifecycle anchor \(lead, opportunity, or engagement\) must be set. Present only when the Lead Management plugin is installed.

</td></tr><tr><td>

Opportunity

</td><td>

Opportunity record associated with this business need. At least one lifecycle anchor must be set. Present only when the Opportunity Management plugin is installed.

</td></tr><tr><td>

Engagement

</td><td>

Engagement record associated with this business need. At least one lifecycle anchor must be set. Present only when the Account Lifecycle plugin is installed.

</td></tr><tr><td>

State

</td><td>

The current state:-   Draft
-   Qualified
-   Closed
-   No longer required

</td></tr><tr><td>

Priority

</td><td>

This can be:-   Critical
-   High
-   Medium
-   Low \(default\)
-   Very low

</td></tr><tr><td>

Drivers

</td><td>

The business driver: -   Growth
-   Risk
-   Cost

</td></tr><tr><td>

Closure code

</td><td>

Required when State is Closed or No Longer Required. -   Achieved
-   Missed
-   Cancelled

</td></tr><tr><td>

Close notes

</td><td>

Required when State is Closed or No Longer Required.

</td></tr><tr><td>

Work notes

</td><td>

Work notes on this record.

</td></tr><tr><td>

Domain

</td><td>

Domain for multi-domain deployments.

</td></tr><tr><td>

Domain path

</td><td>

Domain path for multi-domain deployments.

</td></tr></tbody>
</table>The following roles can view or modify this table.

|Role|Access|
|----|------|
|`sn_cust_disc_hb.discovery_viewer`|Read|
|`sn_cust_disc_hb.discovery_writer`|Read, write|

**Parent Topic:**[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

**Related topics**  


[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

[Manage engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-manage-engage.md)

