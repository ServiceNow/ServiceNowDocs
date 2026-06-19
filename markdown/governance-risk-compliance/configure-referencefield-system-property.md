---
title: Update number of records for reference fields
description: Update the number of the records that are displayed for a reference field in the Business Continuity Management \(BCM\) Workspace. You can configure the referenceFieldLoadLimit system property to control the number of the records that are displayed for each reference field on the grid configuration pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-referencefield-system-property.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup by system administrators, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Update number of records for reference fields

Update the number of the records that are displayed for a reference field in the Business Continuity Management \(BCM\) Workspace. You can configure the **referenceFieldLoadLimit** system property to control the number of the records that are displayed for each reference field on the grid configuration pages.

## Before you begin

Role required: admin

## About this task

You can configure the **referenceFieldLoadLimit** system property for the reference fields on these tabs:

-   **RTO Impact Assessment** tab, **RPO Impact Assessment** tab, and **Dependency Assessment** tab in a Business Impact Analysis
-   **Recovery Tasks** tab in a Plan
-   **Impacts** tab and **Event Tasks** tab in an Exercise

## Procedure

1.  Navigate to **All** &gt; **sys\_declarative\_action\_assignment.list** in the BCM application instance.

    A list view of the Action Assignments table is displayed as shown in the example.

    \[Omitted image "prop-update-action-assignments-table.png"\] Alt text: Action assignments table.

2.  In the **Action label** column, enter the name of the assessment action and select the assessment.

    A sample search string for the assessment is displayed in the example.

    \[Omitted image "prop-update-dependency-assessment-action-label-column.png"\] Alt text: Action label column.

    When you select the assessment, the form view of the Action Assignment table is displayed as shown in the example.\[Omitted image "prop-update-advanced-view-action-assignment-table.png"\] Alt text: Form view for the selected action.

3.  In the form view of the Action Assignment table, select **Advanced View**.

    After you’ve selected the **Advanced View**, the properties for the selected action are displayed in the **Component Attributes** tab as shown in the example.

    \[Omitted image "prop-update-componentattributes.png"\] Alt text: Component attributes.

    An informational message is displayed on the screen: `To edit this record, click Here.`

4.  To update the **referenceFieldLoadLimit** property for the selected record, select **Here** in the informational message.

    By updating the **referenceFieldLoadLimit** property, you can control the number of the records on the grid configuration page.

    A sample configuration of the **referenceFieldLoadLimit** property is displayed in the example.

    \[Omitted image "prop-update-configured-value.png"\] Alt text: Sample configuration of the property.

5.  Select **Update**.

    You’ve configured the **referenceFieldLoadLimit** property for the selected assessment as shown in the example. \[Omitted image "configured-value.png"\] Alt text: Property set for the assessment.

    **Note:** As outlined in the context of this task, you can set the **referenceFieldLoadLimit** property to control the number the reference fields on different grid configuration pages.

    The example shows the updated number of the records for the **Disruption Duration** field in the **RTO Impact Assessment** tab.

    \[Omitted image "prop-update-updated-value-on-the-screen.png"\] Alt text: Sample display of the records.


**Parent Topic:**[Setup by system administrators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/set-up-bcm-sys-admin-tasks.md)

