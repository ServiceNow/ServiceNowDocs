---
title: Remote Data Options for Remote Tables
description: Understand the different approaches of implementing remote tables, and the advantages and disadvantages of each.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Developer resources, Financial Services Operations \(FSO\)]
---

# Remote Data Options for Remote Tables

Understand the different approaches of implementing remote tables, and the advantages and disadvantages of each.

## Full Remote

In a full remote system, all account information \(accounts, insurance policies, and transactions\) is stored in an external system.

This configuration provides real-time information for customers that want financial accounts/policies to come directly from the source system when:

-   Looking at a customer record
-   Relating information to a case
-   Getting a 360 view of a customer; for example, in the Customer Information tab

<table id="table_mdp_w2j_mcc"><thead><tr><th>

Pros

</th><th>

Cons

</th></tr></thead><tbody><tr><td>

-   Provides a real-time aggregate view of account &amp; transaction information \(Customer 360\) for a single customer across multiple request types \(for example, Deposit/Loan accounts\)
-   The latest information always appears for fulfillers within the workspace
-   No sensitive data or Personally Identifiable Information \(PII\) is stored in the platform

</td><td>

-   No remote table data will be available on parent local tables, resulting in lost functionality with sold product/consumer/account
-   Updates are required on customer information \(C360\), record producers, forms, playbooks, reference fields, reference qualifiers, UI actions, scripts, and other areas to point from base system FSO tables to remote tables

</td></tr></tbody>
</table>## Hybrid

In a hybrid system, the system utilizes lookup and save functionality to query information from external systems and persist header-level information into local tables.

This functionality can be utilized in tandem with batches/real-time API calls to store certain data locally.

Customer 360 is possible in this view, but it may require additional strategies around batch uploads and API calls to populate the data. You must be willing to store certain information about external data in local tables in this configuration.

<table id="table_yvz_dgj_mcc"><thead><tr><th>

Pros

</th><th>

Cons

</th></tr></thead><tbody><tr><td>

-   Store only non-sensitive information in the system that is required and doesn’t change often
-   Use the base system FSO field lookup decorator to search &amp; persist data
-   The FSO Remote Table plugin can reduce development time if used with lookup and save functionality
-   Fully remote data that is presented on the record will be current

</td><td>

-   Data persisted onto local tables will become outdated if not refreshed - you must have a strategy to refresh data from the external system
-   An aggregate view of financial accounts/transactions for an account or consumer won’t be shown until information has been persisted \(if using lookup and save functionality\) or a batch/real-time API synchronization has been performed at runtime

</td></tr></tbody>
</table>## Full local

In a full local data storage architectural approach, all customer and account information \(customer, accounts, insurance policies\) is stored in FSO. This configuration provides faster access to information for customers who want financial accounts/policies to be refreshed from the source system on a periodic basis \(daily or at regular intervals throughout the day\).

You may find this approach useful when the use case does not rely on the most recent data and prioritizes reporting needs.

This approach helps with the following user actions:

-   Looking at a customer record
-   Relating information to a case
-   Getting a 360 view of a customer; for example, in the Customer Information tab

<table id="table_tvp_2z1_4cc"><thead><tr><th>

Pros

</th><th>

Cons

</th></tr></thead><tbody><tr><td>

-   Best suited for use cases that require less frequently changing information aggregate view
-   Information loaded into FSO is required for Reporting and dashboarding purposes
-   Easy to build Customer 360 for a single customer for different personas

</td><td>

-   Data persisted onto local tables will become outdated if not refreshed - you must have a strategy to refresh data from the external system
-   Users have to manually switch between tools \("swivel chair"\) for the most updated information
-   Additional solutions may be needed to secure PII data

</td></tr></tbody>
</table>