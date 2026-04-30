---
title: Data capture and validation
description: This phase is meant to gather the necessary information about the account such as support contacts, locations, sold products, entitlements, and so on.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up the account onboarding playbook, Configuring account onboarding, Account onboarding, Customer Success Management]
---

# Data capture and validation

This phase is meant to gather the necessary information about the account such as support contacts, locations, sold products, entitlements, and so on.

<table id="table_ghf_3n4_1yb"><thead><tr><th>

Stage

</th><th>

Activity

</th></tr></thead><tbody><tr><td>

**Data Capture &amp; Validation**

</td><td>

In this task, select the type of activity being performed:

-   Data capture: Denotes important data being imported into the system.
-   Risk mitigation: Denotes a risk associated with the onboarding of this customer that must be managed.
-   Development: Tracks an internal or external development action that is required.
-   Training: Denotes a training activity required before the go-live date.
-   Testing: Denotes a testing activity required before the go-live date.

 The following default tables are available with the base system:

-   Customer contacts
-   Location
-   Service entitlement
-   Install base item
-   Account address relationship
-   Contract
-   Sold products
-   Install base M2M sold products

 Custom conditions have been defined and field values in these tables like source table, target table, and data source are auto populated in each of these tables. You can use these flows by directly importing data into these tables and publish them when they’re ready. For details on importing data into these tables, see [Import data into the account onboarding playbook](../task/account-lifecycle-import-data.md).

 These tables have been configured with specific conditions and field values have been auto populated. You can modify these tables, add new tables, and activities depending on your requirements using the Process Automation Designer. See [Configure data validation using the Data Validation Assist table](../task/account-lifecycle-data-valid-assist.md) for details.

</td></tr></tbody>
</table>Review the data in the Summary activity and click **Mark Complete** to move to the next stage.

