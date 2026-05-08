---
title: Create a return to work case from an injury or illness
description: If an employee is returning to work after an injury or illness, create a return to work case to assess the employee's capability to work before they return.
locale: en-US
release: australia
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage incidents and observations, Manage incidents, observations, and anonymous safety concerns, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Create a return to work case from an injury or illness

If an employee is returning to work after an injury or illness, create a return to work case to assess the employee's capability to work before they return.

## Before you begin

Ensure that the following conditions are met:

-   The Health and Safety Case Management \(sn\_hs\_cm\) application is installed on your ServiceNow instance. For more information, see [Install Health and Safety Case Management](../../hs-case-management/task/install-hs-case-management.md).
-   The Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is not installed on your instance. For more information on activating it, see [Activate Case and Knowledge Management](../../human-resources/task/activate-case-and-knowledge-management-scoped.md).
-   **Employee** is selected in the **Person type** field on the injury and illness record. For more information, see [Injury and illness fields](../reference/hs-injury-illness-form.md).

Role required: sn\_ohs\_im.manager, sn\_ohs\_im.agent, or sn\_ohs\_im.operations\_manager, and sn\_hs\_cm.case\_manager

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the incident management icon \(![Incident Management icon.](../image/list-icon-hs.png)\) and navigate to the **Lists** tab.

3.  Open an injury and illness record to add the return to work case to.

<table id="choicetable_case"><thead><tr><th align="left" id="d138467e145">

Option

</th><th align="left" id="d138467e148">

Steps

</th></tr></thead><tbody><tr><td id="d138467e154">

**From a safety incident**

</td><td>

1.  In the **Safety Incidents** list, select **All**.
2.  In the list, select the incident that contains the injury and illness report to add the return to work case to.
3.  Select the **Report an incident** tab to open the playbook.
4.  In the **Add injury and illness** activity, select the injury and illness report to add the case to.


</td></tr><tr><td id="d138467e190">

**From an injury and illness list**

</td><td>

1.  In the **Injury / illnesses** list, open the list.
2.  In the list, open the injury and illness report that you want to add the return to work case to.


</td></tr></tbody>
</table>4.  Select **Create RTW case** and then select **Confirm**.


## Result

-   The return to work case is created and added to the **RTW case record** field on the injury form. For more information, see [Injury and illness fields](../reference/hs-injury-illness-form.md).
-   The injury and illness record is auto-populated in the **Injury and illness** tab of the return to work case. For more information, see [Health and Safety case](../../hs-case-management/task/hs-work-health-safety-case.md).

**Parent Topic:**[Managing Health and Safety incidents and observations](../concept/managing-hs-incidents-obs.md)

