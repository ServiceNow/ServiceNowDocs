---
title: Administering form personalization
description: Administrators can configure several aspects of form personalization, which allows users to customize the layout for any form view.Form personalization is activated for new instances. To activate form personalization for upgraded instances, an administrator must activate the Form Personalization \(com.glide.ui.personalize\_form\) plugin.By default, the itil role is required to personalize forms, but you can change this requirement with a system property.When a user personalizes a form, the system stores the customizations as a user preference record. You can view and manage the user preferences.If you do not want your users to customize forms, you can disable form personalization.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Administering form personalization

Administrators can configure several aspects of form personalization, which allows users to customize the layout for any form view.

Administrators can manage this function using the following options.

-   Activate or deactivate form personalization globally.
-   Control user access to form personalization based on roles.
-   Manage the personalized forms of users.

**Note:** Personalizing a form in this way modifies the form for you only. To make changes to a form that are visible to all users, you must configure the form.

**Parent Topic:**[Form administration](form-administration.md)

## Activate form personalization

Form personalization is activated for new instances. To activate form personalization for upgraded instances, an administrator must activate the Form Personalization \(com.glide.ui.personalize\_form\) plugin.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Form Personalization \(com.glide.ui.personalize\_form\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## Change form personalization role requirements

By default, the itil role is required to personalize forms, but you can change this requirement with a system property.

### Before you begin

Role required: admin

### Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Locate the **glide.ui.personalize\_form.role** property in the System Properties list.

3.  In the **Value** field, specify the roles that can access form personalization.


## Manage personalized forms

When a user personalizes a form, the system stores the customizations as a user preference record. You can view and manage the user preferences.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  Filter the list by **\[Name\] \[contains\] \[personalize\]**.

    There is a user preference for each form view each user personalizes. The name format combines the word personalize with the name of the table and the name of the view. For example, if a user personalizes the default view of the Asset \[alm\_asset\] form, the user preference is called **personalize\_alm\_asset\_default**.

3.  Delete a user preference to remove the customizations for the user.


## Disable form personalization

If you do not want your users to customize forms, you can disable form personalization.

### Before you begin

Role required: admin

### About this task

Activating the Personalize Forms plugin sets the **glide.ui.personalize\_form** property to true. You can disable form personalization.

### Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Locate the **glide.ui.personalize\_form** property in the System Properties list.

3.  Set the **Value** field to `false`.


