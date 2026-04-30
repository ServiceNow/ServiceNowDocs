---
title: Configure content filtering rules
description: Use content filtering rules to specify the role a user must have to access content.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content filtering, User access to flows, Flows, Configure, Workflow Studio, Build workflows]
---

# Configure content filtering rules

Use content filtering rules to specify the role a user must have to access content.

## Before you begin

Role required: flow\_designer, action\_designer, or admin

Content filtering requires some familiarity with user roles and Workflow Studio tables and records.

Role required: flow\_designer, action\_designer, or admin

## About this task

Filter Workflow Studio flow content based on user role. Filtering content requires you to set up:

1.  Content definitions to describe the content that you want to filter. Content definitions specify types of Workflow Studio flow resources, such as actions and subflows.
2.  Content filtering rules to state the role a user must have to access the resource in a particular definition.

Workflow Studio includes several content definitions and filtering rules by default. Get started with content filtering by modifying the pre-existing definitions and rules or creating your own.

## Procedure

1.  To modify or create a content filtering rule, navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Filtering Rules**.

2.  Select the rule that you want to modify or click **New** to create one.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the content filtering rule.|
    |User Role|The role a user must have to access the content in the **Resource Definition** field.|
    |Active|Option to enable the rule.|
    |Application|Application scope to which the content filtering rule applies. This field is automatically set to the currently selected application scope. If no application scope is selected, the field is set to Global. If you set a specific application scope, then the content filtering rule only applies to that application scope. If you select the Global application scope, then the content filtering rule applies to all applications.|
    |Resource Definition|The name of the content definition that specifies the resource to filter.|

4.  Click **Submit**.


**Parent Topic:**[Content filtering for Workflow Studio flows](../concept/content-filtering-flow-designer.md)

