---
title: Visualize 360° relationships for BIAs
description: Visualize the 360° relationships for a business impact analysis and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating a business impact analysis.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Visualize 360° relationships for BIAs

Visualize the 360° relationships for a business impact analysis and its associated entities in BCM UIB Workspace. You can access the 360° view at any time while creating a business impact analysis.

## Before you begin

Role required: sn\_bia.bia\_admin, sn\_bcm.program\_manager, sn\_bcm.planner

## About this task

The configurations for the 360° view are stored in **360° View Configurations** &gt; **Configure 360° Views**. If you have the BCM administrator role, you can configure the relationships for the records in **360° View Configurations** &gt; **Relationship Registries**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Business Impact Analysis** and select a record from the list.

    The business impact analysis record is displayed.

3.  Select **360° view**.

    You can select **360° view** to view the relationships for a BIA as shown in the example.

    ![360° view for a business impact analysis.](../image/360-bia-action-button.png)

    The example shows the 360° view of a business impact analysis and its details.

    ![360° view for a BIA record.](../image/360-bia.png)

    The 360° view for the business impact analysis shows these details:

    -   **Impact Analysis**: Name of the business impact analysis such as My Service Importance Assessment.
    -   **Applies to**: Entity that the business impact analysis applies to such as Business process or Business service.
    -   **Template**: BIA template details such as the name of the template and its description. You can select the **BIA template** capsule and view the details of the BIA template.
    -   **Depends on**: Dependencies associated with the business impact analysis. You can select the **Depends on** capsule and view its details.
4.  Select **BIA template** in the view.

    The details of the BIA template such as the name and description of the template are displayed in the right panel of the view as shown in the example.

    ![360-bia-template.](../image/360-bia-bia-template.png)

5.  Select **Depends on** in the view.

    The details of the dependencies are displayed in the right panel of the view as shown in the example.

    ![360-dependencies.](../image/360-bia-dependencies.png)

6.  Select **Vendors** in the view.

    The details of the vendors are displayed in the right panel of the view as shown in the example.

    ![360-vendors.](../image/360-bia-vendors.png)

7.  To navigate to the BIA again, select the BIA or list view in the breadcrumb navigation on the page.


**Parent Topic:**[Structured workflows for BIAs](../concept/bia-tasks-performed-by-bia-owner.md)

