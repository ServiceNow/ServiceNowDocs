---
title: Create a KPI Configuration
description: Create a key performance indicator \(KPI\) that aggregates values from the Space table for use in the Space Planning module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-space-management/create-kpi-configuration.html
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 3
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

    For a description of the field values, see [KPI Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/kpi-configuration-form.md).

4.  Select **Submit**.

    The KPI Configuration record is saved and added to the **KPI Configurations** list.


## Result

A KPI Configuration record is created on the KPI Configuration \[sn\_wsd\_spcmgmt\_kpi\_configuration\] table. Active KPIs are evaluated against the Space \[sn\_wsd\_core\_space\] table and the calculated values appear in the Space Planning workspace.

For more information about the Space Planning workspace, see [Space Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/space-planning.md).

**Parent Topic:**[Managing workplace locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/Creating-workplace-location-records-using-spce-mgmt.md)

**Related topics**  


[Add a campus]()

[Add a building using Workplace Space Management]()

[Add a floor using Workplace Space Management]()

[Add an area using Workplace Space Management]()

[Add a room using Workplace Space Management]()

[Add a space using Workplace Space Management]()

[Allocate a cost center, department, or workplace entity]()

[Configure a workspace or desk as flexible or permanent]()

[Update the measurement details of a workplace location]()

[Change the status of a workplace location]()

[Configure a BOMA type]()

[Map a space type with BOMA type]()

[Create a Space Recommender rule]()

[Raise a space assistance request]()

[Create a view-by configuration]()

[Reviewing allocation changes]()

