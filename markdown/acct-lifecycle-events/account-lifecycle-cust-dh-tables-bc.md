---
title: Customer business challenge
description: The customer business challenge table \(sn\_cust\_disc\_hb\_business\_challenge\) stores a specific pain point, gap, or enhancement request that a customer has expressed. Challenges are triaged and linked to a customer business need when qualified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-cust-dh-tables-bc.html
release: australia
topic_type: reference
last_updated: "2026-06-29"
reading_time_minutes: 1
breadcrumb: [Customer Discovery Hub tables, Reference, Customer Success Management]
---

# Customer business challenge

The customer business challenge table \(`sn_cust_disc_hb_business_challenge`\) stores a specific pain point, gap, or enhancement request that a customer has expressed. Challenges are triaged and linked to a customer business need when qualified.

The customer business challenge table contains the following fields.

<table id="table_yl4_pnf_tjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifier for this record. This field is automatically set with the prefix `CBCH`.

</td></tr><tr><td>

Account

</td><td>

Customer account associated with this record. Auto-derived from the set lifecycle anchor.

</td></tr><tr><td>

Short description

</td><td>

Summary of the challenge.

</td></tr><tr><td>

Description

</td><td>

Full description of the challenge.

</td></tr><tr><td>

Type

</td><td>

Category of the challenge. -   Pain Point
-   Gap
-   Enhancement

</td></tr><tr><td>

Priority

</td><td>

Urgency level of the challenge. -   Critical
-   High
-   Medium
-   Low \(default\)
-   Very Low

</td></tr><tr><td>

Lead

</td><td>

Lead record associated with this challenge. Present only when the Lead Management plugin is installed.

</td></tr><tr><td>

Opportunity

</td><td>

Opportunity record associated with this challenge. Present only when the Opportunity Management plugin is installed.

</td></tr><tr><td>

Engagement

</td><td>

Engagement record associated with this challenge. Present only when the Account Lifecycle plugin is installed.

</td></tr><tr><td>

State

</td><td>

Current state:-   Draft
-   Qualified
-   Not Qualified
-   No Longer Required

</td></tr><tr><td>

Customer Business Need

</td><td>

Parent business need linked to this challenge. This field appears only when the challenge is qualified.

</td></tr><tr><td>

Closure code

</td><td>

Reason the challenge was closed. This field appears only when the state is Not Qualified or No Longer Required. -   Not Valid
-   Duplicate
-   Cancelled

</td></tr><tr><td>

Close notes

</td><td>

Notes explaining why the challenge was closed. This field appears only when the state is Not Qualified or No Longer Required.

</td></tr><tr><td>

Work notes

</td><td>

Internal notes on this record.

</td></tr><tr><td>

Domain

</td><td>

Domain assigned to this record in a multi-domain deployment.

</td></tr><tr><td>

Domain path

</td><td>

Domain path for this record in a multi-domain deployment.

</td></tr></tbody>
</table>User roles that can view or modify this table.

|Role|Access|
|----|------|
|`sn_cust_disc_hb.discovery_viewer`|Read|
|`sn_cust_disc_hb.discovery_writer`|Read, write|

**Parent Topic:**[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

**Related topics**  


[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

[Manage engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-manage-engage.md)

