---
title: View and manage alerts in the crisis map interface
description: Business Continuity Management integrates with the Crisis Map to provide you the capability of identifying a threat and its geolocation from your asset locations.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Crisis Management map, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# View and manage alerts in the crisis map interface

Business Continuity Management integrates with the Crisis Map to provide you the capability of identifying a threat and its geolocation from your asset locations.

## Before you begin

It not only helps you to identify a threat as a business crisis but also notify your stakeholders and declare it as a crisis event if it has the potency to disrupt your business.

**Note:** Activate the Business Crisis Management Map \(sn-crisis-map\) application for the crisis map feature.

Role required: BCM admin or BCM Program Manager

## About this task

Use the crisis map to manage feeds, prioritize alerts based on their severity, and create events. Thereafter, you can run the Crisis Management workflow and activate the business continuity and recovery plans for the locations impacted by the event.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the map icon \(![Crisis map icon.](../image/CrisisMapIcon.png)\).

    The alerts section is on the left of the workspace and the map view is on the right.

    |Alert control feature|Description|
    |---------------------|-----------|
    |Search Alerts|Key word to search and filter alerts from the list.|
    |Select active or dismissed alerts|List to select either active or dismissed alerts. When an alert is dismissed, it becomes inactive.|
    |Select column to sort by|List to select and display alerts based on their severity, created, or updated date.|
    |Change sort order \(![Change sort order icon.](../image/ChangeSortOrderIcon.png)\)|Sorting order of the alerts, either in ascending or descending order.|
    |Refresh Alerts \(![Refresh alerts icon.](../image/RefreshAlertsIcon.png)\)|Option to refresh the alert list and the map components after an update.|

    Threat alerts, based on severity or in any sorting order that you have set, are displayed in a list view. As you point to an alert in the list of alerts, you can view additional details about the impact of the threat.

    Each alert record in the list has these details:

    ![Alert record in the alert list.](../image/AlertRecordMap.png "Alert record in the alert list")

    -   **Title**

        Name of the alert.

    -   **Description**

        Brief note about the impact of the alert.

    -   **Severity**

        Intensity of the threat impact. It can be extreme, severe, moderate, minor, or unknown.

    -   **Updated details**

        The alert's last updated date and timestamp.

3.  Click an alert record to open the alert in its detailed view and view its corresponding impacted area on the map.

4.  To go back to the list view of alerts, click the **Back** button.

5.  To open the alert details in the form view, click the **Open Alert** option in the alert menu icon \(![Alert menu icon.](../image/AlertMenuIcon.png)\).

    This action opens the record in a separate **Details** tab.

6.  To go back to the alert list, click the **Map** tab.

7.  If the alert does not pose a threat currently to your employee locations, datacenters, core companies, or any of your business establishments, click the **Dismiss Alert** option in the alert menu.

    If you know that the alert would not hamper your business operations, you can dismiss it in the list view as well as in its detailed view. When you dismiss an alert in the list view, it is removed from the list. If you dismiss an alert from the detailed view, the alert is removed and brings you back to the list view so that you can review the other alerts in the list. In both cases, you can see a confirmation message about the dismissal of the alert.

8.  To subscribe to the alert notifications, click the subscribe icon \(![Subscribe icon.](../image/SubscribeIcon.png)\).

    You receive an email and workspace notifications every time the alert or its source feed item is updated.


**Parent Topic:**[Crisis Management map](../concept/crisis-management-map-integration.md)

