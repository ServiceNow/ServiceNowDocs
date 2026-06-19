---
title: Create an operational success dashboard
description: Create a KPI category and map with the operational dashboard to view the performance of the ITSM processes in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/itsm-success-dashboard-indicators/create-operational-success-dashboard.html
release: australia
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Operational Success Admin Console, Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# Create an operational success dashboard

Create a KPI category and map with the operational dashboard to view the performance of the ITSM processes in your organization.

## Before you begin

Role required: sn\_sd.success\_dashboard\_admin

## Procedure

1.  In the navigation list, enter `sn_sd_kpi_category.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the KPI category.|
    |Dashboard type|Dashboard type of the new KPI category that is to be associated.|
    |Order|Order of the dashboard.|

4.  Select **Submit**.

5.  In the navigation list, enter `sn_sd_tab_m2m_dashboard.list`.

6.  Select **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Tab|Unique name of the dashboard.|
    |PAR Dashboard|The PAR dashboard that must be associated with the Operational success tab.|
    |Order|Order of the dashboard.|

8.  Select **Submit**.


## Result

The new dashboard appears on the Operational success dashboard.

**Parent Topic:**[Operational Success Admin Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-success-dashboard-indicators/admin-console-os.md)

