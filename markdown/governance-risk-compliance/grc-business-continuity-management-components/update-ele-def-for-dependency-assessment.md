---
title: Update the number of element definitions
description: Update the number of the element definitions that are displayed on the Dependency Assessment tab in the Business Continuity Management \(BCM\) Workspace. You can configure the dependencyAssessmentElementsLimit system property to control the number of the element definitions that are used for the dependency assessment in a business impact analysis.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup by system administrators, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Update the number of element definitions

Update the number of the element definitions that are displayed on the **Dependency Assessment** tab in the Business Continuity Management \(BCM\) Workspace. You can configure the **dependencyAssessmentElementsLimit** system property to control the number of the element definitions that are used for the dependency assessment in a business impact analysis.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_declarative\_action\_assignment.list** in the BCM application instance.

    A list view of the Action Assignments table is displayed as shown in the example.

    ![Action assignments table.](../image/prop-update-action-assignments-table.png)

2.  In the **Action label** column, enter the name of the assessment such as **Dependency Assessment** and select the assessment.

    A sample text string is displayed in the example.

    ![Action label column.](../image/prop-update-dependency-assessment-action-label-column.png)

    When you select the assessment, the form view of the Action Assignment table is displayed as shown in the example.

    ![Dependency Assessment action.](../image/prop-update-advanced-view-action-assignment-table.png)

3.  In the form view of the Action Assignment table, select **Advanced View**.

    After you’ve selected the **Advanced View**, the properties for the selected action are displayed in the **Component Attributes** tab as shown in the example.

    ![Component attributes.](../image/prop-update-componentattributes.png)

    An informational message is displayed on the screen: `To edit this record, click Here.`

4.  To update the **dependencyAssessmentElementsLimit** property, select **Here** in the informational message.

    By updating the **dependencyAssessmentElementsLimit** property, you can control the number of the element definitions for the dependency assessment.

    A sample configuration of the **dependencyAssessmentElementsLimit** property is displayed in the example.

    ![Sample configuration of the property.](../image/configuration-of-element-definition.png)

5.  Select **Update**.

    You’ve configured the **dependencyAssessmentElementsLimit** property as shown in the example.

    ![Sample display of the property.](../image/configured-element-def.png)

    The updated number of the element definitions are displayed on the **Dependency Assessment** tab.


**Parent Topic:**[Setup by system administrators](../concept/set-up-bcm-sys-admin-tasks.md)

