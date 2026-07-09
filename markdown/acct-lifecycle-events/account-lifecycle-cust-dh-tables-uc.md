---
title: Customer use case
description: The customer use case table \(sn\_cust\_disc\_hb\_cust\_use\_case\) is a per-customer record that documents how a specific customer plans to use a product to address a business need. It captures the customer's current process flow and specifies how their implementation aligns to one or more supported use cases from the product catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-cust-dh-tables-uc.html
release: australia
topic_type: reference
last_updated: "2026-06-29"
reading_time_minutes: 1
breadcrumb: [Customer Discovery Hub tables, Reference, Customer Success Management]
---

# Customer use case

The customer use case table \(`sn_cust_disc_hb_cust_use_case`\) is a per-customer record that documents how a specific customer plans to use a product to address a business need. It captures the customer's current process flow and specifies how their implementation aligns to one or more supported use cases from the product catalog.

The customer use case table extends the Base Use Case table \(`sn_prod_cap_core_base_use_case`\) and inherits several fields from it. It contains the following fields:

<table id="table_tb5_4cf_tjc"><thead><tr><th>

Field label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifier for this record. This field is automatically set with the prefix `CUC`.

</td></tr><tr><td>

Short description

</td><td>

Summary of the customer use case.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the customer use case.

</td></tr><tr><td>

Process flow

</td><td>

Description of the customer's workflow or scenario.

</td></tr><tr><td>

Complexity

</td><td>

Implementation complexity. Options: -   Very High
-   High
-   Medium
-   Low

</td></tr><tr><td>

Owner

</td><td>

User responsible for this use case.

</td></tr><tr><td>

State

</td><td>

Current state of the record. -   Draft
-   Published
-   Retired
-   Canceled

</td></tr><tr><td>

Active

</td><td>

Automatically set to True when the state is Published.

</td></tr><tr><td>

Account

</td><td>

Customer account associated with this record. Automatically populated from the parent business need.

</td></tr><tr><td>

Customer Business Need

</td><td>

Parent business need for this use case. This field displays only business needs associated with the selected account.

</td></tr><tr><td>

Alignment

</td><td>

Relates this use case to supported use cases in the product catalog. -   Out of the box
-   Extended
-   Custom

**Note:** When alignment is Out of the box or Extended, the customer use case is linked to one or more supported use cases. When alignment is Custom, no supported use cases are linked.

</td></tr><tr><td>

Work notes

</td><td>

Internal notes about this record.

</td></tr></tbody>
</table>Users with the following roles can view or edit this table:

|Role|Access|
|----|------|
|`sn_cust_disc_hb.discovery_viewer`|Read|
|`sn_cust_disc_hb.discovery_writer`|Read, write|

**Parent Topic:**[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

**Related topics**  


[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

[Manage engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-manage-engage.md)

