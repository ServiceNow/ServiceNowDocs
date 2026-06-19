---
title: Configure the AI widget builder for Employee Slate
description: Configure the AI widget builder in Employee Slate. Set the scope, the role access, and the chat panel that drives widget generation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-configure-ai-widget-builder.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [AI widget builder, widget configuration, widget scope, chat compatibility, role access, Employee Slate]
breadcrumb: [AI-powered Widget Builder, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure the AI widget builder for Employee Slate

Configure the AI widget builder in Employee Slate. Set the scope, the role access, and the chat panel that drives widget generation.

## Before you begin

Activate Employee Slate for Now Assist in the instance.

An Oasis for Creator license for any admin who uses the AI chat panel.

Role required: admin or Employee Slate administrator.

## About this task

The AI widget builder lets admins describe a widget in plain language. The builder generates the widget code, validates it, and compiles it before preview.

The landing card lists the widgets in the instance. Admins can search, filter custom widgets from out-of-the-box widgets, edit a widget, or clone a widget.

## Procedure

1.  Navigate to **Admin Console** &gt; **All** &gt; **AI widget builder**.

    The landing card lists every widget available in the instance.

2.  Set the scope for new widgets.

    Select **Global** to create widgets at the global scope, or select an application scope. The scope applies to every widget created from this point.

3.  Select **Create** to open the create workflow.

    The create workflow opens the chat panel on the left and the component and server script editor on the right.

4.  Enter a widget description in the chat panel.

    An example description is `Create a widget that creates an OTP page.` The skill validates, compiles, and renders the widget. The build can take 15 to 20 seconds.

5.  Set the widget properties.

    Set the element name, the widget name, the tag, and the description. Detailed property values improve the next chat prompt.

6.  Set **Chat compatibility** for the widget.

    Chat compatibility maps the widget to the output of tools used in agents. The setting renders the widget in the interactive chat view rather than inline.

7.  Assign roles for widget access.

    Select the roles that can view and use the widget. Restrict the widget to admin roles when the widget operates on admin-only data.

8.  Review the generated code.

    Open the component and the server script. Run quality checks and edit the code manually when needed.

9.  Preview the widget.

    Provide sample inputs and select **Refresh preview**. Drag, drop, and resize the widget to confirm responsive behavior.

10. Refine the widget with a subsequent prompt.

    An example refinement is `When the timer is less than 30 seconds, change the background color to red.` Accept or reject the change. Select **Undo** to revert to the prior version.

11. Save the widget.

    The save commits the widget code, the properties, the chat compatibility, and the role access. The widget is available in the widget library.


## Result

Admins create, clone, and refine AI-powered widgets from the same builder. Each widget honors the configured scope, the chat compatibility, and the role access. Admins can review the generated code and revert any change with the undo control.

