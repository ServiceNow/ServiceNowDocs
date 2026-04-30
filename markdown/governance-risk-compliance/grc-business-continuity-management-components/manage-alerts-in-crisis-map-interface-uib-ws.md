---
title: Manage alerts from the map interface
description: Manage alerts from the Crisis map interface to identify threats and their geo-locations relative to your assets. You can open alerts for details, dismiss them when resolved, adjust the impacted area boundaries, or undo recent changes.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Structured workflows for Crisis map, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Manage alerts from the map interface

Manage alerts from the Crisis map interface to identify threats and their geo-locations relative to your assets. You can open alerts for details, dismiss them when resolved, adjust the impacted area boundaries, or undo recent changes.

## Before you begin

Role required: sn\_bcm.admin or sn\_bcm.program\_manager

## About this task

The Crisis map interface has been optimized to handle over 10,000 resources and more than 1,000 alerts without performance issues.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select the **Crisis map** icon in the list view.

2.  Select an alert record.

    **Note:** Starting with BCM release 9.0.x and later, pagination has been added for alerts, which improves readability for the users.

    This action opens the alert record in the **Alerts** panel. You can view the details of the record in the header of the record.

    In the **Details** tab, you can view the assets at risk in the **Assets at Risk** section. You can view the suggested actions such as **Notify Stakeholders** or **Declare a Crisis Event** in the **Suggested Actions** section.

    You can open the detailed view of an alert and view its corresponding impacted area on the map as shown in the example.![Alerts view in Crisis map.](../image/alert-view-in-crisis-map.png)

3.  Open the alert details in the form view by selecting the **Open Alert** option in the **Alert menu** icon \(![Alert menu icon.](../image/AlertMenuIcon.png)\).

    This action opens the record on a separate **Details** tab as shown in the example.

    ![Alerts form.](../image/alerts-record-details-tab.png)

4.  View the response tasks associated with the alert in the **Response Tasks** tab.

5.  Monitor the activity on the alert and add your comments in the **Compose** section of the **Activity** tab.

6.  Sort the alerts with the **Sort by** option.

    You can sort the alerts by their **Severity**, **Created**, and **Updated** options. You can also use the sorting icon ![Sort.](../image/ChangeSortOrderIcon.png) to sort the alerts in an ascending or descending order.

7.  Subscribe to an alert using the ![Subscribe.](../image/SubscribeIcon.png) icon.

    When an alert or its source feed item is updated, you receive the workspace notification, such as `Alert subscribed: Drought is ongoing in Madagascar`, which is displayed on the screen.

8.  Open an alert with the **Open alert** option in the ![More options.](../../grc-workspace-risk/image/more-details.png) icon.

    The alert form is displayed. If you want to edit the alert, you can make necessary changes and select **Save**.

9.  Dismiss an alert using the **Dismiss alert** option in the ![More options.](../../grc-workspace-risk/image/more-details.png) icon.

    If the alert doesn’t pose a threat currently to your employee locations, datacenters, core companies, or any of your business establishments, you can dismiss the alert. If you know that the alert wouldn’t hamper your business operations, you can dismiss it in the list view as well as in its detailed view.

    When you dismiss an alert in the list view, it’s removed from the list. When you dismiss an alert from the detailed view, it's removed and you return to the list view to review the remaining alerts. In both cases, you can see a confirmation message about the dismissal of the alert.

    A message is displayed on the screen that the alert is dismissed.

10. Edit an impacted area using the **Alert menu** icon.

    1.  Select the **Edit Impact Area** option.

    2.  In the Edit Impacted Area pop over that opens on the map, select either **Custom Shape** or **Custom Radius** depending on the shape of the impacted area.

        -   Select **Custom Shape** if the impacted area is polygonal shape.
        -   Select **Custom Radius** if the impacted area is a circle.
    3.  Select and drag the vertex on the boundary of the impacted area to include the asset location.

    4.  Select **Save**.

    5.  To revert the impacted area, select the **More options** icon and select **Revert impacted area**.


**Parent Topic:**[Structured workflows for Crisis map](../concept/crisis-map-collective-tasks.md)

