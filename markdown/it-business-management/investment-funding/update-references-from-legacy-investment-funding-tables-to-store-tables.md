---
title: Update references from legacy Investment Funding tables to Store tables
description: Post migration of your legacy Investment Funding data, you must update the reference tables for the Investment and Funding Entity fields from the legacy Investment Funding tables to the ServiceNow Store application tables in the required tables.
locale: en-US
release: yokohama
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Upgrading legacy Investment Funding to Store application, Investment Funding, Strategic Portfolio Management]
---

# Update references from legacy Investment Funding tables to Store tables

Post migration of your legacy Investment Funding data, you must update the reference tables for the **Investment** and **Funding Entity** fields from the legacy Investment Funding tables to the ServiceNow Store application tables in the required tables.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Update the reference tables from the legacy Investment Funding tables to the Store application for the **Investment** and **Funding Entity** fields for the following tables.

    |Table|Column label \(Field\)|Reference table for the legacy Investment Funding plugin|Reference table for the Store application|
    |-----|----------------------|--------------------------------------------------------|-----------------------------------------|
    |Cost Plan|Investment|invst\_investment|sn\_invst\_pln\_invst\_investment|
    |Cost Plan|Funding Entity|invst\_investment\_entity|sn\_invst\_pln\_invst\_funding\_entity|
    |Benefit Plan|Investment|invst\_investment|sn\_invst\_pln\_invst\_investment|
    |Goal|Investment|invst\_investment|sn\_invst\_pln\_invst\_investment|


**Parent Topic:**[Upgrading legacy Investment Funding to Store application](../concept/upgrading-legacy-investment-funding-to-store.md)

