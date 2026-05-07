---
title: Use schedule flows in Oracle Financial Cloud
description: Use the schedule flows to retrieve information from Oracle Financial Cloud, including Currencies, General Ledger \(GL\) accounts, Legal entities, Payment terms details from Oracle Financial Cloud.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Source-to-Pay integration with Oracle Financial Cloud, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use schedule flows in Oracle Financial Cloud

Use the schedule flows to retrieve information from Oracle Financial Cloud, including Currencies, General Ledger \(GL\) accounts, Legal entities, Payment terms details from Oracle Financial Cloud.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements. The Source-to-Pay with Oracle Financial Cloud integration supports the following subflows:

## Primary Data Integration with Oracle Financial Cloud

The Primary Data Integration with Oracle Financial Cloud integration supports the following subflows or actions:

|Subflow|Description|
|-------|-----------|
|Fetch Payment Terms|Use this subflow to fetch and synchronize all payment terms from Oracle Financial Cloud system.|
|Fetch Legal Entities|Use this subflow to fetch and synchronize all legal entities from Oracle Financial Cloud system.|
|Fetch Currencies|Use this subflow to fetch and synchronize all currencies from Oracle Financial Cloud system.|
|Fetch GL Accounts|Use this subflow to fetch and synchronize all GL Accounts from Oracle Financial Cloud system.|
|Fetch Purchase Groups|Use this subflow to fetch and synchronize all purchasing groups from Oracle Financial Cloud system.|
|Fetch Cost Center|Use this subflow to fetch and synchronize all cost centers from Oracle Financial Cloud system.|
|Fetch Purchasing Orgs|Use this subflow to fetch and synchronize all purchasing organizations from Oracle Financial Cloud system.|
|Fetch Plant Address|Use this subflow to fetch plant addresses from Oracle Financial Cloud system.|

**Important:**

These subflows are read only. To modify a flow or subflow, create a copy and then apply the required changes.

## Supplier Lifecycle Operations Integration with Oracle Financial Cloud

The Supplier Lifecycle Operations Integration with Oracle Financial Cloud supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or update supplier location|Creates or updates supplier location in Oracle Financial Cloud.|
|Create or update supplier payment information|Creates or updates supplier payment information in Oracle Financial Cloud.|
|Create, update or deactivate supplier|Creates or updates or deactivates supplier details in Oracle Financial Cloud.|

**Important:**

These subflows are read-only. To modify a flow or subflow, create a copy and then apply the required changes.

