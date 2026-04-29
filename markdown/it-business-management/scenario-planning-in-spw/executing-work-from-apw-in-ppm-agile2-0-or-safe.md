---
title: Strategic Planning with PPM, Agile 2.0, and SAFe
description: Facilitate execution of the work planned in Strategic Planning in ServiceNow applications such as Project Portfolio Management \(PPM\), Agile Development 2.0, or Scaled Agile Framework.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [PPM integration with Strategic Planning, SAFe execution from alignment planner, Agile 2.0 delivery, epic delivery in SAFe, strategic planning to PPM sync, planning to execution integration]
breadcrumb: [Explore, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Strategic Planning with PPM, Agile 2.0, and SAFe

Facilitate execution of the work planned in Strategic Planning in ServiceNow applications such as Project Portfolio Management \(PPM\), Agile Development 2.0, or Scaled Agile Framework.

While planning personas like portfolio managers or product owners use Strategic Planning to align their plans with the business objectives, they can provide flexibility to the execution teams to decide how they deliver their work.

Teams can choose the methodology that would be the most effective for them, and decide on the execution system that would best fit their needs. They can use applications such as ServiceNow® Project Portfolio Management, Agile Development 2.0, or Scaled Agile Framework \(SAFe\) to execute the work planned by their managers.​

With this flexible approach of delivering work, empower your teams to deliver more value, while being able to fund, manage, and monitor all work from a single workspace.

![The real-time bi-directional sync of information between Strategic Planning and PPM, Agile Development 2.0, and SAFe.](../images/spw-integration.png "Strategic Planning integration with ServiceNow applications")

## Key benefits of Strategic Planning with PPM, Agile 2.0, and SAFe

-   View available PPM, Agile 2.0, and SAFe planning items in Strategic Planning.
-   Import planning items from PPM, Agile 2.0, or SAFe to Strategic Planning.
-   Export planning items from Strategic Planning to PPM, Agile 2.0, or SAFe.
-   Synchronize updates for linked planning items of Strategic Planning with PPM, Agile 2.0, and SAFe.
-   Track the progress of the linked planning items in Strategic Planning.

To get started on integrating Strategic Planning with PPM, Agile 2.0, and SAFe, see [Configuring Strategic Planning with PPM, Agile 2.0, and SAFe](configuring-apw-with-agile-safe-and-ppm.md).

## Frequently asked questions about execution integration

-   **Can I use PPM Standard for project execution without Agile 2.0 or SAFe?**

    Yes. If your teams follow waterfall or traditional Project Management methodology, use PPM Standard \(Project Portfolio Management\) as your execution system. Planning items created in Strategic Planning can be exported to PPM as projects. Changes in PPM \(project status, costs, resources\) sync back to Strategic Planning automatically.

    Use case: Infrastructure team plans in Strategic Planning, executes data-center migration project in PPM Standard with Gantt charts, task dependencies, and resource management.

-   **How do I decide between PPM, Agile 2.0, and SAFe for execution?**

    Base your decision on team methodology and org scale:

    -   PPM Standard: For waterfall projects, traditional PM teams, infrastructure work, conformance-driven initiatives.
    -   Agile 2.0: For single scrum teams, small agile projects, product development teams under 50 people.
    -   SAFe: For enterprise-scale agile, multiple Agile Release Trains \(ARTs\), large programs with 50+ team members, portfolio-level coordination.
    Hybrid approach: Many organizations use multiple execution systems. Marketing team uses Agile 2.0 for campaigns, IT uses PPM for infrastructure, product engineering uses SAFe for platform development—all visible in one Strategic Planning view.

-   **Should I install all three execution systems to use Strategic Planning?**

    No. Install only the execution systems your teams actually use. Strategic Planning works standalone for planning and prioritization. Add PPM, Agile Development 2.0, or SAFe plug-ins when teams are ready to execute work in those systems.

-   **What data syncs between Strategic Planning and execution systems?**

    Bi-directional sync includes:

    -   From Strategic Planning → execution: Planning item name, description, owner, goals, budget, priority, timeline.
    -   From execution → Strategic Planning: Status, progress %, actual costs, resource assignments, risks/issues.
    -   Real-time updates: Changes in either system appear in both within seconds.
-   **Can a single planning item be executed in multiple systems?**

    No. Each planning item links to a single execution system. However, you can break down a large initiative into child planning items, each executed in different systems. For example, the Digital Transformation Initiative parent planning item contains: Mobile App Redesign \(Agile 2.0\), Legacy System Migration \(PPM\), and API Platform Modernization \(SAFe\).


## Common execution scenarios

-   Scenario 1: PPM only organization \(waterfall projects\)
    1.  Portfolio managers create planning items in Strategic Planning.
    2.  After prioritization, export planning items to PPM Standard as projects.
    3.  Project managers build WBS, create tasks, assign resources, manage timeline in PPM.
    4.  Strategic Planning shows project status, costs, risks automatically
-   Scenario 2: SAFe only enterprise \(Scaled Agile Framework\)
    1.  Product managers create epics in Strategic Planning.
    2.  Export epics to SAFe for Program Increment \(PI\) planning.
    3.  SAFe teams break epics into features and stories, execute in sprints.
    4.  SAFe tracks epic progress across multiple ARTs.
-   Scenario 3: Hybrid organization \(multiple methodologies\)
    1.  Strategic Planning backlog contains projects \(PPM\), epics \(Agile 2.0 and SAFe\), and demands.
    2.  Each team exports their planning items to their preferred execution system.
    3.  Executives view unified progress, costs, and goals achievement in Strategic Planning regardless of the execution method.

## Troubleshoot execution integration

-   Issue: Planning item not appearing in PPM/Agile Development 2.0/SAFe
    -   Verify the execution system plugin is installed and activated.
    -   Check that planning item state is Prioritized \(items in the Backlog state don't export\).
    -   Confirm user has required role in execution system \(project\_manager, scrum\_admin, safe\_admin\).
-   Issue: Changes in PPM not syncing back to Strategic Planning
    -   Verify bi-directional sync is enabled in integration configuration.
    -   Check that the planning item and PPM project/epic are properly linked \(primary planning item field is populated\).
    -   Review transformation maps for any table, field, or choice mapping issues.

For detailed configuration steps, see [Configuring Strategic Planning with PPM, Agile 2.0, and SAFe](configuring-apw-with-agile-safe-and-ppm.md).

**Parent Topic:**[Exploring Portfolio Planning in Strategic Planning Workspace](../../alignment-planner-workspace/concept/alignment-planner-workspace.md)

