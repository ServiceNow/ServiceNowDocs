---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. See the following sections for release notes by version.Version 4.20.0 adds fiscal calendar support for goals. You can set goal targets, breakdowns, and check-in due dates on Standard, 13-Period, 4-4-5, 4-5-4, and 5-4-4 fiscal calendars in the Strategic Planning workspace and the Goal Framework and Advanced Goal Framework features.The version 4.19.0 release adds capabilities for demand management and Enterprise Agile Planning \(EAP\). You can partition demand data by department or business unit and define demand experiences that control fields, modules, and layout. Scrum and Kanban teams can plan under the same Agile Release Train in EAP. Goal targets support Maintain types and unique numbers, and target type changes keep recorded actuals.The version 4.18.0 delivers dedicated RIDAC pages within portfolio plans to consolidate portfolio governance \(risks, issues, decisions, actions, requested changes\) in one interface. Programs enhanced experience provides automatic dedicated planning views for every program with zero setup required. Additional enhancements include automated cost recalculation, scenario approval notifications, automatic target status calculation, and Scrum configuration options in Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/strategic-planning-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 20
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. See the following sections for release notes by version.

## About Strategic Planning

-   Define and manage strategic plans, goals, and targets while aligning planning items across portfolio plans, enterprise agile iterations, and organizational hierarchies to drive business outcomes.
-   Prioritize, roadmap, and score work items using predefined or custom lenses, with support for capacity planning, financial planning, and scenario planning to optimize portfolio decisions.
-   Capture and assess customer feedback and demands through configurable playbooks, using AI to summarize, identify similar items, and accelerate prioritization before converting them into work items.
-   Track risks, issues, decisions, actions, and changes \(RIDAC\) across planning items, iterations, and goals, and gain actionable insights through dashboards covering strategy, planning, feedback, and execution.

See [Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/alignment-planner-workspace-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/it-business-management-rn-landing.md)

## Version 4.20.0

Version 4.20.0 adds fiscal calendar support for goals. You can set goal targets, breakdowns, and check-in due dates on Standard, 13-Period, 4-4-5, 4-5-4, and 5-4-4 fiscal calendars in the Strategic Planning workspace and the Goal Framework and Advanced Goal Framework features.

### What's new

-   **[Fiscal calendars for goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/fiscal-calendar-support-targets.md)**

    Create, edit, and break down goal targets on fiscal calendars. The supported calendar types are Standard, 13-Period, 4-4-5, 4-5-4, and 5-4-4. Target breakdowns, due dates, and roll-ups follow the fiscal periods of the active calendar. Gregorian calendar behavior does not change.

-   **[Setting and switching goal calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/set-a-goal-calendar.md)**

    Set the goal calendar to Gregorian, which is the default, or to fiscal. Fiscal calendars come in three types: Regular, 4-4-5, and 13 Period. Switch from Gregorian to fiscal in the **sn\_gfa.calendar\_type** system property. Switch between fiscal types by changing the fiscal calendar type property, setting the fiscal unit, and regenerating the fiscal periods. A calendar change can make targets stale.

-   **[Fiscal check-in due dates and reminders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configure-target-checkin-reminders-spw.md)**

    Set check-in due dates by fiscal period for goal targets. When you enter actuals on a target breakdown, the check-in due date updates to match the fiscal period. Reminders for the Period check-in frequency follow the fiscal calendar.

-   **[Fiscal planning range and time scale](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/fiscal-calendar-support-targets.md)**

    View goals in fiscal mode in the Strategic Planning workspace. The planning range, time scale, saved preferences, graph, stale target actions, and check-in panel all use the fiscal periods of the active calendar. The grid and goals list show the generated fiscal period names.

-   **[Fiscal check-in frequencies for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/fiscal-calendar-support-targets.md)**

    Choose a check-in frequency that the active fiscal calendar supports. The target form offers only the frequencies that are valid for the calendar and the target date range, including Period. The target breakdown preview shows each generated period with its display name. The server validates every frequency and period on save, so a rejected change keeps the current breakdowns and shows the reason.

-   **[Stale target protection for goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-stale-targets.md)**

    Identify goal targets that become stale after a goal calendar change. Only targets with breakdowns can become stale, and stale targets stay locked until they are recovered. Recover a stale target in one of two ways. An administrator runs the **Goal calendar alignment - Reset check-in frequency for stale targets** scheduled job, and the target owner then selects a check-in frequency again. Or the target owner duplicates the target and sets a check-in frequency on the copy. The copy starts without the remarks, work notes, and history of the stale target.

-   **[AI target generation and goal insights in fiscal mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-insights-for-goal-spw.md)**

    Generate goal targets with the AI target generation skill on fiscal calendars. Generation uses the active calendar, the allowed frequencies, and the generated period names and dates. The server validates the generated output before it fills the new target form. Goal insights read fiscal period history in period order and do not assume Gregorian months or quarters.

-   **[Fiscal target automation and check-in history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-actuals-automation-spw.md)**

    Automation writes target values into the breakdown of the current fiscal period, using the fiscal period boundaries in the fiscal calendar time zone. Check-in history records take their reporting period from the fiscal calendar, and the roll-up remark shows the fiscal period name.

-   **[Track work within a state using substates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/substates-in-eap.md)**

    Teams that do several kinds of work in one state can't see where that work waits. Substates divide a state into steps that match how your team works. A scrum master creates substates on the **Substates** tab of Team Settings, sets their order, and marks one default for each state. When you change the state of a story, the substate changes to the default of the new state. The **Substate** field is hidden for teams that have no substates.

-   **[Spot overloaded lanes with WIP limits on the Planning board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/wip-limits-in-eap.md)**

    A lane that holds more work than planned can hide where work is stuck. WIP limits make those lanes visible on the Planning board. Each lane header shows the number of stories and the limit, for example 3/5. An amber header marks a lane at its limit. A red header with an alert icon marks a lane over its limit. Counts update as you move stories, and a limit never blocks a move.

-   **[Set WIP limits for your own team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/set-wip-limits-for-kanban-lanes-in-eap.md)**

    Each team works differently, so each team sets its own limits. A scrum master selects **Team Settings** on the Planning board and adds limits on the **Kanban WIP limits** tab. Choose a lane, which is a state or a substate of the team, and enter the limit. The **Team** field is set automatically, and each lane can have one limit.


### What's changed

-   **Target import check-in frequencies**

    Target import accepts Period as a check-in frequency. Import rejects a check-in frequency that the active calendar does not allow and shows a message that states the reason.

-   **[Duplicate target behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-a-copy-of-a-goal-or-target.md)**

    When you duplicate a target, the copy keeps the source check-in frequency only if the active calendar supports it. The copy gets new breakdowns from the active calendar and never copies the source breakdowns. The source target does not change.

-   **[Find the open sprints that block Planning Interval completion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/start-or-complete-iteration-in-eap.md)**

    When open child sprints prevent you from completing a Planning Interval, you must know which sprints to close. The completion alert now lists every open sprint by team. Each sprint links to the Agile board of the team for Agile Development 2.0 sprints. CWM teams link to the CWM board. All other sprints link to the EAP Backlog of the team.


## Version 4.19.0

The version 4.19.0 release adds capabilities for demand management and Enterprise Agile Planning \(EAP\). You can partition demand data by department or business unit and define demand experiences that control fields, modules, and layout. Scrum and Kanban teams can plan under the same Agile Release Train in EAP. Goal targets support Maintain types and unique numbers, and target type changes keep recorded actuals.

### What's new

-   **[Enterprise-wide deployment for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/ewd-for-demands-dw.md)**

    Partition demand data by any criteria, such as department or business unit, using Enterprise-Wide Deployment \(EWD\) partitioning on the Demand table and related entities. Demands are stamped with a matching partition, and users see only the demands, list views, search results, and dashboards for the partitions their role grants them.

    EWD for demands includes the following functionalities:

    -   Demand experiences: Define the way a particular demand should work including its form view, modules, and dynamic attributes. For example, a particular view or certain functions available on a demand or menu items hidden or visible for different types of demands.
    -   Demand partitions: Control the data visible to different users.
    -   Demand partitions dashboard: Dedicated dashboard for different demand partitions.
-   **[Smart assessments for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/smart-assessments-overview.md)**

    Smart assessments are now available for demands, which are triggered on moving the demand to screening. These assessments are controlled by the **sn\_align\_ws.enable\_smart\_assessments** system property. After this property is enabled, smart assessments are triggered for the new demands and the ones that aren't yet in the screening state.

    The smart assessment form is more intuitive and supports text-based questions. The assessments are available at the individual demand record and in a consolidated Smart Assessments module in the main navigation menu. This module displays all assigned smart assessments across demands.

-   **[Resource profiling for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-planning-for-demands-dw.md)**

    Plan and manage resource assignments for a demand from the **Resources** tab in Next Experience for Demand Management. The resource board shows assignments alongside resource capacity so you can confirm availability before converting a demand to a project. Create, copy, move, split, end, or reassign resource assignments directly from the grid, group by primary group, role, or skill, and use the allocation heatmap to identify over-allocated and available resources. Use the Resource Finder to get fit-scored, ranked resource recommendations with rationale for unassigned work.

-   **[Kanban teams in the portfolio structure in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scrum-and-kanban-teams-in-eap.md)**

    Run Scrum and Kanban teams under the same Agile Release Train \(ART\). Select a planning methodology when you add a team to an ART, or set the Planning methodology field on an existing team. Kanban teams plan from the team backlog: sprint controls are hidden, planning intervals skip them, and the Home page shows the Kanban Team dashboard. Both team types appear side by side on the ART planning board.

-   **[Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-types-overview.md)**

    Track targets that must hold steady across every check-in period using the **Maintain above**, **Maintain below**, and **Maintain constant** target types. Each breakdown period's planned target defaults to the final target value, or 0 if no final value is set, and you can edit it for each period. Target progress is the share of periods that met the condition: at or above the target for Maintain above, at or below it for Maintain below, and within a tolerance band around it for Maintain constant. The default tolerance band is ±5%, and administrators can change it with the **sn\_gf.maintain\_constant\_tolerance\_percent** system property. For example, a Maintain above target of 75 with quarterly actuals of 78, 72, 80, and 76 shows 75% progress, because one of the four quarterly actuals didn't meet the target.

    When you change the start date, end date, or final target value, the breakdowns and planned values adjust automatically and actuals in the remaining periods are kept. The **Target value distribution** field is hidden for Maintain types.

-   **[Unique numbers and prefixes for goals and targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/change-number-prefix-goals-targets-spw.md)**

    Differentiate goals and targets that share a name across teams by using the **Number** field. Goals use the OBJ prefix and targets use the KR prefix, for example OBJ0004512 and KR0009871. The number appears on goal and target forms, list views, board views, and exports. The **GF - Override Goal and Target Number fields with customized prefixes** scheduled job updates existing GOAL and TRGT numbers to OBJ and KR and keeps the numeric portion. An administrator can run the scheduled job to override default populated prefixes.


### What's changed

-   **[Switching a team to Kanban in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/switch-agile-team-to-kanban-in-eap.md)**

    Sprints that aren't complete are cancelled when you set a team's Planning methodology to Kanban, including the team's current sprint. Completed and cancelled sprints aren't changed, and work items stay assigned to the sprints that were cancelled. A team connected to Collaborative Work Management \(CWM\) can't be switched to Kanban while it has active or planned sprints.

-   **[Planning methodology on existing teams in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scrum-and-kanban-teams-in-eap.md)**

    Each existing agile team is assigned a planning methodology when you upgrade: Scrum if the team or its configuration has a business calendar, Kanban if neither has one. Because Kanban teams don't show sprint controls, review any team created without a business calendar and set its Planning methodology to Scrum if that team plans in sprints.

-   **[Automatic status for Maintain type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/automatic-status-calculation-targets-spw.md)**

    Automatic status calculation extends to Maintain type targets. Each breakdown period is set to Green when its actual meets the Maintain condition and Red when it doesn't.

-   **[Target type changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-types-overview.md)**

    Change a target's type after actuals are recorded, without deleting and recreating the target. Actuals to date are kept and recorded in the latest breakdown period. Planned values are recalculated for the new type, and progress is evaluated under the new type's logic. A confirmation message appears before the change is applied, and selecting **Cancel** keeps the previous type and data. Type changes are captured in the audit history.

-   **[Unit of measure on targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/set-targets-for-goal-egm.md)**

    Select the target type before the unit of measure when you create a target. Milestone sets the unit of measure to Yes/No, and Maximize, Minimize, and Maintain types default to Count. Later type changes keep the unit of measure you selected. If it isn't valid for the new type, you're prompted to pick one. This applies to the target modals in Enterprise Goals and portfolio plan goals, and to inline editing in the target list.

-   **[No status label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/components-installed-with-alignment-planner-workspace.md)**

    The None status choice is labeled **No status** for goals, strategic priorities, targets, target progress, and target breakdowns.

-   **[RIDAC by portfolio and program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-plan-ridac-spw.md)**

    View decisions alongside other RIDAC items for portfolios and programs when you open RIDAC from the Strategic Planning Workspace RIDAC menu. The **Portfolio Risks** and **Program Risks** menus are renamed **RIDAC by Portfolio** and **RIDAC by Program**.

-   **[Target generation for Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-targets-for-goal.md)**

    Generate Maintain above, Maintain below, and Maintain constant targets with ServiceNow Otto target generation skill for goals that sustain a level rather than move toward one, such as platform uptime, a cost ceiling, or team headcount. When a Maintain type is suggested, the target modal shows the threshold value and hides the start value field. Review the suggested type and change it if needed before you save the target.

-   **[Goal insights for Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-insights-for-goal-spw.md)**

    ServiceNow Otto goal insights include Maintain-type targets \(Maintain above, Maintain below, and Maintain constant\) when summarizing goal progress.

-   **[Resource assignment offsets when converting a demand to a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/data-migrated-from-demand-to-project-dw.md)**

    When a demand with resource assignments is converted to a project, assignment offsets are recalculated against the project's schedule, which counts only the working days defined in the project schedule, instead of the demand, which has no schedule and counts every calendar day.

-   **[Execution URL on planning item demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/update-execution-url-for-demand-spw.md)**

    Run the **Update Demand Planning Item Execution URL** scheduled job to update the execution URLs on your existing demands to the latest format.

-   **[Roadmap export range](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/export-a-portfolio-plan-to-powerpoint-strategic-planning.md)**

    The maximum date range for exporting a roadmap to PowerPoint increased from 1 year to 3 years, within the start and end dates of the portfolio. The exported timescale adjusts to the range you select: months for a range of 1 year or less, and quarters for a range longer than 1 year.

-   **[Program portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-spw.md)**
    -   **Program details** — Select the information icon next to the program name to view the planning item types, program timeline, and program manager.
    -   **Program value for new items** — When you create a demand or project from a program portfolio plan, the **Program** field is prefilled with that program.
    -   **Prioritization default layout** — The default **Prioritization** view shows the Rank, Name, Planning state, Planning item type, Status, Cost status, Resource status, Schedule status, Scope status, Percent complete, Primary goal, and Owner columns.
    -   **Goals tab** — Program portfolio plans include the **Goals** tab, which shows all primary and non-primary goals linked to the planning items in the plan, along with goals assigned directly to the program.
    -   **Public views** — Any user who can access a program portfolio plan can create and update its public views. Previously, only plan editors could create or update public views.

## Version 4.18.0

The version 4.18.0 delivers dedicated RIDAC pages within portfolio plans to consolidate portfolio governance \(risks, issues, decisions, actions, requested changes\) in one interface. Programs enhanced experience provides automatic dedicated planning views for every program with zero setup required. Additional enhancements include automated cost recalculation, scenario approval notifications, automatic target status calculation, and Scrum configuration options in Enterprise Agile Planning.

### What's new

-   **[RIDAC for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-plan-ridac-spw.md)**

    Access portfolio risks, issues, decisions, actions, and requested changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page within the portfolio plan. View all portfolio governance items in a single, integrated interface without navigating to the separate RIDAC menu. The RIDAC page reduces context-switching and improves portfolio visibility by consolidating governance data. The portfolio plan RIDAC displays the RIDAC items that match the portfolio plan's criteria or belong to the planning items of that portfolio plan.

-   **[Show or hide RIDAC page of a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/show-or-hide-the-features-for-your-portfolio-plan-spw.md)**

    As a portfolio manager, show or hide the RIDAC page of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Programs enhanced experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-spw.md)**

    Access dedicated program planning views automatically created with zero setup. Navigate to the new Programs menu and click any program to open its dedicated plan with Prioritization, Roadmap, Kanban, and Financials views. New programs get plans instantly; existing programs receive them through an automatic one-time backfill \(500 at a time, newest first\). Role-based access ensures users with the sn\_align\_core.ap\_read\_only role can read, users with the sn\_align\_core.apw\_user role can manage items, and program managers are automatic plan owners.

-   **[Program-scoped data with fiscal calendar support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-spw.md)**

    View and manage program-scoped planning data in a focused, streamlined interface. Program plans display only that program's planning items. The Financials tab defaults to your fiscal calendar; if the fiscal calendar doesn't span the program dates, the system gracefully falls back to Gregorian with an explanatory message. Making the portfolio plan public and scenario planning for these program portfolio plans are hidden.

-   **[Automated email notification for scenario approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/approve-a-scenario-in-strategic-planning.md)**

    Receive email notification when a scenario is approved. The system sends the notification to the scenario approver and portfolio owner. During the approval process, the portfolio plan becomes read-only to prevent unintended modifications and maintain data integrity.

-   **[Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/automatic-status-calculation-targets-spw.md)**

    Automatically determine target status based on actual achievement percentages. When you enter actual values for a target period, the system compares the achievement percentage against predefined thresholds and automatically assigns a status \(Green, Yellow, or Red\). This eliminates manual status selection, reducing data entry errors and improving organizational governance.

    Status is calculated and updated when you enter actual values using the formula: \(\(Actual Value - Start Value\) / \(Planned Target - Start Value\)\) x 100. Target owners can override automatically calculated status values at any time. If you update the actual value after a manual override, the system recalculates the status automatically.

-   **[Configure automatic status calculation thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configure-automatic-status-calculation-spw.md)**

    Enable administrators to customize automatic status calculation thresholds and enable or disable the feature based on organizational requirements. By default, automatic status calculation is enabled with system-defined thresholds of Green \(≥90%\), Yellow \(75-89%\), and Red \(&lt;75%\).

    Administrators can adjust threshold percentages using the system property **sn\_gfa.target.auto\_status.thresholds**. To disable automatic status calculation and revert to manual status selection, set the system property to `false`.

-   **[Scrum Configuration in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-configurations-in-eap.md)**

    Set up teams that run Sprints without a Planning Interval above them by using the Scrum Configuration in Enterprise Agile Planning. It defines a single team level of the type Agile Team and allows the Epic and Story work item types. Story is the default work item type for that level and is mapped to the new **Scrum Sprint** planning calendar. The **Epic methodology** field is set to **Scrum**. Like the other default configurations, the Scrum Configuration is inactive until you activate it.

-   **[Unique iteration cadence for each team in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/simplified-iteration-creation-in-eap.md)**

    Let each team set its own iteration dates by selecting **Allow unique cadence for each team** on an Enterprise Agile Planning configuration. If the configuration has planning calendars at more than one team level, each top-level team receives its own calendar. If the configuration has a single level of iterations, such as Sprints only, the iterations carry their own start and end dates instead of following a planning calendar entry. Teams that you add after you select this option receive a unique calendar, and teams that already exist continue to use the default calendar of the configuration.

-   **[Spillover and New scope fields on iterations in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/start-or-complete-iteration-in-eap.md)**

    See how the scope of a Sprint moved during its run by using the **Spillover** and **New scope** fields on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] record. Spillover is the sum of the story points of the committed stories that are no longer in the iteration when it completes. New scope is the sum of the story points of the stories that were added after the iteration started. Both fields are read-only and are calculated when you complete the iteration. Select a value to open the stories that it counts.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/clone-customize-demand-summarization-skill.md)**

    Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/my-demands-widget.md)**

    Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


### What's changed

-   **Financials**

    Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Enterprise Agile Planning configuration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-eap-configuration.md)**
    -   The **Have unique calendars** option is renamed to **Allow unique cadence for each team**.
    -   An EAP admin can now clear the **Allow unique cadence for each team** option after selecting it. Selecting the option doesn't change the calendars or the iterations that already exist.
    -   The **Scrum Sprint** planning calendar type is available by default, alongside **Planning Interval** and **Sprint**.
-   **[Iteration dates in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/edit-pi-sprint-iteration-details-in-eap.md)**
    -   The **Enterprise agile calendar entry** field on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] table is no longer mandatory, which supports iterations that carry their own start and end dates. A fix script makes the field optional when you upgrade.
    -   Users with the `sn_apw_advanced.eap_user` role can set the start date and the end date while they create an iteration. They can change those dates afterward on an iteration that doesn't follow a planning calendar entry. However, changing the dates on an iteration that follows a planning calendar entry still requires the `sn_apw_advanced.eap_scrum_master` role.
-   **[Sprint sync with Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/sync-eap-and-agile-2.md)**
    -   Sprints that don't follow a planning calendar entry now sync to Agile Development 2.0 by using the start date and the end date on the iteration.
    -   Changing the start date or the end date of an iteration now updates the dates on the corresponding Sprint in Agile Development 2.0.
-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-spw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/summarize-demand-in-demand-workspace.md)**

    The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Process Mining**

    Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining.md) documentation.


