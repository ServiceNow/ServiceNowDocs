---
title: Approve with a process guide
description: Process guides work similarly to approval rules in that their execution is controlled via a condition.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Approval rules, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Approve with a process guide

Process guides work similarly to approval rules in that their execution is controlled via a condition.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/ask-approval-flow-designer.md). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

## Before you begin

Role required: none

## About this task

The default version of approval tasks allows you to specify that the approval in question be approved by:

1.  One or more specific people
2.  One or more groups of people

You can optionally use Process Guides instead of approval tasks. Process guides are more flexible in that they allow for:

1.  "Any of" or "All of" approvals
2.  Sequenced approvals

You can link a process guide to a execution task.

## Procedure

1.  From the left navigation pane, select **System Policy** &gt; **Process Guides**.

2.  Create a new guide.

3.  Set the table to **Catalog task**.

4.  Fill in a condition under which this guide should attach.

    Example \#1: Apply to all "Capacity Review" tasks.

    ![Capacity](../image/Capacity.png)

    Example \#2: Apply to all "Capacity Review" tasks where there requester is in Atlanta.

    ![Capacity Atlanta](../image/CapacityAtlanta.png)

    Process guide tips and tricks:

    1.  All catalog tasks are generated when a request is first submitted, but tasks which aren't active yet have a state of "pending". So if you do not want to send out approval requests until a task has actually started, add "state=open" as part of your condition.
    2.  There is a "Default" process guide in the system for catalog tasks with a sequence number of 10,000. It behaves exactly the same way the old, pre-process guide code did in regards to approvals. Approvals are based on the execution of task-related lists.

**Parent Topic:**[Approval rules](../concept/c_ApprovalRules.md)

