---
title: Create a task template for common task requests
description: If you have tasks that are often repeated across multiple jobs, you can create and reuse a task template in multiple request templates. You can also use it on a Work order request to pull common and repeatable information into a request.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Request task management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Create a task template for common task requests

If you have tasks that are often repeated across multiple jobs, you can create and reuse a task template in multiple request templates. You can also use it on a Work order request to pull common and repeatable information into a request.

## Before you begin

Role required: wm\_admin

Create a request template and an associated task template that contains the information you want to reuse.

**Note:** Checklist templates are a way to populate a checklist of tasks to be completed. Checklist templates are created on a Work order request or on a Work order task. After being created, they can be saved as a template and be reused.

When you create subsequent request templates, you can select the task template from the **Task Template** field and save the file.

## About this task

A work order outlines the entire request or process. A work order task are the detailed steps for the parent work order. Every work order needs at least one work order task to get assigned to a specific agent to finish that step. Every work order task must have a parent work order to track the request.

Sometimes work orders are opened with the same purpose, and these work orders should have similar flows and similar work order tasks. A work order template can be used to fill in some fields in the work order, and create work order tasks.

The difference between a work order template and task template is you can’t create a task template alone, it must be part of the work order template. Creating a task template is a step of creating a work order template since you can define tasks and task templates for a work order or work order template.

With request tasks, work order tasks are not required, though they can be used. Request task management gives you the ability to split a request into multiple tasks. This document, Create a task template for common request tasks, describes the ability to use the work order task templates to apply them to common or repeated requests that you might have.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Catalog &amp; Knowledges** &gt; **Work Order Templates**.

2.  Select **New** and enter the following information.

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the Work order Template.|
    |Short description|A short description of the template.|
    |Description|A detailed description of the template.|
    |Checklist template|A Checklist template saved from the Work Order Request Form.|

3.  Select **Add Task**.

4.  Select **Copy Task Template** to use a previously created template, or enter the following information.

    |Field|Description|
    |-----|-----------|
    |Task type|The type of task being requested.|
    |Name|Descriptive name of the task.|
    |Description|Detailed description of the task.|
    |Parts and quantities|What parts and how many are needed to complete the task.|
    |Dispatch group|The dispatch group to assign the task to.|
    |Depends on|Indicates if the task depends on another task. For example, if you have two tasks, you can make task 2 dependent on task 1 completing before task 2 can start.|
    |Checklist template|A Checklist template saved from the Work order Request Form.|
    |Work type|The type of work being performed during the task.|

5.  Select **Submit**.


