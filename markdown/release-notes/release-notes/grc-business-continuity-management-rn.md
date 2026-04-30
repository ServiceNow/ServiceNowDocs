---
title: Business Continuity Management release notes
description: The ServiceNow Business Continuity Management application enables your organization to deliver products and services at an acceptable level during disruptive incidents. Business Continuity Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
---

# Business Continuity Management release notes

The ServiceNow® Business Continuity Management application enables your organization to deliver products and services at an acceptable level during disruptive incidents. Business Continuity Management was enhanced and updated in the Zurich release.

## Business Continuity Management highlights for the Zurich release

-   Set up phases in recovery tasks and event tasks for recovery event management.
-   Calculate more accurate RTO and RPO with the finalized RTO and RPO columns in BIAs, BCPs, and events.
-   View plans from the enhanced BCM Mobile application.
-   Manage templates and generate Microsoft Word reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using the Document designer add-in.
-   Avoid duplicate event tasks by identifying and grouping similar tasks in exercises and crises.
-   Create action items and send out threat assessments by leveraging Smart Assessment during exercises and crises.

See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Business Continuity Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Business Continuity Management release

-   **[Map recovery tasks and event tasks to the phases](https://www.servicenow.com/docs/access?context=mapping-recovery-tasks-to-phases&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Set up phases for plans and events using the administrative setup. The base version of the application includes a set of default active phases, provided as seed data.

    The logical grouping of tasks into phases enables clear progression tracking for exercises and crisis events, offering flexible execution and task completion requirements for phase transitions.

-   **[Exclude non-recovery tasks from time calculation](https://www.servicenow.com/docs/access?context=add-a-recovery-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Exclude specific recovery or event tasks from time calculations by using the **Do not include in time calculation** field within recovery or event tasks.

-   **[View and generate PDFs of approved plans](https://www.servicenow.com/docs/access?context=mobile-bcm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    View the continuity and recovery plans directly from your mobile devices. BCM managers can generate PDFs of the approved plans, which BCM planners can then view and download, streamlining access to critical information on the go.

-   **[Verify asset recovery levels](https://www.servicenow.com/docs/access?context=create-new-impact-analysis-reference-form-bcm-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Track event assets and verify the achieved recovery level of the impacted assets of a task in the **Asset recovery level** field. Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables coordinators to identify when dependent assets can safely start their recovery process. Color-coded recovery levels of the assets offer visual cues for various recovery progress levels.

-   **[Use finalized RTO and RPO in BIAs, Plans, and Events](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use the **Finalized RTO** field to calculate an accurate Recovery Time Objective \(RTO\) for comparison, using values from the **Recovery time objective** and **Adjusted RTO** fields.

    Similarly, use the **Finalized RPO** field to calculate an accurate Recovery Point Objective \(RPO\) values for comparison, using values from the **Recovery point objective** and **Adjusted RPO** fields.

    A fix script now populates finalized RTO and RPO values in existing Business Impact Analyses \(BIAs\), ensuring consistency across all records.

-   **[Configure recovery tasks for exercises, events, or both](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Configure recovery tasks with event-specific scopes \(exercises, actual crises, or both\). When a recovery event is initiated, the system automatically filters tasks by event type: ensuring exercises include necessary setup and validation, and actual crises focus exclusively on actionable recovery work.

-   **[Auto-calculate the Planned end date on activated plans and event tasks](https://www.servicenow.com/docs/access?context=create-exercise-event-ref-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Enter the Planned start date for exercises and events. The system then calculates the Planned start and end dates for activated plans and event tasks automatically based on the **Planned duration** field and dependencies.

-   **[Use hierarchical structure in the associated plans](https://www.servicenow.com/docs/access?context=add-related-plans-recovery-teams-bcp-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use the hierarchical structure in the associated plans, establishing clear upstream-downstream relationships. This hierarchy confirms that only relevant downstream plans are brought into scope. The system automatically handles cyclic dependency checks, confirming that tasks from downstream plans aren’t added as dependencies in the upstream plans.

-   **[Use Gantt chart in the Hierarchy view](https://www.servicenow.com/docs/access?context=managing-enhanced-hierarchical-view-in-event-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use the Gantt chart in the Hierarchy view to visualize the planned and actual timelines of event tasks. Task dependencies can now be created directly on the Gantt chart, provided the dependency points to a task scheduled ahead in time. Plans are automatically sorted based on the planned start time of their earliest event task, verifying a clear chronological view.

-   **[Generate reports in a Microsoft Word format using Document designer](https://www.servicenow.com/docs/access?context=integrating-document-designer-with-bcm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Create standardized reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using predefined Microsoft Word templates. To use these templates, first establish a template relationship registry and install the necessary add-in to design and configure the templates.

    Then, import the relevant documents and customize their content, including the table of contents, details, impact assessments, dependencies, and attachments, to be included in the reports. Finally, generate the reports and save them to the corresponding application records.

    You can control whether to retain or replace the existing report attachments by configuring the **sn\_bcm.retain\_report\_attachments** system property.

-   **[Avoid duplicate event tasks by grouping similar event tasks](https://www.servicenow.com/docs/access?context=identifying-running-dup-tasks-once&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Group similar event tasks during recovery events. The system automatically designates the first event task as the original task. When the original task is in progress, the remaining tasks are placed in the **On Hold** state. After the original task is closed, the other tasks in the group are automatically marked in the **Closed duplicate** state.

    Tasks with internal dependencies can't be part of the same group. You can also unlink the tasks from their groups, so that the system helps to prevent cyclic dependencies within a group.

-   **[Manage action items for ad-hoc tasks and threat assessments](https://www.servicenow.com/docs/access?context=create-action-items-based-on-smart-assessments&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Create action items for ad-hoc tasks and send out threat assessments that leverage Smart Assessment during exercises and crises. You can create action items for tasks that support recovery efforts, such as communicating with stakeholders, leadership, or vendors, without directly restoring an asset. Use these action items to conduct threat assessments with the Smart Assessment Engine before, during, or after a recovery event.

    To enable task creation during an ongoing event, the Smart Assessment template must include both an event and an action item within its scope.

-   **[Revert an archived BIA or BCP to the Draft state](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Revert an archived business impact analysis \(BIA\) or business continuity plan \(BCP\) to its **Draft** state by selecting the **Edit** button on the form. By revising previously completed BIAs, you save time by using a BIA that's already been created.

-   **[Optimized Crisis map interface](https://www.servicenow.com/docs/access?context=manage-alerts-in-crisis-map-interface-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Crisis map interface has been optimized to handle over 10,000 resources and more than 1,000 alerts without performance issues.

    Customize the display of impacted areas for alerts by using custom shapes or specifying a custom radius. To edit an impacted area, simply select its corresponding card and make the necessary adjustments to the shape. If needed, you can also revert the changes made to an impacted area directly within the map interface.


## UI changes

-   **[Configuring the phases](https://www.servicenow.com/docs/access?context=set-up-phases&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Active phases module is available in the General Administration setup for configuring the phases.

-   **[Phase column](https://www.servicenow.com/docs/access?context=add-a-recovery-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The recovery and event tasks now include the Phase column in the list and form views, indicating association with specific phases within the recovery process.

-   **[Do not include tasks in time calculation](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The **Do not include tasks in time calculation** field has been added to Recovery tasks, enabling you to exclude specific tasks from overall time calculations.

-   **[Asset recovery level column](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Asset recovery level column is added to the recovery tasks to indicate recovery levels of the assets.

-   **[Include task in field](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The **Include task in** field is added in the recovery tasks to specify whether a task should be included in an exercise, crisis event, or both.

-   **[Finalized RTO and RPO](https://www.servicenow.com/docs/access?context=create-new-impact-analysis-reference-form-bcm-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Finalized RTO column is shown in the chart and list views, replacing the previously shown RTO and Adjusted RTO columns. Similarly, the Finalized RPO column is shown in the chart and list views, replacing the previously shown RPO and Adjusted RPO columns.

-   **[Associated plans tab](https://www.servicenow.com/docs/access?context=add-related-plans-recovery-teams-bcp-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The **Associated plans** tab in the Plan record replaces the **Related plan** and **Parent plan** tabs. Upstream, Downstream, and Related plans are now included as associated plan types.

-   **[Gantt chart in the Hierarchy view](https://www.servicenow.com/docs/access?context=managing-enhanced-hierarchical-view-in-event-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    A Gantt chart has been added to the Hierarchy view to help visualize the planned and actual timelines of event tasks.

-   **[Predefined Word templates](https://www.servicenow.com/docs/access?context=edit-report-temp&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Predefined Microsoft Word templates are now provided in the instance.

-   **[Similar tasks group tab](https://www.servicenow.com/docs/access?context=identifying-running-dup-tasks-once&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The **Similar tasks groups** tab is now included in the events and the **Create similar tasks group** UI action is available in the **Event tasks** tab.

-   **[Action items tab in Exercises and Crises modules](https://www.servicenow.com/docs/access?context=create-action-items-based-on-smart-assessments&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The **Action items** tab is now available in both exercises and crises.

-   **[Pagination for alerts](https://www.servicenow.com/docs/access?context=manage-alerts-in-crisis-map-interface-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Pagination has been added to alerts in Crisis map, to make them more readable on the map interface.

    Edit the impacted area of an alert by using custom shapes or a custom radius. Similarly, you can revert the changes made to an impacted area within the map interface.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install Business Continuity Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

