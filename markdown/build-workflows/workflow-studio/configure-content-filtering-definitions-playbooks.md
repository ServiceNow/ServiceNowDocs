---
title: Configure content filtering definitions for playbooks
description: Specify which content a user can access by creating content definitions.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [User access to playbooks in Workflow Studio, Administering playbooks, Playbooks, Configure, Workflow Studio, Build workflows]
---

# Configure content filtering definitions for playbooks

Specify which content a user can access by creating content definitions.

## Before you begin

Content filtering requires some familiarity with user roles and Workflow Studio tables and records.

Role required: admin, playbook.admin

## About this task

Filter Workflow Studio playbook content based on user role. Filtering content requires you to set up:

1.  Content definitions describe the content that you want to filter. Content definitions specify types of Workflow Studio resources, such as activity definitions.
2.  Content filtering rules to state the role a user must have to access the resource in a particular definition.

There is one content definition for playbooks by default, the **Playbooks - All Activity Definitions** content definition. The **Playbooks - All Activity Definitions** content definition has two content filtering rules by default:

-   **\(Default\) Playbook - Users with delegated\_developer role can access all activity definitions**
-   **\(Default\) Playbook - Users with playbook.activity\_def\_read role can access all activity definitions**

This means that users with the roles delegated\_developer or playbook.activity\_def\_read role can access all activity definitions. Get started with content filtering by using default definitions and rules, or create your own.

## Procedure

1.  To modify or create a content definition, navigate to **Process Automation** &gt; **Flow Administration** &gt; **Content Definitions**.

    **Note:** If you don't have access to Flow Administration, the Content Definitions module is directly under Process Automation instead.

2.  Select the definition that you want to modify or click **New** to create one.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the content definition.|
    |Application|Application scope to which the content definition applies. This field is automatically set to the currently selected application scope. If no application scope is selected, the field is set to Global. If you set a specific application scope, then the content definition only applies to that application scope. If you select the Global application scope, then the content definition applies to all applications.|
    |Table|Table containing the resource type that you're defining. For example, the Activity Definitions \[sys\_pd\_activity\_definition\] table includes all the activity definitions available on your instance.|
    |Conditions|Conditions used to filter the records in the table. For example, creating a condition where **\[Name\] \[contains\] \[Guided Decisions\]** returns only the activities that include the term Guided Decisions in the name.|
    |Resource Tags|Tags used to filter the resources in the table.|

4.  Click **Submit**.


**Parent Topic:**[User access to playbooks in Workflow Studio](../concept/user-access-playbooks.md)

