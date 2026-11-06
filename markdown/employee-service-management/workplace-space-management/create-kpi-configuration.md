---
title: Create a KPI Configuration
description: Create a key performance indicator \(KPI\) that aggregates values from the Space table for use in the Space Planning module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/workplace-space-management/create-kpi-configuration.html
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Create a KPI Configuration

Create a key performance indicator \(KPI\) that aggregates values from the Space table for use in the Space Planning module.

## Before you begin

Role required: sn\_wsd\_spcmgmt.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Space Management** &gt; **Administration** &gt; **KPI Configuration**.

2.  On the KPI Configurations list, select **New**.

3.  On the KPI Configuration form, fill in the fields.

    For a description of the field values, see [KPI Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/kpi-configuration-form.md).

    If you set **Type** to SUM, AVG, or COUNT DISTINCT, you must also select a **Computation field**. You can't save two KPI configurations that have the same Type and Computation field.

4.  Select **Submit**.

    The KPI Configuration record is saved and added to the **KPI Configurations** list.


## Result

A KPI Configuration record is created on the KPI Configuration \[sn\_wsd\_spcmgmt\_kpi\_configuration\] table. Active KPIs are evaluated against the Space \[sn\_wsd\_core\_space\] table and the calculated values appear in the Space Planning workspace.

For more information about the Space Planning workspace, see [Space Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-central/space-planning.md).

The KPI appears on the details panel of the Space Planning workspace, in the order that you set in the **Order** field. For the KPIs that are installed by default, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/default-kpis-installed-with-workplace-space-mgmt.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/default-kpis-installed-with-workplace-space-mgmt.md). To change, deactivate, or delete a KPI, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/edit-kpi-configuration.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/edit-kpi-configuration.md).

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/edit-kpi-configuration.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/edit-kpi-configuration.md)

**Parent Topic:**[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/configurable-kpis-space-planning.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-space-management/configurable-kpis-space-planning.md)

