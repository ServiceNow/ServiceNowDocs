---
title: Exploring Workplace Maintenance Management
description: Workplace administrators and managers can create maintenance plans for preventive maintenance. Create duration or meter-based schedules for locations or assets. Associate different templates to your plan records to create maintenance cases.
locale: en-US
release: xanadu
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Exploring Workplace Maintenance Management

Workplace administrators and managers can create maintenance plans for preventive maintenance. Create duration or meter-based schedules for locations or assets. Associate different templates to your plan records to create maintenance cases.

You can create and manage maintenance plans for workplace models \(assets\) and location \(spaces\). Preventive maintenance cases are created in response to time elapsed or measured usage of an asset. For example: Coffee machines, elevators, lighting, and furniture.

Publish your maintenance plans and automate schedules to create maintenance cases for plan records. Maintenance cases are created in response to workplace issues where remedial work is required. For example: coffee spills, broken furniture, and so on.

Workplace agents are assigned maintenance cases to act on scheduled cases. Workplace agents can create, view, update, and delete maintenance cases.

## Benefits

Administrators and workplace managers can perform the following:

-   Create maintenance plans for workplace models \(assets\) and workplace locations.
-   Create schedules or copy an existing schedule for a maintenance plan.
-   Create duration-based or meter-based schedules.
-   Associate a template \(Workplace service\) to a plan record, maintenance plan, asset, or location. You can construct any condition on the Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\) table, and the template is assigned to a maintenance case when a condition is satisfied. Associate multiple templates across maintenance plans and also within maintenance plans.

    For example, maintenance plans created for printers for a location use Template A. Similarly, maintenance plans for office desks use Template B. To achieve further granularity within maintenance plans, you can assign different templates for different printer types or model types \(HP, Cannon, and so on\). You can also use a different template for different maintenance schedules \(daily, weekly, quarterly, and so on\).

-   Schedule job checks for an associated template and creates maintenance cases. It also pre-creates maintenance cases for plan records whose schedule is less than a day.
-   Track and monitor maintenance plan records and maintenance cases on Workplace Central.
-   Analyze metrics and trends to show preventive maintenance cases versus corrective maintenance cases. Administrators and workplace managers can take appropriate measures to reduce corrective maintenance issues. For example, sudden outages and printer breakdown. Create maintenance plans for your models and assets to reduce the volume of corrective cases. For more information, see [Workplace Maintenance Management dashboard and analytics](workplace-maintenance-management-dashboard-overview.md).

