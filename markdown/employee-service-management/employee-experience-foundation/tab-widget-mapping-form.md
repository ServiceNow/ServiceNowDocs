---
title: Tab widget mapping form
description: You can use the tab widget mapping form to display widgets on a tab and control their visibility.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Reference, Employee Center, Employee Service Management]
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
Values that are defined in the Not Available For group take precedence over the values defined in the Available For group. If both aren't defined, the widget is visible to all users. For more information on widget visibility based on user criteria, see [User Criteria output](user-criteria-output.md).

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

Comma-separated list of widget parameters auto-populated with default values.For the **Employee Schedule** widget, to send Email or SMS, specify the widget parameters `enable_send_email` and `enable_send_sms` values to true. For more information, see [Configure the mail and SMS send to self](../task/deskless-kiosk-sendtoself-sms-email.md).

For default calendar view, specify `default_calendar_view` value to day or week or month.

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center reference](emp-center-reference.md)

**Related topics**  


[Activity Configuration form](ec-activity-configuration-form.md)

[Activity Configuration Detail form](activity-configuration-detail-form.md)

[Approvals experience reference](approval-hub-ootb.md)

[Block content form](block-content-form.md)

[Browser Extension for Employee Center forms](../concept/ecbe-forms.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Publishing](installed-with-content-delivery-1.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Connected Content form](connected-content-form.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Default Employee Profile Header Configuration record](default-profile-header.md)

[Employee Center widgets](../concept/employee-center-widgets-list.md)

[Employee Profile form](employee-profile-fieldconfig.md)

[Employee Profile Header Configuration form](profile-header-config-form.md)

[Employee Profile portal configuration form](profile-portal-config-form.md)

[Employee Profile upgrade scenarios](emp-profile-upgrade.md)

[Enhanced Requests Experience forms](req-concept-ec.md)

[External Link form](external-link-form.md)

[Featured Content form](featured-content-form.md)

[Feedback Analytics dashboard](../concept/ex-fdback-board.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Footer form](ec-footer-form.md)

[Footer Menus form](ec-footer-menus.md)

[Guided Self-Service reference](gss-guided-self-service-reference-info.md)

[Link content form](link-content-form.md)

[Menu Item form](menu-item-form.md)

[Configuring translation for Content Publishing after upgrade](../concept/ec-multiple-language-support.md)

[Notification content form](notification-content-form.md)

[Employee Profile Overview section form](profile-overview-section-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Quick Link form](ec-quick-link-form.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[Taxonomy form](taxonomy-form.md)

[To-do content form](to-do-content-form.md)

[Topic form](topic-form.md)

[User Criteria form](ec-user-criteria-form.md)

[User Criteria output](user-criteria-output.md)

[Manage profile tabs and visibility in Employee Profile](../task/manage-employee-profile-tabs-visibility.md)

