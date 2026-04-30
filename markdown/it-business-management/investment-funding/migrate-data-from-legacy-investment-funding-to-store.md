---
title: Migrate data from legacy Investment Funding to Store application
description: With the admin role, you can migrate your existing data from the legacy Investment Funding tables to the new ServiceNow Store application tables by running the scheduled job.
locale: en-US
release: xanadu
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Upgrading legacy Investment Funding to Store application, Investment Funding, Strategic Portfolio Management]
---

# Migrate data from legacy Investment Funding to Store application

With the admin role, you can migrate your existing data from the legacy Investment Funding tables to the new ServiceNow Store application tables by running the scheduled job.

## Before you begin

Role required: admin

**Note:** Migrating data to the ServiceNow Store application tables is a one-time job, and not meant to be on a schedule.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and click the **Migrate Investment Funding To Store** scheduled job.

3.  On the Scheduled Script Execution form, ensure that the frequency is selected as **On Demand** in the **Run** field.

4.  Click **Execute Now**.


**Parent Topic:**[Upgrading legacy Investment Funding to Store application](../concept/upgrading-legacy-investment-funding-to-store.md)

