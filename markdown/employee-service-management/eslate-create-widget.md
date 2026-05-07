---
title: Create a widget with the AI-powered Widget Builder
description: Use the AI-powered Widget Builder to generate an Employee Slate widget from a natural-language prompt. Refine the widget properties and publish the widget to the widget library.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [widget creation, AI-powered Widget Builder, natural-language prompt, widget library]
breadcrumb: [AI-powered Widget Builder, Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Create a widget with the AI-powered Widget Builder

Use the AI-powered Widget Builder to generate an Employee Slate widget from a natural-language prompt. Refine the widget properties and publish the widget to the widget library.

## Before you begin

Before you create a widget, verify the following prerequisites:

-   You have the administrator role required to create widgets in the target scope.
-   An Now Assist Creator license is assigned to your user account. Without this license, the AI chat panel isn't available.
-   The target scope for the widget is selected.

Role required: System administrator.

## About this task

The Widget Builder generates, validates, and compiles the widget behind the scenes. Generation can take 15 to 20 seconds for the initial prompt and for each refinement prompt.

## Procedure

1.  In the Widget Builder library, select **Create**.

    The create workflow opens with the widget preview on the right and the AI chat panel on the left.

2.  In the chat panel, enter a description of the widget that you want to build.

    Include the widget purpose, the inputs tables data, and any visual behaviors that you expect. For example: `Create a widget that renders a one-time password entry page with a 60 second countdown.`

    **Note:** When your prompt is clear and detailed, the generated widget can be more effective.

3.  Wait for the widget to generate.

    The Widget Builder validates and compiles the generated widget before it appears in the preview.

4.  Review the generated widget in the preview.

    Drag, resize, and switch between desktop and mobile presentations to verify the responsive behavior. If the widget accepts input values, enter sample values through the widget settings to drive the preview.

5.  Set the widget properties such as **Tag name**, **Description**, and **Chat compatibility** values.

    The widget properties are configured and ready for publication.

6.  Refine the widget with an additional prompt.

    Enter a follow-up prompt to modify the widget. For example: `When the timer is less than 30 seconds, change the background color to red.`

    After the refinement generates, select **Accept** to apply the change or use the undo control to revert to the previous version.

7.  Open the generated component and server script to review or edit the code.

    The component and server script panels show the generated code. Edit the code directly for changes that aren't easily expressed as a chat prompt.

8.  Save the widget.

    The widget appears in the Widget Builder library, ready to add to canvas dashboards and to the widget library for employee personalization.


## Result

The new widget is available in the Widget Builder library with the tag name, description, and role assignments that you configured. You can add the widget to the default canvas dashboard, and can also expose it through the widget library so employees can add it to their personal canvas.

