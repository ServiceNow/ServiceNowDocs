---
title: Tab widget mapping form
description: You can use the tab widget mapping form to display widgets on a tab and control their visibility.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/tab-widget-mapping-form.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Employee Center reference, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Tab widget mapping form

You can use the tab widget mapping form to display widgets on a tab and control their visibility.

<table id="id_apm_rzw_mwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the widget-mapping record that is available in the **widgetTitle** variable of the widget options object. Use this variable value as the widget title.

</td></tr><tr><td>

Application

</td><td>

Application of the tab. For example, you can select one of the applications such as **Employee Center Pro** or **Employee Center Pro Kiosk**.

</td></tr><tr><td>

Active

</td><td>

Option to activate the widget in the tab.

</td></tr><tr><td>

Order

</td><td>

Order number in which you want the widget to appear on the tab.

</td></tr><tr><td>

Tab

</td><td>

Unique name of the tab that you want to associate with.

</td></tr><tr><td>

Accessible by

</td><td>

Users who can view the widgets.-   Employee only
-   Manager only
-   Employee and manager
-   Everyone
-   Manager and Other Managers
-   Employee, Manager, and Other Managers
-   User criteria: Provide the access only to specific users, groups, and roles with the user criteria. The widget is visible to the users based on the following:

    -   Available For: User group for whom the widget is visible. Define and select the user group based on your business needs.
    -   Not Available For: User group for whom the widget isn’t visible. Define and select the user group based on your business needs.
Values that are defined in the Not Available For group take precedence over the values defined in the Available For group. If both aren't defined, the widget is visible to all users. For more information on widget visibility based on user criteria, see [User Criteria output](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/user-criteria-output.md).

**Note:** Use the user criteria cautiously because the profile page load time can take longer based on your criteria.


Based on your selection, the profile visibility is either locked or made available for editing by the employee.

</td></tr><tr><td>

Allow employee to control visibility

</td><td>

This field appears only when you select one of the Employee only, Employee and manager, or Everyone options. **Note:** To view and change the visibility setting, embed the **Public Profile Visibility** widget inside the configured widget.

When you select the value as **true**, employees can see the edit option used to modify the visibility settings. The modified visibility setting **\(employee\_profile.widget\_visibility\)** is stored in the user preference table. **Note:** Settings configured in the **Allow employee to control visibility** field take precedence over the settings configured in the **Accessible by** field to display the information. Employees can change the admin configuration and determine how much of the profile information is visible to the public.

Here’s a sample code for invoking the Public Profile Visibility widget. `data.publicProfileWidget = $sp.getWidget("public_profile_visibility", { tabWidgetMappingId: options.tabWidgetMappingId ? options.tabWidgetMappingId : "", isUserSelectionEnabled: options.isUserSelectionEnabled ? options.isUserSelectionEnabled : "", widgetTitle: options.widgetTitle ? options.widgetTitle : “” });`

`To embed it in your widget use the sp-widget directive. For example, <sp-widget widget="data.publicProfileWidget"></sp-widget>`

This field value is available in the **isUserSelectionEnabled** variable of the widget options object.

</td></tr><tr><td>

Widget

</td><td>

Widget to display on the tab.**Note:** Only when you map a widget to the tab, the information displays inside the tab on the employee profile page.

When the widget is visible on the UI, set the **isVisible** variable value to **true** in the server script data object to indicate the widget visibility. For example, **data.isVisible = true**.

For optimal tab load time, use a max of seven associated widgets, which can take 250 ms or equivalent.

**Note:** If the widget type is Employee Profile Overview, you can select the set of sections to be displayed under this widget.

</td></tr><tr><td>

Widget parameters

</td><td>

Comma-separated list of widget parameters auto-populated with default values.For the **Employee Schedule** widget, to send Email or SMS, specify the widget parameters `enable_send_email` and `enable_send_sms` values to true. For more information, see [Configure the mail and SMS send to self](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/deskless-kiosk-sendtoself-sms-email.md).

For default calendar view, specify `default_calendar_view` value to day or week or month.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/emp-center-reference.md)

**Related topics**  


[Activity Configuration form]()

[Activity Configuration Detail form]()

[Approvals experience reference]()

[Connected Content form]()

[Default Employee Profile Header Configuration record]()

[Employee Center widgets]()

[Employee Profile form]()

[Employee Profile Header Configuration form]()

[Employee Profile portal configuration form]()

[Employee Profile upgrade scenarios]()

[Enhanced Requests Experience forms]()

[External Link form]()

[Featured Content form]()

[Footer form]()

[Footer Menus form]()

[Guided Self-Service reference]()

[Menu Item form]()

[Overview section form]()

[Portal notification configuration form]()

[Portal notification content form]()

[Trigger conditions form]()

[Quick Link form]()

[Taxonomy form]()

[Topic form]()

[User Criteria form]()

[User Criteria output]()

[Schedule appointment form]()

[Location Consent form]()

[Website configuration form]()

[Manage profile tabs and visibility in Employee Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/manage-employee-profile-tabs-visibility.md)

