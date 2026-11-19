---
title: Create plan service configuration
description: Configure a plan service to associate workplace services and set scheduling conditions for a plan record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-maintenance-management/create-maint-service-config.html
release: zurich
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage plans, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Create plan service configuration

Configure a plan service to associate workplace services and set scheduling conditions for a plan record.

## Before you begin

The maintenance schedule must have an entry in the Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\) table for a plan record. Set conditions for a scheduling job to create maintenance cases for active plan records.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Preventive Maintenance** &gt; **Plan Service Configurations**.

2.  Select **New**.

3.  On the Workplace Maintenance Configuration form, fill in the fields:

    1.  Workplace service: Name of the Workplace service.

        Select the lookup list icon \(\[Omitted image "icon-lookup.png"\] Alt text: Lookup list icon.\) and workplace service for a plan record. For example: Cleaning desk.

        For more information, see [Create workplace services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/create-workplace-services.md).

    2.  Order: Integer-based value.

        The highest order value is prioritized. For example: 100.

    3.  Select the **Set conditions** filter and apply filter conditions for a selected item.

        For example, select **Schedule****is****Workplace cleaning**. The selected condition is applied to all plan records in a selected plan.

        \[Omitted image "wsd-schedule-conditions-plan-service-config.png"\] Alt text: Create plan service configuration.

        For more information about Workplace services, see [Create workplace services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/create-workplace-services.md).

        .

    4.  Select **Set**.

    5.  Expand **View matching results** to see services associated with a plan service configuration.

    1.  Select and open the **View matching results** to see the schedule job **Name****Next run time** or **Next run value** duration.

        \[Omitted image "wsd-meter-based-next-run-value.png"\] Alt text: View matching results showing the Next run value for a meter-based schedule.

        The selected schedule is updated in the Workplace Maintenance Service Configuration table and the schedule template is associated to it. If there’s a template associated to a schedule, it creates a workplace maintenance case.

        \[Omitted image "workplace-template-configuration-new.png"\] Alt text: Workplace template configuration form showing workplace service for a plan record.

        For more information, see [Workplace planned maintenance scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/sch-job-planned-nightly.md) and [Workplace maintenance cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/create-maint-cases.md).

4.  Select **Save**.

5.  The schedule job **Workplace Planned Maintenance Nightly Run** runs and creates maintenance cases for a workplace service in a plan record.

6.  Navigate to a published plan record.

7.  Select **Maintenance cases** in the calendar view.

8.  The Workplace Services column shows the plan service configuration associated with a plan record.

    \[Omitted image "wsd-published-maint-case-wiht-service.png"\] Alt text: Published maintenance plan showing mapped workplace services to a maintenance case.

    This record is updated in the Workplace Maintenance Service Configuration table.

    For more information, see [Workplace maintenance cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/create-maint-cases.md).


**Parent Topic:**[Manage Workplace Maintenance Management plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/manage-maintenance-plans.md)

**Previous topic:**[Create workplace services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/create-workplace-services.md)

**Next topic:**[Workplace Maintenance Management dashboard and analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-maintenance-management/workplace-maintenance-management-dashboard-overview.md)

