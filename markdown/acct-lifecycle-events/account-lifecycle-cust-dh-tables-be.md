---
title: Customer business expectation
description: The customer business expectation table \(sn\_cust\_disc\_hb\_business\_expectation\) captures a measurable success outcome tied to a customer business need. Expectations define what success looks like for the customer, including target values and success criteria.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-cust-dh-tables-be.html
release: australia
topic_type: reference
last_updated: "2026-06-29"
reading_time_minutes: 1
breadcrumb: [Customer Discovery Hub tables, Reference, Customer Success Management]
---

# Customer business expectation

The customer business expectation table \(`sn_cust_disc_hb_business_expectation`\) captures a measurable success outcome tied to a customer business need. Expectations define what success looks like for the customer, including target values and success criteria.

## Fields

The customer business expectation table contains the following fields:

<table id="table_dmc_qqf_tjc"><thead><tr><th>

Field label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifier for this record. This field is automatically set with the prefix `CBEX`.

</td></tr><tr><td>

Account

</td><td>

Customer account associated with this record. Auto-derived from the parent business need's lifecycle anchor. This field may be empty when no lifecycle anchor carries an account.

</td></tr><tr><td>

Customer Business Need

</td><td>

Parent business need. Only business needs in Draft or Qualified states are selectable.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the expectation.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the expectation.

</td></tr><tr><td>

Metric

</td><td>

The Performance Analytics indicator tracked by this expectation.

</td></tr><tr><td>

Unit

</td><td>

Unit of measure for the current and target values \(for example, percent, days, dollars\).

</td></tr><tr><td>

Current value

</td><td>

Latest observed value against the metric. Used to measure progress toward the target value.

</td></tr><tr><td>

Target value

</td><td>

Target value for the metric.

</td></tr><tr><td>

Start date

</td><td>

Start of the measurement window.

</td></tr><tr><td>

End date

</td><td>

End of the measurement window.

</td></tr><tr><td>

State

</td><td>

Current state: -   Draft
-   Qualified
-   Achieved
-   No Longer Required

</td></tr><tr><td>

Closure code

</td><td>

Required when the State is set to Achieved or No Longer Required. -   Achieved
-   Missed
-   Cancelled

</td></tr><tr><td>

Close notes

</td><td>

Required when the State is set to Achieved or No Longer Required.

</td></tr><tr><td>

Work notes

</td><td>

Running notes on this record.

</td></tr></tbody>
</table>**Note:** The lead, opportunity, and engagement fields are present on this table as read-only fields when the respective plugins are active. They are auto-populated from the parent business need and can't be edited.

The following user roles can view or modify this table:

|Role|Access|
|----|------|
|`sn_cust_disc_hb.discovery_viewer`|Read|
|`sn_cust_disc_hb.discovery_writer`|Read, write|

**Parent Topic:**[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

**Related topics**  


[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

[Manage engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-manage-engage.md)

