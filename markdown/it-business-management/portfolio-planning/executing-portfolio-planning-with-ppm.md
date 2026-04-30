---
title: Executing Portfolio Planning work in PPM
description: Facilitate execution of the work planned in Portfolio Planning in ServiceNow Project Portfolio Management application.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Portfolio Planning, Strategic Portfolio Management]
---

# Executing Portfolio Planning work in PPM

Facilitate execution of the work planned in Portfolio Planning in ServiceNow Project Portfolio Management application.

Import, export, and manage your planning items between Portfolio Planning and PPM.

![Real-time sync of planning items between Portfolio Planning and PPM.](../../apw-internal-integrations/images/planning-items.png "Integrating Portfolio Planning and PPM")

## Key benefits of Portfolio Planning with PPM

-   View available PPM planning items in Portfolio Planning.
-   Import planning items from PPM to Portfolio Planning.
-   Export planning items from Portfolio Planning to PPM.
-   Synchronize updates for linked planning items of Portfolio Planning with PPM.
-   Track the progress of the linked planning items in Portfolio Planning.

To get started on integrating Portfolio Planning with PPM, see [Configuring Portfolio Planning with PPM](configuring-portfolio-planning-with-ppm.md).

## Frequently asked questions about execution integration

-   **Can I use PPM Standard for project execution without Agile 2.0 or SAFe?**

    Yes. If your teams follow waterfall or traditional Project Management methodology, use PPM Standard \(Project Portfolio Management\) as your execution system. Planning items created in Portfolio Planning can be exported to PPM as projects. Changes in PPM \(project status, costs, resources\) sync back to Portfolio Planning automatically.

    Use case: Infrastructure team plans in Portfolio Planning, executes data-center migration project in PPM Standard with Gantt charts, task dependencies, and resource management.

-   **When do I use PPM for execution?**

    Base your decision on team methodology and org scale: PPM Standard: For waterfall projects, traditional PM teams, infrastructure work, conformance-driven initiatives.

-   **Should I install PPM Standard to use Portfolio Planning?**

    No. Install PPM Standard if your teams actually uses it. Portfolio Planning works standalone for planning and prioritization. Add the PPM plug-in when teams are ready to execute work in this system.

-   **What data syncs between Portfolio Planning and PPM?**

    Bi-directional sync includes:

    -   From Portfolio Planning → execution: Planning item name, description, owner, goals, budget, priority, timeline.
    -   From execution → Portfolio Planning: Status, progress %, actual costs, resource assignments, risks/issues.
    -   Real-time updates: Changes in either system appear in both within seconds.

## Common execution scenarios

Scenario: PPM only organization \(waterfall projects\)

1.  Portfolio managers create planning items in Portfolio Planning.
2.  After prioritization, export planning items to PPM Standard as projects.
3.  Project managers build WBS, create tasks, assign resources, manage timeline in PPM.
4.  Portfolio Planning shows project status, costs, risks automatically

## Troubleshoot execution integration

-   Issue: Planning item not appearing in PPM
    -   Verify the execution system plugin is installed and activated.
    -   Check that planning item state is Prioritized \(items in the Backlog state don't export\).
    -   Confirm user has required role in execution system \(project\_manager, scrum\_admin, safe\_admin\).
-   Issue: Changes in PPM not syncing back to Portfolio Planning
    -   Verify bi-directional sync is enabled in integration configuration.
    -   Check that the planning item and PPM project/epic are properly linked \(primary planning item field is populated\).
    -   Review transformation maps for any table, field, or choice mapping issues.

