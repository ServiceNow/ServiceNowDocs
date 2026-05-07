---
title: AI-powered Widget Builder
description: Administrators and partners use the AI-powered Widget Builder to generate, clone, and refine Employee Slate widgets. The builder provides natural-language prompts, a visual preview, and direct access to the generated component and server script.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [AI-powered Widget Builder, widget authoring, natural-language prompts, widget library]
breadcrumb: [Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# AI-powered Widget Builder

Administrators and partners use the AI-powered Widget Builder to generate, clone, and refine Employee Slate widgets. The builder provides natural-language prompts, a visual preview, and direct access to the generated component and server script.

The Widget Builder is the single authoring surface for all Employee Slate canvas widgets. It combines a widget library, an AI chat panel, and an inline code and preview workspace. Administrators move from a written requirement to a working widget without leaving the tool.

## Widget library

The first card in the Widget Builder lists every widget available in the instance. Administrators use the library to:

-   Search for widgets by name or description.
-   Filter between custom widgets built in the instance and widgets included in the base system.
-   Duplicate an existing widget as the starting point for a new one.
-   Edit an existing widget directly.
-   Select the scope in which to create the widget.

## AI-driven widget generation

The Widget Builder chat panel generates widget code from a written description. The builder creates the widget and validates the generated code. It then compiles the widget to confirm that the output is a working component before it appears in the preview. Generation typically completes in 15 to 20 seconds.

After the Widget Builder generates the widget, administrators refine it with follow-up prompts. Each prompt produces a new version of the widget that the administrator accepts or rejects. The Widget Builder keeps an undo history so administrators can revert to any earlier version.

**Note:** AI-driven widget generation requires an Now Assist Creator license. Without the license, the chat panel isn't available and administrators author widgets manually in the component and server script editors.

## Widget properties

The Widget Builder generates the widget tag name, element name, and description from the prompt. Administrators can refine the following properties:

|Property|Description|
|--------|-----------|
|Tag name and description|Identifies the widget in the library and in generated code.|
|Chat compatibility|Controls whether the widget maps to the output of tools that agents use. When enabled, the widget can be mapped to a tool output with interactive and inline toggle view in the conversation.|
|Role access|Limits the widget to employees with specific roles. For example, assign an administrator role to restrict the widget to administrators.|

## Preview and code review

The Widget Builder preview supports drag, resize, and responsive checks so administrators can confirm that the widget behaves correctly across canvas layouts. Generated widgets follow the Employee Slate design system and use design tokens for styling.

Administrators open the generated component and server script to inspect the code and run manual quality checks. They can also edit the widget outside of the chat panel. To drive the preview, administrators provide sample input values through the widget settings.

