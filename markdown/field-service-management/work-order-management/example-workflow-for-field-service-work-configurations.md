---
title: Example workflow for Field Service Work Configurations
description: Explore how to use Field Service Work Configurations for a break-fix task for MRI Scanner. This example workflow shows a customized flow, and an additional state for break-fix work order for MRI Scanner.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work Configurations, Work orders and tasks, Configure, Field Service Management]
---

# Example workflow for Field Service Work Configurations

Explore how to use Field Service Work Configurations for a break-fix task for MRI Scanner. This example workflow shows a customized flow, and an additional state for break-fix work order for MRI Scanner.

## Before you begin

Role required: admin, wm\_agent

Make sure the Field Service Work Configurations plugin \(com.snc.fsm\_work\_types\) and the Field Service Demo Work Configuration for Break fix \(com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\) plugin is installed.

## About this task

The demo workflow for Field Service Work Configurations uses a custom SM configuration \(MRI Scanner Break Fix\) for work orders of type break-fix for MRI Scanner. The customizations included in the configuration for this workflow are:

-   Auto-qualify the work order
-   Auto-accept the work order task when assigned to an agent
-   An additional state **Complete Diagnosis**
-   Questionnaire for MRI Scanner break-fix
-   Work order summary template for the completion of the task

## Procedure

1.  Create a work order of type break-fix specifying the template as **MRI Scanner Break Fix Template**.

2.  Select **Ready for Qualification**; the task moves to **Qualified** state.

3.  Assign the task.

    1.  Navigate to the work order task.
    2.  Select dispatch group, assignment group, and the agent.
    3.  Save the task.
    The work order task transitions to **Accepted** state.

4.  As an agent, do the following:

    1.  Navigate to the work order task and fill in the additional fields **Problem Type**, **Problem Details**, and **Diagnosis Details**, that are added for this work configuration.
    2.  Select **Complete Diagnosis**; the work order task transitions to **Diagnosis Completed**.
    3.  Select **Questionnaires** to complete the questionnaire included in the work configuration.
    4.  Enter the closing comments in **Work notes** and select **Close complete**.
5.  Close the work order.

    1.  Navigate to the work order and select **Sign and Confirm**.
    2.  Enter your name and signature in the **Signature Pad** and select **Accept**.
    3.  Download the work order summary customized for the demo work configuration workflow.

