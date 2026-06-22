---
title: Combined Business Continuity Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Business Continuity Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-businesscontinuitymanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Business Continuity Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Business Continuity Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Business Continuity Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Business Continuity Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Business Continuity Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Using latest assessment for conducting BIAs](https://servicenow-staging.fluidtopics.net/access?context=using-smart-asmt-template&family=yokohama&ft:locale=en-US)**

Conduct a Business Impact Analysis \(BIA\) by using the latest assessment template. The assessment template enables you to create questions of different types and automate the responses from existing data sources. You can configure the logic for calculating the recovery tier, recovery point objective, recovery time objective, or maximum tolerable downtime.

-   **[Adopting UIB page for improved performance](https://servicenow-staging.fluidtopics.net/access?context=crisis-map-migration&family=yokohama&ft:locale=en-US)**

Leverage the Crisis map functionality that includes the latest UIB components. By adopting the UIB components, you can help to minimize development efforts and get more configuration options within the Crisis map application.

You can filter alerts by their state \(active or inactive\), severity level, location \(regions\), or source. You can refine your search, perform detailed queries, or edit actions on the alerts, so that it's easier to find both the alerts and assets on the map. Additionally, you can set the secondary values such as urgency, severity, category for the alerts in the Details card.

-   **[Using nested plans](https://servicenow-staging.fluidtopics.net/access?context=creating-nested-plan-in-event&family=yokohama&ft:locale=en-US)**

Create nested plans in an event so that you can activate cross-references to multiple plans. You can use the hierarchical view to organize nested event tasks according to their dependencies with the work-breakdown structure \(WBS\) functionality. You can also monitor the progress bar to track the creation of related plans, event assets, or event tasks.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Map recovery tasks and event tasks to the phases](https://servicenow-staging.fluidtopics.net/access?context=mapping-recovery-tasks-to-phases&family=zurich&ft:locale=en-US)**

Set up phases for plans and events using the administrative setup. The base version of the application includes a set of default active phases, provided as seed data.

The logical grouping of tasks into phases enables clear progression tracking for exercises and crisis events, offering flexible execution and task completion requirements for phase transitions.

-   **[Exclude non-recovery tasks from time calculation](https://servicenow-staging.fluidtopics.net/access?context=add-a-recovery-task&family=zurich&ft:locale=en-US)**

Exclude specific recovery or event tasks from time calculations by using the **Do not include in time calculation** field within recovery or event tasks.

-   **[View and generate PDFs of approved plans](https://servicenow-staging.fluidtopics.net/access?context=mobile-bcm&family=zurich&ft:locale=en-US)**

View the continuity and recovery plans directly from your mobile devices. BCM managers can generate PDFs of the approved plans, which BCM planners can then view and download, streamlining access to critical information on the go.

-   **[Verify asset recovery levels](https://servicenow-staging.fluidtopics.net/access?context=create-new-impact-analysis-reference-form-bcm-uib-ws&family=zurich&ft:locale=en-US)**

Track event assets and verify the achieved recovery level of the impacted assets of a task in the **Asset recovery level** field. Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables coordinators to identify when dependent assets can safely start their recovery process. Color-coded recovery levels of the assets offer visual cues for various recovery progress levels.

-   **[Use finalized RTO and RPO in BIAs, Plans, and Events](https://servicenow-staging.fluidtopics.net/access?context=create-bia-in-uib-ws&family=zurich&ft:locale=en-US)**

Use the **Finalized RTO** field to calculate an accurate Recovery Time Objective \(RTO\) for comparison, using values from the **Recovery time objective** and **Adjusted RTO** fields.

Similarly, use the **Finalized RPO** field to calculate an accurate Recovery Point Objective \(RPO\) values for comparison, using values from the **Recovery point objective** and **Adjusted RPO** fields.

A fix script now populates finalized RTO and RPO values in existing Business Impact Analyses \(BIAs\), ensuring consistency across all records.

-   **[Configure recovery tasks for exercises, events, or both](https://servicenow-staging.fluidtopics.net/access?context=create-new-recovery-task-form&family=zurich&ft:locale=en-US)**

Configure recovery tasks with event-specific scopes \(exercises, actual crises, or both\). When a recovery event is initiated, the system automatically filters tasks by event type: ensuring exercises include necessary setup and validation, and actual crises focus exclusively on actionable recovery work.

-   **[Auto-calculate the Planned end date on activated plans and event tasks](https://servicenow-staging.fluidtopics.net/access?context=create-exercise-event-ref-form&family=zurich&ft:locale=en-US)**

Enter the Planned start date for exercises and events. The system then calculates the Planned start and end dates for activated plans and event tasks automatically based on the **Planned duration** field and dependencies.

-   **[Use hierarchical structure in the associated plans](https://servicenow-staging.fluidtopics.net/access?context=add-related-plans-recovery-teams-bcp-uib-ws&family=zurich&ft:locale=en-US)**

Use the hierarchical structure in the associated plans, establishing clear upstream-downstream relationships. This hierarchy confirms that only relevant downstream plans are brought into scope. The system automatically handles cyclic dependency checks, confirming that tasks from downstream plans aren’t added as dependencies in the upstream plans.

-   **[Use Gantt chart in the Hierarchy view](https://servicenow-staging.fluidtopics.net/access?context=managing-enhanced-hierarchical-view-in-event-tasks&family=zurich&ft:locale=en-US)**

Use the Gantt chart in the Hierarchy view to visualize the planned and actual timelines of event tasks. Task dependencies can now be created directly on the Gantt chart, provided the dependency points to a task scheduled ahead in time. Plans are automatically sorted based on the planned start time of their earliest event task, verifying a clear chronological view.

-   **[Generate reports in a Microsoft Word format using Document designer](https://servicenow-staging.fluidtopics.net/access?context=integrating-document-designer-with-bcm&family=zurich&ft:locale=en-US)**

Create standardized reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using predefined Microsoft Word templates. To use these templates, first establish a template relationship registry and install the necessary add-in to design and configure the templates.

Then, import the relevant documents and customize their content, including the table of contents, details, impact assessments, dependencies, and attachments, to be included in the reports. Finally, generate the reports and save them to the corresponding application records.

You can control whether to retain or replace the existing report attachments by configuring the **sn\_bcm.retain\_report\_attachments** system property.

-   **[Avoid duplicate event tasks by grouping similar event tasks](https://servicenow-staging.fluidtopics.net/access?context=identifying-running-dup-tasks-once&family=zurich&ft:locale=en-US)**

Group similar event tasks during recovery events. The system automatically designates the first event task as the original task. When the original task is in progress, the remaining tasks are placed in the **On Hold** state. After the original task is closed, the other tasks in the group are automatically marked in the **Closed duplicate** state.

Tasks with internal dependencies can't be part of the same group. You can also unlink the tasks from their groups, so that the system helps to prevent cyclic dependencies within a group.

-   **[Manage action items for ad-hoc tasks and threat assessments](https://servicenow-staging.fluidtopics.net/access?context=create-action-items-based-on-smart-assessments&family=zurich&ft:locale=en-US)**

Create action items for ad-hoc tasks and send out threat assessments that leverage Smart Assessment during exercises and crises. You can create action items for tasks that support recovery efforts, such as communicating with stakeholders, leadership, or vendors, without directly restoring an asset. Use these action items to conduct threat assessments with the Smart Assessment Engine before, during, or after a recovery event.

To enable task creation during an ongoing event, the Smart Assessment template must include both an event and an action item within its scope.

-   **[Revert an archived BIA or BCP to the Draft state](https://servicenow-staging.fluidtopics.net/access?context=create-bia-in-uib-ws&family=zurich&ft:locale=en-US)**

Revert an archived business impact analysis \(BIA\) or business continuity plan \(BCP\) to its **Draft** state by selecting the **Edit** button on the form. By revising previously completed BIAs, you save time by using a BIA that's already been created.

-   **[Optimized Crisis map interface](https://servicenow-staging.fluidtopics.net/access?context=manage-alerts-in-crisis-map-interface-uib-ws&family=zurich&ft:locale=en-US)**

The Crisis map interface has been optimized to handle over 10,000 resources and more than 1,000 alerts without performance issues.

Customize the display of impacted areas for alerts by using custom shapes or specifying a custom radius. To edit an impacted area, simply select its corresponding card and make the necessary adjustments to the shape. If needed, you can also revert the changes made to an impacted area directly within the map interface.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Business Continuity Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Using latest assessment for conducting BIAs](https://servicenow-staging.fluidtopics.net/access?context=using-smart-asmt-template&family=yokohama&ft:locale=en-US)**

You can use the latest assessment template to conduct the Business Impact Analysis \(BIA\).


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Business Continuity Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Business Continuity Management features or functionality were deprecated.

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

Install Business Continuity Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

</td></tr><tr><td>

Zurich

</td><td>

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

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

Various accessibility issues in the Crisis map application have been resolved with the implementation of the Geomap \[sn\_geo\_map\] component, which has replaced the FAM Map \[sn-fam-map\] component.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

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

 See [Business Continuity Management](https://servicenow-staging.fluidtopics.net/access?context=business-continuity-mangmt-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Set up phases in recovery tasks and event tasks for recovery event management.
-   Calculate more accurate RTO and RPO with the finalized RTO and RPO columns in BIAs, BCPs, and events.
-   View plans from the enhanced BCM Mobile application.
-   Manage templates and generate Microsoft Word reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using the Document designer add-in.
-   Avoid duplicate event tasks by identifying and grouping similar tasks in exercises and crises.
-   Create action items and send out threat assessments by leveraging Smart Assessment during exercises and crises.

 See [Business Continuity Management](https://servicenow-staging.fluidtopics.net/access?context=business-continuity-mangmt-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

