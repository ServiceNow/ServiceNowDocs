---
title: Combined Business Continuity Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Business Continuity Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/delta-yokohama-australia/australia-yokohama-businesscontinuitymanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined Business Continuity Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Business Continuity Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Business Continuity Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Business Continuity Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Business Continuity Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Using latest assessment for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&family=yokohama&ft:locale=en-US)**

Conduct a Business Impact Analysis \(BIA\) by using the latest assessment template. The assessment template enables you to create questions of different types and automate the responses from existing data sources. You can configure the logic for calculating the recovery tier, recovery point objective, recovery time objective, or maximum tolerable downtime.

-   **[Adopting UIB page for improved performance](https://www.servicenow.com/docs/access?context=crisis-map-migration&family=yokohama&ft:locale=en-US)**

Leverage the Crisis map functionality that includes the latest UIB components. By adopting the UIB components, you can help to minimize development efforts and get more configuration options within the Crisis map application.

You can filter alerts by their state \(active or inactive\), severity level, location \(regions\), or source. You can refine your search, perform detailed queries, or edit actions on the alerts, so that it's easier to find both the alerts and assets on the map. Additionally, you can set the secondary values such as urgency, severity, category for the alerts in the Details card.

-   **[Using nested plans](https://www.servicenow.com/docs/access?context=creating-nested-plan-in-event&family=yokohama&ft:locale=en-US)**

Create nested plans in an event so that you can activate cross-references to multiple plans. You can use the hierarchical view to organize nested event tasks according to their dependencies with the work-breakdown structure \(WBS\) functionality. You can also monitor the progress bar to track the creation of related plans, event assets, or event tasks.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Map recovery tasks and event tasks to the phases](https://www.servicenow.com/docs/access?context=mapping-recovery-tasks-to-phases&family=zurich&ft:locale=en-US)**

Set up phases for plans and events using the administrative setup. The base version of the application includes a set of default active phases, provided as seed data.

The logical grouping of tasks into phases enables clear progression tracking for exercises and crisis events, offering flexible execution and task completion requirements for phase transitions.

-   **[View and generate PDFs of approved plans](https://www.servicenow.com/docs/access?context=mobile-bcm&family=zurich&ft:locale=en-US)**

View the continuity and recovery plans directly from your mobile devices. BCM managers can generate PDFs of the approved plans, which BCM planners can then view and download, streamlining access to critical information on the go.

-   **[Verify asset recovery levels](https://www.servicenow.com/docs/access?context=create-new-impact-analysis-reference-form-bcm-uib-ws&family=zurich&ft:locale=en-US)**

Track event assets and verify the achieved recovery level of the impacted assets of a task in the **Asset recovery level** field. Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables coordinators to identify when dependent assets can safely start their recovery process. Color-coded recovery levels of the assets offer visual cues for various recovery progress levels.

-   **[Use finalized RTO and RPO in BIAs, Plans, and Events](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&family=zurich&ft:locale=en-US)**

Use the **Finalized RTO** field to calculate an accurate Recovery Time Objective \(RTO\) for comparison, using values from the **Recovery time objective** and **Adjusted RTO** fields.

Similarly, use the **Finalized RPO** field to calculate an accurate Recovery Point Objective \(RPO\) values for comparison, using values from the **Recovery point objective** and **Adjusted RPO** fields.

A fix script now populates finalized RTO and RPO values in existing Business Impact Analyses \(BIAs\), ensuring consistency across all records.

-   **[Configure recovery tasks for exercises, events, or both](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&family=zurich&ft:locale=en-US)**

Configure recovery tasks with event-specific scopes \(exercises, actual crises, or both\). When a recovery event is initiated, the system automatically filters tasks by event type: ensuring exercises include necessary setup and validation, and actual crises focus exclusively on actionable recovery work.

-   **[Auto-calculate the Planned end date on activated plans and event tasks](https://www.servicenow.com/docs/access?context=create-exercise-event-ref-form&family=zurich&ft:locale=en-US)**

Enter the Planned start date for exercises and events. The system then calculates the Planned start and end dates for activated plans and event tasks automatically based on the **Planned duration** field and dependencies.

-   **[Use hierarchical structure in the associated plans](https://www.servicenow.com/docs/access?context=add-related-plans-recovery-teams-bcp-uib-ws&family=zurich&ft:locale=en-US)**

Use the hierarchical structure in the associated plans, establishing clear upstream-downstream relationships. This hierarchy confirms that only relevant downstream plans are brought into scope. The system automatically handles cyclic dependency checks, confirming that tasks from downstream plans aren’t added as dependencies in the upstream plans.

-   **[Use Gantt chart in the Hierarchy view](https://www.servicenow.com/docs/access?context=managing-enhanced-hierarchical-view-in-event-tasks&family=zurich&ft:locale=en-US)**

Use the Gantt chart in the Hierarchy view to visualize the planned and actual timelines of event tasks. Task dependencies can now be created directly on the Gantt chart, provided the dependency points to a task scheduled ahead in time. Plans are automatically sorted based on the planned start time of their earliest event task, verifying a clear chronological view.


 -   **[Exclude non-recovery tasks from time calculation](https://www.servicenow.com/docs/access?context=add-a-recovery-task&family=zurich&ft:locale=en-US)**

Exclude specific recovery or event tasks from time calculations by using the **Do not include in time calculation** field within recovery or event tasks.

-   **[Generate reports in a Microsoft Word format using Document designer](https://www.servicenow.com/docs/access?context=integrating-document-designer-with-bcm&family=zurich&ft:locale=en-US)**

Create standardized reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using predefined Microsoft Word templates. To use these templates, first establish a template relationship registry and install the necessary add-in to design and configure the templates.

Then, import the relevant documents and customize their content, including the table of contents, details, impact assessments, dependencies, and attachments, to be included in the reports. Finally, generate the reports and save them to the corresponding application records.

You can control whether to retain or replace the existing report attachments by configuring the **sn\_bcm.retain\_report\_attachments** system property.

-   **[Avoid duplicate event tasks by grouping similar event tasks](https://www.servicenow.com/docs/access?context=identifying-running-dup-tasks-once&family=zurich&ft:locale=en-US)**

Group similar event tasks during recovery events. The system automatically designates the first event task as the original task. When the original task is in progress, the remaining tasks are placed in the **On Hold** state. After the original task is closed, the other tasks in the group are automatically marked in the **Closed duplicate** state.

Tasks with internal dependencies can't be part of the same group. You can also unlink the tasks from their groups, so that the system helps to prevent cyclic dependencies within a group.

-   **[Manage action items for ad-hoc tasks and threat assessments](https://www.servicenow.com/docs/access?context=create-action-items-based-on-smart-assessments&family=zurich&ft:locale=en-US)**

Create action items for ad-hoc tasks and send out threat assessments that leverage Smart Assessment during exercises and crises. You can create action items for tasks that support recovery efforts, such as communicating with stakeholders, leadership, or vendors, without directly restoring an asset. Use these action items to conduct threat assessments with the Smart Assessment Engine before, during, or after a recovery event.

To enable task creation during an ongoing event, the Smart Assessment template must include both an event and an action item within its scope.

-   **[Revert an archived BIA or BCP to the Draft state](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&family=zurich&ft:locale=en-US)**

Revert an archived business impact analysis \(BIA\) or business continuity plan \(BCP\) to its **Draft** state by selecting the **Edit** button on the form. By revising previously completed BIAs, you save time by using a BIA that's already been created.

-   **[Optimized Crisis map interface](https://www.servicenow.com/docs/access?context=manage-alerts-in-crisis-map-interface-uib-ws&family=zurich&ft:locale=en-US)**

The Crisis map interface has been optimized to handle over 10,000 resources and more than 1,000 alerts without performance issues.Customize the display of impacted areas for alerts by using custom shapes or specifying a custom radius. To edit an impacted area, simply select its corresponding card and make the necessary adjustments to the shape. If needed, you can also revert the changes made to an impacted area directly within the map interface.


</td></tr><tr><td>

Australia

</td><td>

-   **[Task template groups and Task templates](https://www.servicenow.com/docs/access?context=create-reco-task-tem-groups&family=australia&ft:locale=en-US)**

Create reusable Task templates for recovery and event tasks, and organize them into groups with configurable dependencies. Scope groups to all element definitions or a specific type, and define task sequencing within a group to preserve execution order when applied.

-   **[Task templates and Task template groups integration in plan templates](https://www.servicenow.com/docs/access?context=configure-a-bcp-template-uib-ws&family=australia&ft:locale=en-US)**

Associate Task template groups and Task templates at the plan, loss scenario, and recovery strategy levels within a plan template. Creating a plan from a template automatically generates all linked records at each level, with a progress tracker showing status throughout.

-   **[Task templates and Task template groups support in plans](https://www.servicenow.com/docs/access?context=create-reco-task-tem-groups&family=australia&ft:locale=en-US)**

Add Task template groups and individual Task templates directly from recovery task lists.

-   **[Task templates and Task template groups support in Exercises and Crisis events](https://www.servicenow.com/docs/access?context=add-an-event-task-to-exercise-event&family=australia&ft:locale=en-US)**

Add Task template groups and individual templates directly from event task lists. Select groups, assign an activated plan when required, and the system creates all tasks with dependencies intact. An auto-refresh banner tracks progress and refreshes the list once after all tasks are created.

-   **[Recovery strategy templates](https://www.servicenow.com/docs/access?context=configure-recovery-strategy-template-uib-ws&family=australia&ft:locale=en-US)**

Create reusable recovery strategy templates with standard fields including name, description, estimated time limit, and maximum duration. Apply a template to auto-populate a recovery strategy, reducing manual entry and keeping strategies consistent across plans.

-   **[Gantt chart for recovery tasks in plans](https://www.servicenow.com/docs/access?context=view-gantt-chart-for-reco-tasks&family=australia&ft:locale=en-US)**

Visualize recovery task sequences, durations, and dependencies on an interactive Gantt timeline within the plan record. Toggle between list and Gantt views from the **Recovery tasks** tab. Add or edit tasks using a right-select quick-insert panel, pre-filled with task type and sequencing context.Filters, sorting, and selections remain consistent when switching between list and Gantt views. The quick-add panel is also available on loss scenario and recovery strategy records. Access is role-controlled: Planners manage tasks in their own plans; Program Managers have full access across all plans.

-   **[Export and import event tasks in Microsoft Excel](https://www.servicenow.com/docs/access?context=using-export-import-feature-event-tasks&family=australia&ft:locale=en-US)**

Export recovery event tasks to Microsoft Excel from the Event tasks related list. The workbook includes a Data sheet, a read-only Event details tab, and an Instructions sheet. Non-editable columns are locked. Import the updated file when the event is in the Open or Work in progress state. Track import progress in real time, with a full audit trail available on the Recovery event form.

-   **[Role-based Performance Analytics dashboards](https://www.servicenow.com/docs/access?context=pa-dashboard-summary&family=australia&ft:locale=en-US)**

Access role-based Performance Analytics dashboards directly from the BCM workspace. Four dashboards are available, each tailored to a functional area: Home \(overall BCM status\), BIA \(impact analysis progress\), BCP \(planning records\), and Event \(recovery exercises and activities\). Each dashboard is permission-controlled and views are displayed relevant to the roles.

-   **[Assessment template version control](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&family=australia&ft:locale=en-US)**

Track the template version used at the time of assessment creation on Smart Assessment Engine \(SAE\) templates. Assessors and reviewers can clearly see which template version was in effect, making it easier to audit and compare assessments over time.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Business Continuity Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Using latest assessment for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&family=yokohama&ft:locale=en-US)**
    -   The BIA form displays the assessment questionnaire that is based on the latest assessment template. The **Assessments** tab in the BIA record page has been enhanced to eliminate repetitive UI actions and reduce large empty spaces. The latest assessment template includes additional question types such as drop-down, references, text, attachments, check boxes, date, time, and number value inputs.
    -   The PDF template for the BIA has been updated to include the questions and answers that are based on the latest assessment template.
-   **[Adopting UIB page for improved performance](https://www.servicenow.com/docs/access?context=crisis-map-migration&family=yokohama&ft:locale=en-US)**

The enhancements to the Crisis map user interface are:

    -   Alerts are displayed in the side panel of the Crisis map application.
    -   The alert details page includes the **Open alert** and **Dismiss alert** UI actions, which enable you to either open or dismiss alerts.
    -   The active alerts can be sorted by using the **Severity**, **Created**, **Updated** fields, and can also be toggled from top-to-bottom or bottom-to-top by using the Toggle option.
    -   The alerts display can be updated with the Refresh icon \[Omitted image "image.refresh-icon"\] Alt text: Refresh icon..
    -   The active and dismissed alerts are now displayed on the Alerts page.
-   **[Using nested plans](https://www.servicenow.com/docs/access?context=creating-nested-plan-in-event&family=yokohama&ft:locale=en-US)**

The enhancements to the nested plans user interface are:

    -   The hierarchical view shows the nested event tasks.
    -   The progress bar displays the progress of the creation of related plans, event assets, or event tasks.

 -   **[Using latest assessment for conducting BIAs](https://www.servicenow.com/docs/access?context=using-smart-asmt-template&family=yokohama&ft:locale=en-US)**

You can use the latest assessment template to conduct the Business Impact Analysis \(BIA\).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Configuring the phases](https://www.servicenow.com/docs/access?context=set-up-phases&family=zurich&ft:locale=en-US)**

The Active phases module is available in the General Administration setup for configuring the phases.

-   **[Phase column](https://www.servicenow.com/docs/access?context=add-a-recovery-task&family=zurich&ft:locale=en-US)**

The recovery and event tasks now include the Phase column in the list and form views, indicating association with specific phases within the recovery process.

-   **[Do not include tasks in time calculation](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&family=zurich&ft:locale=en-US)**

The **Do not include tasks in time calculation** field has been added to Recovery tasks, enabling you to exclude specific tasks from overall time calculations.

-   **[Asset recovery level column](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&family=zurich&ft:locale=en-US)**

The Asset recovery level column is added to the recovery tasks to indicate recovery levels of the assets.

-   **[Include task in field](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&family=zurich&ft:locale=en-US)**

The **Include task in** field is added in the recovery tasks to specify whether a task should be included in an exercise, crisis event, or both.

-   **[Finalized RTO and RPO](https://www.servicenow.com/docs/access?context=create-new-impact-analysis-reference-form-bcm-uib-ws&family=zurich&ft:locale=en-US)**

The Finalized RTO column is shown in the chart and list views, replacing the previously shown RTO and Adjusted RTO columns. Similarly, the Finalized RPO column is shown in the chart and list views, replacing the previously shown RPO and Adjusted RPO columns.

-   **[Associated plans tab](https://www.servicenow.com/docs/access?context=add-related-plans-recovery-teams-bcp-uib-ws&family=zurich&ft:locale=en-US)**

The **Associated plans** tab in the Plan record replaces the **Related plan** and **Parent plan** tabs. Upstream, Downstream, and Related plans are now included as associated plan types.

-   **[Gantt chart in the Hierarchy view](https://www.servicenow.com/docs/access?context=managing-enhanced-hierarchical-view-in-event-tasks&family=zurich&ft:locale=en-US)**

A Gantt chart has been added to the Hierarchy view to help visualize the planned and actual timelines of event tasks.


 -   **[Predefined Word templates](https://www.servicenow.com/docs/access?context=edit-report-temp&family=zurich&ft:locale=en-US)**

Predefined Microsoft Word templates are now provided in the instance.

-   **[Similar tasks group tab](https://www.servicenow.com/docs/access?context=identifying-running-dup-tasks-once&family=zurich&ft:locale=en-US)**

The **Similar tasks groups** tab is now included in the events and the **Create similar tasks group** UI action is available in the **Event tasks** tab.

-   **[Action items tab in Exercises and Crises modules](https://www.servicenow.com/docs/access?context=create-action-items-based-on-smart-assessments&family=zurich&ft:locale=en-US)**

The **Action items** tab is now available in both exercises and crises.

-   **[Pagination for alerts](https://www.servicenow.com/docs/access?context=manage-alerts-in-crisis-map-interface-uib-ws&family=zurich&ft:locale=en-US)**

Pagination has been added to alerts in Crisis map, to make them more readable on the map interface.Edit the impacted area of an alert by using custom shapes or a custom radius. Similarly, you can revert the changes made to an impacted area within the map interface.

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Recovery strategy templates](https://www.servicenow.com/docs/access?context=configure-recovery-strategy-template-uib-ws&family=australia&ft:locale=en-US)**

The Recovery strategy template form is used to create reusable templates that can be applied to recovery strategies across loss scenarios and business continuity plans.

-   **[Task template integration in plan templates](https://www.servicenow.com/docs/access?context=configure-a-bcp-template-uib-ws&family=australia&ft:locale=en-US)**

Plan templates support two synchronization options: Plan scope asset synchronization and Loss scenario asset synchronization with recovery strategy assets.

-   **[Related lists for Plan templates](https://www.servicenow.com/docs/access?context=plan-template-form&family=australia&ft:locale=en-US)**

The Plan templates record has the following related lists:

    -   Task template groups
    -   Task templates
-   **[Related lists for Loss scenarios](https://www.servicenow.com/docs/access?context=add-loss-scenario-recovery-task-bcp-uib-ws&family=australia&ft:locale=en-US)**

The Loss scenarios record has the following related lists:

    -   Task template groups
    -   Task templates
    -   Recovery strategies
    -   Plan templates
-   **[Related lists for Recovery strategies](https://www.servicenow.com/docs/access?context=create-new-recovery-strategy-for-loss-scenario-uib-ws&family=australia&ft:locale=en-US)**

The Recovery strategies record has the following related lists:

    -   Task template groups
    -   Task templates
    -   Loss scenarios
    -   Plan templates
-   **[Recovery tasks](https://www.servicenow.com/docs/access?context=create-quick-recovery-task&family=australia&ft:locale=en-US)**

The recovery task list includes four additional columns: Plan loss scenario, Plan recovery strategy, Tag, and Task group. Use these columns to filter, group, and report on recovery tasks by scenario, strategy, or template group.The recovery task list toolbar includes **Insert** \(with Select task template groups\), **Save as group** \(with Add to group and Save tasks sub-options\), and **Add groups** for bulk insertion of task template groups.The Create a quick recovery task panel includes Phase, Plan recovery strategy, All assets from plan, and a Planned duration field accepting hours, minutes, and seconds. The All assets from plan field can be narrowed to a subset of assets when a task applies to only part of the plan.A Gantt view is available on the **Recovery tasks** tab of a plan record.

-   **[Event task list toolbar](https://www.servicenow.com/docs/access?context=export-import-event-tasks-using-excel&family=australia&ft:locale=en-US)**

The event task list toolbar adds **Export to Excel** and **Import from Excel** actions for managing tasks in bulk and switching between list and Gantt views.

-   **[Loss scenario Recovery tasks tab](https://www.servicenow.com/docs/access?context=add-loss-scenario-recovery-task-bcp-uib-ws&family=australia&ft:locale=en-US)**

Each loss scenario record includes a **Recovery tasks** tab that lists only the recovery tasks scoped to that scenario.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Business Continuity Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Business Continuity Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Business Continuity Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Business Continuity Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


**Important:** Business Continuity Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Business Continuity Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Business Continuity Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Business Continuity Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Business Continuity Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Business Continuity Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Business Continuity Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Browser requirements**

Business Continuity Management requires the following browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

Business Continuity Management requires the following browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Business Continuity Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Accessibility information**

Various accessibility issues in the Crisis map application have been resolved with the implementation of the Geomap \[sn\_geo\_map\] component, which has replaced the FAM Map \[sn-fam-map\] component.


</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Business Continuity Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Business Continuity Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Use the latest assessment template to perform a Business Impact Analysis.
-   Create nested plans in an event so that you can activate cross-references to multiple plans.
-   Use the hierarchical view in the plans to organize nested event tasks according to their dependencies.
-   Use the Crisis map functionality that includes the latest UIB components.

 See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Set up phases in recovery tasks and event tasks for recovery event management.
-   Calculate more accurate RTO and RPO with the finalized RTO and RPO columns in BIAs, BCPs, and events.
-   View plans from the enhanced BCM Mobile application.
-   Manage templates and generate Microsoft Word reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using the Document designer add-in.
-   Avoid duplicate event tasks by identifying and grouping similar tasks in exercises and crises.
-   Create action items and send out threat assessments by leveraging Smart Assessment during exercises and crises.

 See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Build reusable Task templates and groups with dependencies across plans, loss scenarios, and exercises.
-   Auto-generate full plan hierarchies — scenarios, strategies, and tasks — from plan templates.
-   Export event tasks to Microsoft Excel, edit offline, and reimport updated records with validation and progress tracking.
-   Monitor performance through role-based dashboards with key performance indicators and usage insights.

 See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/delta-yokohama-australia/rn-combined-intro.md)

