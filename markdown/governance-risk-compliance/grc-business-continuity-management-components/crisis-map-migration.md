---
title: Adopting UIB page for improved performance
description: Beginning with the Yokohama release, the Crisis map application is now built with a UI Builder \(UIB\) page. Previously, the single-use component limited the ability to customize the user interface \(UI\), add filters, or modify the design in the Crisis map. By adopting the UIB page, you can gain full control over the implementation, enabling you to extend support for your specific use cases.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Structured workflows for Crisis map, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Adopting UIB page for improved performance

Beginning with the Yokohama release, the Crisis map application is now built with a UI Builder \(UIB\) page. Previously, the single-use component limited the ability to customize the user interface \(UI\), add filters, or modify the design in the Crisis map. By adopting the UIB page, you can gain full control over the implementation, enabling you to extend support for your specific use cases.

## Limitations of a single-use component used in prior releases

The single-use component in the Crisis map application had several limitations.

-   Lack of configuration flexibility: The component was not open for configuration, limiting options to customize the user interface \(UI\).
-   Limited customization options: It restricted the ability to change the design of elements such as cards, add different filters or sorting options, or update other features on the page.
-   Restricted tailoring: It limited the ability to tailor the application to meet specific needs.

## Benefits of adopting the UIB page

Adopting the UIB page in the Crisis map application offers the following benefits.

-   **Configuration flexibility**

    The UIB page provides full control over the implementation, and enables you to extend it for your own use case. It also helps you to minimize development efforts and offers more configuration options. You can filter alerts based on their state \(active or inactive\), severity level, location \(regions\), and source. This setup enables you to fine-tune details, perform searches, and edit actions on the alerts, making it easier to locate both alerts and assets on the map. Additionally, you can set secondary values for the alerts in the Details card.

-   **Accessibility**

    The FAM Map \[sn-fam-map\] component used earlier for the map was outdated and no longer supported new updates or defect fixes. It also had various accessibility issues. Replace the FAM Map \[sn-fam-map\] component with the Geomap component addresses these accessibility issues and enables for the implementation of new features, as the old component has been deprecated.


## Actions on the alerts

The Crisis map application now includes enhanced functionality such as listing alerts, sorting by severity, and displaying resources such as locations, vendors, datacenters, as shown in the illustration.

![Map UI.](../image/new-crisis-map.png)

Actions on the alerts: You can perform the following actions on the alerts in the map:

-   Select the **Sort by** option to sort the alerts by their **Severity**, **Created**, and **Updated** options. You can also use the sorting icon ![Sort.](../image/ChangeSortOrderIcon.png) to sort the alerts in an ascending or descending order.
-   Select the ![Subscribe.](../image/SubscribeIcon.png) icon to subscribe to an alert. A subscription notification, such as `Alert subscribed: Drought is ongoing in Madagascar` is displayed on the screen.
-   Select the ![More options.](../../grc-workspace-risk/image/more-details.png) icon to open or dismiss an alert. Actions related to an alert are recorded and displayed in the Activity panel of the alert record.

## Additional filters for the alerts

Additional filters on the map, such as region and severity, enhance alert visibility. Previously, you could only filter between active and dismissed alerts. Now, you have more options to filter the alerts as shown in the example.

![Filters.](../image/alert-filters.png)

1.  Alert states: Filter alerts by their states such as Active alerts or Dismissed alerts.
2.  Alert regions: Filter alerts by region, for example, Americas or both Americas and EMEA.
3.  Alert severities: Filter alerts by severity, for example, red or both red and yellow.
4.  Search functionality: Filter alerts by searching multiple fields.
    -   Source: Searching for the source such as GDAC shows all alerts from the GDAC feed.
    -   Alert name: Search for specific alert names, for example, Madagascar Star.
    -   Severity: Search alerts by their severity level such as Extreme, Severe, Moderate, Minor, or Unknown alerts.
    -   Description: Search an alert by its specific description or by using a phrase from the description. For example, searching for Level of strength shows you alerts that include this phrase in their description.

These new filters and search options provide more flexibility and control over the alerts that are displayed on the page.

## Resource configuration

Custom icons and fields: The resources on the map such as Locations or vendors are defined in the BCM element definition table, with options to specify icons, tables, and location fields. You can update the element definition record to add a resource as shown in the example, which adds the Datacenters resource to the map.

![Resource configuration.](../image/resrc-config-ele-def-record.png)

Only active resources within the BCM category are displayed. You can also configure which fields are displayed when a resource, such as the name, location, and additional information, is selected.

The **Display Fields** in the resource configuration are used to customize the information shown on the map. You can add fields such as **Assigned to** and **Category** to show the person assigned to the data center and the categories. You can also remove fields that are no longer needed. Additionally, you can add filter conditions to show only the records that match your specific criteria. For example, setting a filter for a specific name displays only the data centers that match that name as shown in the example.

![Resource configuration.](../image/resource-display-fields.png)

This condition helps you to view relevant fields and analyze a focused view of the data in the map.

![Map view.](../image/resource-display-fields-map-view.png)

Starting with BCM release 9.0.x, the Crisis map application has been enhanced. You can now display more than 10,000 resources on the map. Similarly, the application handles more than 1,000 alerts without any performance issues.

For information on creating a Resource configuration in Crisis map, see [Configure Resource Configuration records](../task/conf-resource-for-crisis-map-uib-ws.md).

## Alert details page

When you select an alert, the map zooms into a smaller area centered on the latitude and longitude of the alert, providing a focused view of the specific location.

In the alert details, additional information on the alert is listed.

1.  Alert name
2.  Secondary values, similar to those in the Workspace.

Starting with BCM release 9.0.x, pagination has been added for alerts, which improves readability for the users.

These secondary values are now configurable. Previously, they were fixed, but you can now customize them to better suit your needs.

![Details view.](../image/alert-details-view.png)

You can configure these secondary values by navigating to **UX Header Configuration** &gt; **BCM Workspace** &gt; **UX Form Headers \(sn\_fam\_alert\)**. You can select the alert that you want to modify and choose which secondary values you want to display or remove as shown in the sample configuration.

![Header.](../image/alert-header.png)![Secondary value.](../image/alert-sec-value.png)

For information on the form headers, see [Set up a form header in Configurable Workspace](https://www.servicenow.com/docs/access?context=config-ws-form-header&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

Zoom and focus: Selecting on an alert zooms the map to a smaller area centered on the alert's location.

Configurable secondary values: The alert details page now includes configurable secondary values, such as urgency, severity, category, enabling you to add more fields to the display. The secondary values are applied to all the alerts in the list.

The Assets at Risk section is displayed on the **Details** tab of an alert. The **Response Tasks** tab shows secondary values such as the Response task number, Title, State, Assigned to, Created.

The Assets at Risk section as shown in the example provides an overview of all assets associated with an alert. You can view the at-risk assets by selecting each element definition, to monitor which assets are at risk for a specific alert.

![Assets.](../image/assets-at-risk.png)

The suggested actions for an alert are displayed in the Alert panel. These actions include steps like notifying stakeholders \(with a feature to send emails\), creating response tasks, and clearing crisis events. Custom alert actions can also be implemented using scripts.

## Custom alert actions

You can add custom alert actions by searching for them in the Alert Actions section. Two base system alert actions are provided, which include a model for user input. For custom alert actions, you can implement your own scripts, but currently, these scripts run without any input or custom model.

For example, if you select the **Test Script** action, it runs a script without any input. You can check the log to confirm that the script has been executed. The log shows a message indicating that the test script alert action has run.

You can add custom scripts for alert actions, and the system supports both base system and custom actions. This migration promotes better configuration, accessibility, and future support for the Crisis map application for the users. For information on alert actions, see [Configure alert actions](../task/configure-alert-action-uib-ws.md).

## Enhanced user experience and accessibility

Various accessibility issues in previous Crisis map releases have been resolved with the implementation of the Geomap \[sn\_geo\_map\] component, which has replaced the FAM Map \[sn-fam-map\] component and the user experience has been enhanced.

**Parent Topic:**[Structured workflows for Crisis map](crisis-map-collective-tasks.md)

