---
title: Configure content filtering rules for Playbook
description: Use content filtering rules to specify the role a user must have to access content.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [User access to Playbooks in Workflow Studio, Administering Playbooks, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Configure content filtering rules for Playbook

Use content filtering rules to specify the role a user must have to access content.

## Before you begin

Role required: admin, playbook.admin

Content filtering requires some familiarity with user roles and playbook tables and records.

## About this task

Filter Workflow Studio playbook content based on user role. Filtering content requires you to set up:

1.  Content definitions describe the content that you want to filter. Content definitions specify types of Workflow Studio resources, such as activity definitions.
2.  Content filtering rules to state the role a user must have to access the resource in a particular definition.

There is one content definition for playbooks by default, the **Playbooks - All Activity Definitions** content definition. The **Playbooks - All Activity Definitions** content definition has two content filtering rules by default:

-   **\(Default\) Playbook - Users with delegated\_developer role can access all activity definitions**
-   **\(Default\) Playbook - Users with playbook.activity\_def\_read role can access all activity definitions**

This means that users with the roles delegated\_developer or playbook.activity\_def\_read role can access all activity definitions, unless **Required Roles** is configured. Get started with content filtering by using default definitions and rules, or create your own.

## Procedure

1.  To modify or create a content filtering rule, navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Filtering Rules**.

    **Note:** If you don't have access to Flow Administration, the Content Filtering Rules module is directly under Process Automation instead.

2.  Select the rule that you want to modify or click **New** to create one.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the content filtering rule.|
    |User Role|The role a user must have to access the content in the **Resource Definition** field.|
    |Delegated Development Permission|The specific **Resource Path** that the user is a delegated developer for. Configure the **Resource Path** in the \[sys\_development\_permission\_set\] table.|
    |Active|Option to enable the rule.|
    |Application|Application scope to which the content filtering rule applies. This field is automatically set to the currently selected application scope. If no application scope is selected, the field is set to Global. If you set a specific application scope, then the content filtering rule only applies to that application scope. If you select the Global application scope, then the content filtering rule applies to all applications.|
    |Resource Definition|The name of the content definition that specifies the resource to filter.|

4.  Click **Submit**.


**Parent Topic:**[User access to Playbooks in Workflow Studio](../concept/user-access-playbooks.md)

