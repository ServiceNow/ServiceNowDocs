---
title: Portal Playbook Widget
description: Explore the Portal Playbook Widget.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure a playbook for Service Portal, Playbooks in Service Portal, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Portal Playbook Widget

Explore the Portal Playbook Widget.

## About the widget

The Playbook widget is an iFrame that enables administrators to specify where a playbook event should be directed. The iFrame URL is the UI Builder Playbooks Portal page. The widget handles events that playbook is listening for via the Session Storage API so that it knows when to perform an action in portal, like opening a record or list in a modal within Service Portal.

The out-of-the-box components are built for any Playbook Experience you may need for your Service Portal users. We do not recommend directly editing the out-of-the-box UI Builder Playbook Portal Page, the Service Portal Playbook widget, or the Playbook Content Item. Changing the out-of-the-box components can result in technical problems.

If, for example, you need a UXF Client Action to work for your instance of the playbook page, we recommend cloning the playbook widget instead.

**Note:** To learn more about how to clone or create your own widget instead, see Developing custom widgets.

## Cloning a Playbook Service Portal Widget

Navigate to **All** &gt; **Service Portal** &gt; **Widgets** and find the **Playbook** widget.

**Note:** If you clone the **Playbook** widget, make sure that all out-of-the-box actions and configuration properties are copied over to your cloned widget.

<table id="table_fnf_ydw_vbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the cloned widget.

</td></tr><tr><td>

ID

</td><td>

The widget ID is created automatically based on the widget name by default, but you can change it to whatever you want.

</td></tr><tr><td>

Description

</td><td>

Add an optional description that provides details for the widget does.

</td></tr><tr><td>

Application

</td><td>

Choose an application scope that you want your widget to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see Application scope.

</td></tr><tr><td>

Public

</td><td>

Select if your widget is public. If unchecked, your widget is private and only authenticated users with the snc\_internal or snc\_external role can see the widget.

</td></tr><tr><td>

Roles

</td><td>

Restrict access to the widget to certain roles.

</td></tr><tr><td>

Body HTML template

</td><td>

Leverage the Angular JS two-way binding to bind your controller variables to your markup.**Danger**

Only make changes to HTML templates if you have advanced coding knowledge and a firm understanding of AngularJS and the platform API.

The iFrame URL is the URL of the UI Builder page. To learn more about the HTML template field, see Developing custom widgets.**Warning:** Make sure the iFrame URL of your cloned widget is different from the iFrame URL for the out-of-the-box widget.

</td></tr><tr><td>

CSS

</td><td>

Configure the widget CSS. Configuring CSS in an actual widget affects all instances of that widget. To learn more about the CSS field, see Developing custom widgets.

</td></tr><tr><td>

Server script

</td><td>

Script the server-side logic. This is helpful primarily with interacting with the Glide platform through server-side APIs.**Danger**

A server script requires knowledge of the ServiceNow API to work with record data.

To learn more about the Server script field, see Developing custom widgets.

</td></tr><tr><td>

Client controller

</td><td>

In Angular, HTML templates contain Angular-specific elements and attributes. Angular combines the template with information from the model and client controller to render the dynamic view that a user sees in the browser. Identifier name for a reference to the controller in the directive's scope**Danger**

A client script requires knowledge of both the ServiceNow API and AngularJS to create a client controller.

</td></tr><tr><td>

controllerAs

</td><td>

The HTML template uses the controllerAs syntax for basic binding.

</td></tr><tr><td>

Link

</td><td>

Use a link function to directly manipulate the DOM.**Danger**

The link function requires knowledge of AngularJS.

 To learn more about the Link field, see Developing custom widgets.

</td></tr><tr><td>

Has preview

</td><td>

Select the option to enable a preview of the widget in the Widget Editor.

</td></tr><tr><td>

Demo data

</td><td>

Provide data when previewing the widget in the widget editor.

</td></tr><tr><td>

Data table

</td><td>

Select a table to use as a data source.

</td></tr><tr><td>

Fields

</td><td>

Select fields to display as instance options.

</td></tr><tr><td>

Option schema

</td><td>

Allows a Service Portal admin to configure a widget. To learn more about the Option schema field, Widget option schema.

</td></tr><tr><td>

Docs

</td><td>

Select a Service Portal documentation link.

</td></tr></tbody>
</table>Check for errors in the UI Builder Playbook Experience Portal page config and events properties, e.g. disable the Open Record event as a maint user.

