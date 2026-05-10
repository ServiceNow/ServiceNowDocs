---
title: Use case: Generate modules using Now Assist
description: Create and configure application menu modules using natural language
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Use case, Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Use case: Generate modules using Now Assist

Create and configure application menu modules using natural language

## Scenario

A ServiceNow admin at a logistics company is building a new custom application for managing warehouse operations. The application menu should include multiple modules: a list of active tasks, a form for logging new incidents, a dashboard for warehouse KPIs, a link to an external supplier portal, and a folder for organizing reporting modules. Configuring each module individually through the standard UI would require navigating multiple forms and configuration screens.

## Problem

Creating and configuring each module in the UI Builder manually can be time-consuming and repetitive, particularly when multiple modules are required simultaneously. Each module type includes its own set of configuration fields, including table names, filters, roles, views, and window settings. As a result, the administrator must fill in these fields individually. When dealing with an application with five or more modules, this process can take considerable time and is prone to configuration errors.

## Solution

Using the Module generation feature, the admin provides a single natural-language prompt that describes all required modules. The AI agent analyzes the prompt, identifies the appropriate module types and key parameters, and generates all modules in a single step. The admin then reviews each generated module, makes any necessary adjustments, and saves the complete application menu.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](../task/install-ui-generation.md) and [Grant UI Builder admin role](../task/grant-ui-builder-admin-role.md).

## Configuration steps

Perform the following steps to generate modules:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  From the application navigator, select **All**, then select **Create menu**.

    ![image.ui_gen_module_gen_create_menu]

3.  Enter a name for the application menu \(for example, Warehouse Operations\) and select Create.
4.  On the Add modules page, select **Generate multiple modules at once using Now Assist**.
5.  Enter the following prompt: `Create a list of active warehouse tasks, a new record form for logging incidents, a KPI dashboard called Warehouse Overview, a URL module linking to https://supplier-portal.example.com with window name Supplier Portal, and a folder called Reports`.
6.  Select **Generate**.

    Now Assist creates five modules and displays an AI indicator next to each.

7.  Review each module. Select **Accept and Edit** for each module to confirm and adjust configuration fields such as table name, role restrictions, or view settings.
8.  Rearrange modules if needed, then select Done.

## Outcome

The administrator creates and configures a five-module application menu within a single workflow. The resulting modules are immediately ready for use in the application navigator.

**Parent Topic:**[UI Generation use cases](../task/ui-generation-use-cases.md)

**Related topics**  


[Module generation](ai_module_creation_concept.md)

[Generate modules using Now Assist](../task/generate-ai-modules.md)

