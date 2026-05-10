---
title: Enhanced Performance with UIB pages
description: The Crisis map application is now built with a UI Builder \(UIB\) page. Previously, the single-use component limited the ability to customize the user interface \(UI\), add filters, or modify the design in the Crisis map. By adopting the UIB page, you can gain full control over the implementation, enabling you to extend support for your specific use cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Structured workflows for Crisis map, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Enhanced Performance with UIB pages

The Crisis map application is now built with a UI Builder \(UIB\) page. Previously, the single-use component limited the ability to customize the user interface \(UI\), add filters, or modify the design in the Crisis map. By adopting the UIB page, you can gain full control over the implementation, enabling you to extend support for your specific use cases.

## Limitations of a single-use component

The single-use component used in prior releases of Crisis map had several limitations.

-   Lack of configuration flexibility: The component wasn’t open for configuration, limiting options to customize the user interface \(UI\).
-   Limited customization options: It restricted the ability to change the design of elements such as cards, add different filters or sorting options, or update other features on the page.
-   Restricted tailoring: It limited the ability to tailor the application to meet specific needs.

## Benefits of adopting the UIB page

Adopting the UIB page in the Crisis map application offers these benefits:

-   **Configuration flexibility**

    The UIB page provides full control over the implementation, and enables you to extend it for your own use case. It also helps you to minimize development efforts and offers more configuration options. You can filter alerts based on their state \(active or inactive\), severity level, location \(regions\), and source. This setup enables you to fine-tune details, perform searches, and edit actions on the alerts, making it easier to locate both alerts and assets on the map. Additionally, you can set secondary values for the alerts in the Details card.

-   **Accessibility**

    The previous FAM Map \[sn-fam-map\] component was outdated and no longer received updates or defect fixes. It also had accessibility issues. The Geomap component addresses these accessibility issues, enables new feature development, and replaces the deprecated FAM Map component.


## Filters and actions on the alerts

Filters on the map, such as states, regions, and severity, enhance alert visibility. Previously, you could only filter between active and dismissed alerts. Now, you have more options to filter the alerts as shown in the example.

![Filters.](../image/alert-filters.png)

1.  **Alert states**: Filter alerts by their states such as Active alerts or Dismissed alerts.
2.  **Alert regions**: Filter alerts by their region, for example, AMS, APJ, and EMEA.
3.  **Alert severities**: Filter alerts by their severity, for example, 1 - Extreme, 2 - Severe, 3 - Moderate, 4 - Minor, 5 - Unknown.
4.  Search functionality: Filter alerts by searching multiple fields.
    -   Source: Searching for the source such as GDAC shows all alerts from the GDAC feed.
    -   Alert name: Search for specific alert names, for example, Madagascar Star.
    -   Severity: Search alerts by their severity level such as Extreme, Severe, Moderate, Minor, or Unknown alerts.
    -   Description: Search an alert by its specific description or by using a phrase from the description. For example, searching for Level of strength shows you alerts that include this phrase in their description.

These new filters and search options provide more flexibility and control over the alerts that are displayed on the page.

The Crisis map application now includes enhanced actions such as listing alerts, sorting by severity, and displaying assets according to their locations, vendors, datacenters, as shown in the illustration.

![Enhanced actions in the map UI.](../image/new-crisis-map.png)

Actions: Perform these actions on the alerts in the map.

-   Select the **Sort by** option to sort the alerts by their **Severity**, **Created**, and **Updated** options. You can also use the sorting icon ![Sort.](../image/ChangeSortOrderIcon.png) to sort the alerts in an ascending or descending order.
-   Select the ![Subscribe.](../image/SubscribeIcon.png) icon to subscribe to an alert. A subscription notification, such as `Alert subscribed: Drought is ongoing in Madagascar` is displayed on the screen.
-   Select the ![More options.](../../grc-workspace-risk/image/more-details.png) icon to open or dismiss an alert. Actions related to an alert are recorded and displayed in the Activity panel of the alert record.

## Resource configuration

Custom icons and fields: The resources on the map such as Locations or vendors are defined in the BCM element definition table, with options to specify icons, tables, and location fields. You can update the element definition record to add a resource as shown in the example, which adds the datacenters resource to the map.

![Creating a resource configuration for an element definition.](../image/resrc-config-ele-def-record.png)

Only active resources within the BCM category are displayed. You can also configure which fields are displayed when a resource, such as the name, location, and additional information, is selected.

The **Display Fields** in the resource configuration are used to customize the information shown on the map. You can add fields such as **Assigned to** and **Category** to show the person assigned to the datacenter and the categories. You can also remove fields that are no longer needed. Additionally, you can add filter conditions to show only the records that match your specific criteria. For example, setting a filter for a specific name displays only the datacenters that match that name as shown in the example.

![Sample resource configuration.](../image/resource-display-fields.png)

This condition helps you to view relevant fields and analyze a focused view of the data in the map.

![Alerts page in Crisis map.](../image/resource-display-fields-map-view.png)

Starting with BCM release 9.0.x, the Crisis map application has been enhanced. You can now display more than 10,000 resources on the map. Similarly, the application handles more than 1,000 alerts without any performance issues.

For information on creating a Resource configuration in Crisis map, see [Configure Resource Configuration records](../task/conf-resource-for-crisis-map-uib-ws.md).

## Alert details page

When you select an alert, the map zooms into a smaller area centered on the latitude and longitude of the alert, providing a focused view of the specific location.

In the alert details, additional information on the alert is listed.

1.  Alert name
2.  Secondary values such as urgency, severity, category of an alert.

Configurable secondary values: You can now customize the secondary values displayed on the alert details page to better suit your needs. These configurable fields—such as urgency, severity, and category—enable you to add more information to the display. The secondary values that you configure apply to all alerts in the list.

![Alert details view.](../image/alert-details-view.png)

You can configure these secondary values by navigating to **UX Header Configuration** &gt; **BCM Workspace** &gt; **UX Form Headers \(sn\_fam\_alert\)**. You can select the alert that you want to modify and choose which secondary values you want to display or remove as shown in the sample configuration.

![UX header configuration.](../image/alert-header.png)![New record for a secondary value.](../image/alert-sec-value.png)

For information on the form headers, see [Configure a form header for a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/config-ws-form-header.md).

The 'Assets at Risk' section is displayed on the **Details** tab of an alert. The **Response Tasks** tab shows secondary values such as the Response task number, Title, State, Assigned to, Created. The 'Assets at Risk' section, as shown in the example, provides an overview of all assets associated with an alert. You can view the at-risk assets by selecting each element definition, to monitor which assets are at risk for a specific alert.

![Assets at Risk section in the map.](../image/assets-at-risk.png)

The suggested actions for an alert are displayed in the Alert panel. These actions include steps like notifying stakeholders \(with a feature to send emails\), creating response tasks, and clearing crisis events. Custom alert actions can also be implemented using scripts.

Zoom and focus options in the map: Selecting on an alert zooms the map to a smaller area centered on the alert's location.

Starting with BCM release 9.0.x, pagination has been added for alerts, which improves readability for the users.

## Custom alert actions

You can add custom alert actions by searching for them in the Alert Actions section. Two base system alert actions are provided, which include a model for user input. For custom alert actions, you can implement your own scripts, but currently, these scripts run without any input or custom model.

For example, if you select the **Test Script** action, it runs a script without any input. You can check the log to confirm that the script has been executed. The log shows a message indicating that the test script alert action has run.

You can add custom scripts for alert actions, and the system supports both base system and custom actions. This migration promotes better configuration, accessibility, and future support for the Crisis map application for the users. For information on alert actions, see [Configure alert actions](../task/configure-alert-action-uib-ws.md).

## Enhanced accessibility and user experience

The implementation of the Geomap \[sn\_geo\_map\] component has resolved various accessibility issues from previous Crisis map releases. This component replaces the FAM Map \[sn-fam-map\] component and provides an enhanced user experience.

**Parent Topic:**[Structured workflows for Crisis map](crisis-map-collective-tasks.md)

