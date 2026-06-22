---
title: Combined Business Continuity Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Business Continuity Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-businesscontinuitymanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Business Continuity Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Business Continuity Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Business Continuity Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Business Continuity Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   **[Map recovery tasks and event tasks to the phases](https://www.servicenow.com/docs/access?context=mapping-recovery-tasks-to-phases&family=zurich&ft:locale=en-US)**

Set up phases for plans and events using the administrative setup. The base version of the application includes a set of default active phases, provided as seed data.

The logical grouping of tasks into phases enables clear progression tracking for exercises and crisis events, offering flexible execution and task completion requirements for phase transitions.

-   **[Exclude non-recovery tasks from time calculation](https://www.servicenow.com/docs/access?context=add-a-recovery-task&family=zurich&ft:locale=en-US)**

Exclude specific recovery or event tasks from time calculations by using the **Do not include in time calculation** field within recovery or event tasks.

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

The Crisis map interface has been optimized to handle over 10,000 resources and more than 1,000 alerts without performance issues.

Customize the display of impacted areas for alerts by using custom shapes or specifying a custom radius. To edit an impacted area, simply select its corresponding card and make the necessary adjustments to the shape. If needed, you can also revert the changes made to an impacted area directly within the map interface.


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

Add task template groups and individual templates directly from event task lists. Select groups, assign an activated plan when required, and the system creates all tasks with dependencies intact. An auto-refresh banner tracks progress and refreshes the list once after all tasks are created.

-   **[Recovery strategy templates](https://www.servicenow.com/docs/access?context=configure-recovery-strategy-template-uib-ws&family=australia&ft:locale=en-US)**

Create reusable recovery strategy templates with standard fields including name, description, estimated time limit, and maximum duration. Apply a template to auto-populate a recovery strategy, reducing manual entry and keeping strategies consistent across plans.

-   **[Gantt chart for recovery tasks in plans](https://www.servicenow.com/docs/access?context=view-gantt-chart-for-reco-tasks&family=australia&ft:locale=en-US)**

Visualize recovery task sequences, durations, and dependencies on an interactive Gantt timeline within the plan record. Toggle between list and Gantt views from the **Recovery tasks** tab. Add or edit tasks using a right-select quick-insert panel, pre-filled with task type and sequencing context.

Filters, sorting, and selections remain consistent when switching between list and Gantt views. The quick-add panel is also available on loss scenario and recovery strategy records. Access is role-controlled: Planners manage tasks in their own plans; Program Managers have full access across all plans.

-   **[Export and import event tasks in Microsoft Excel](https://www.servicenow.com/docs/access?context=using-export-import-feature-event-tasks&family=australia&ft:locale=en-US)**

Export recovery event tasks to Microsoft Excel from the Event tasks related list. The workbook includes a data sheet, a read-only Event Details tab, and an Instructions sheet. Non-editable columns are locked. Import the updated file when the event is in the Open or Work in progress state. Track import progress in real time, with a full audit trail available on the Recovery Event form.

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


For more information, see [BCM and ServiceNow Store](https://www.servicenow.com/docs/access?context=bcm-and-store&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Business Continuity Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

Install Business Continuity Management by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Business Continuity Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Business Continuity Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

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

Zurich

</td><td>

-   ****

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

-   Build reusable task templates and groups with dependencies across plans, loss scenarios, and exercises.
-   Auto-generate full plan hierarchies — scenarios, strategies, and tasks — from plan templates.
-   Export event tasks to Microsoft Excel, edit offline, and reimport updated records with validation and progress tracking.
-   Monitor performance through role-based dashboards with key performance indicators and usage insights.

 See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

