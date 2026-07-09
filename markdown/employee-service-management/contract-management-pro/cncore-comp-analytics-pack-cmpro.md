---
title: Components installed with Analytics Pack for Contract Management Pro
description: Several types of components are installed with activation of the Analytics Pack for Contract Management Pro plugin, including user roles and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-comp-analytics-pack-cmpro.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Contract Management Pro reference, Contract Management Pro, Employee Service Management]
---

# Components installed with Analytics Pack for Contract Management Pro

Several types of components are installed with activation of the Analytics Pack for Contract Management Pro plugin, including user roles and scheduled jobs.

## Roles

<table id="table_krl_dl3_w1c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Contracts PA Admin \[sn\_cm\_pa.pa\_admin\]

</td><td>

Provides the admin with permission to activate and configure the Analytics Pack for Contract Management Pro application.

</td><td>

Contract Report Publisher \[sn\_cm\_core.contract\_report\_publisher\]

</td></tr></tbody>
</table>## Scheduled jobs

<table id="table_mrl_dl3_w1c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contracts Core: Daily Data Collection

</td><td>

Collects analytics information for the indicators and breakdowns in the Contracts Dashboard.

 This job runs daily and populates the contract request data in the widgets of the dashboard.

</td></tr><tr><td>

Contracts Core: Monthly Data Collection

</td><td>

Collects analytics information for the indicators and breakdowns in the Contracts Dashboard.

 This job runs monthly and populates the contract request data in the widgets of the dashboard.

</td></tr><tr><td>

Contracts Core: Historical Data Collection

</td><td>

Provides an immediate insight from your existing contract request data.

 Run this job when you first activate Analytics Pack for Contract Management Pro or create indicators. When collecting data for the first time, the job generates scores and snapshots for existing records.

 For more information on running historical data collection jobs, see [Collect historical data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/t_RunHistoricalDataCollection.md).

</td></tr></tbody>
</table>**Note:** The jobs must be run in the following sequence:

1.  Contracts Core: Daily Data Collection
2.  Contracts Core: Monthly Data Collection
3.  Contracts Core: Historical Data Collection

**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Contract request State and Contract document status in Contract Management Pro]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

