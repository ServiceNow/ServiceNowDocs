---
title: Create a response action for Cloud Provisioning and Governance
description: Create a subflow with the required input parameters that notifies Cloud Provisioning and Governance whether the flow completes successfully or not.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Day 2 operations using Workflow Studio subflow, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a response action for Cloud Provisioning and Governance

Create a subflow with the required input parameters that notifies Cloud Provisioning and Governance whether the flow completes successfully or not.

## Before you begin

-   Ensure that you are familiar with the concepts of , [Subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md), and [Action Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/actions.md).
-   Create a subflow that you intend to invoke for pre or post-provisioning.

Role required: flow\_designer, action\_designer, or admin

## About this task

Inform the Cloud Provisioning and Governance application, the execution status of steps in the subflow, by populating a response for each step.

-   Create a action with relevant input parameters.
-   Add a script to the action.
-   Pass a correlation id to the action in the subflow.

The response action communicates to the Cloud Provisioning and Governance application whether a step in the subflow, executes successfully or the step's condition fails and results in an error.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Actions** tab, select **New Action**.

    For more information, see [Create an action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-action.md).

2.  Fill in the Action Properties.

3.  Create and define action inputs to make data available to the action steps and outputs.

    Create the following input variables: error, log, output, and correlation id.

    ![Sample response action- Cloud Provisioning and Governance](../image/return-action-sample.png "Sample response action to Cloud Provisioning and Governance")

4.  Select and add a script action step to perform an operation on the action inputs.

5.  **Save** and **Publish** the action.

6.  In the **Flow Designer**, open the subflow you are invoking.

    **Note:** Ensure that the subflow input `flowcorrelationid` exists in the subflow.

7.  On the same subflow page, click **Actions** to expand and find **Actions**, **Subflow** or **Flow Logic**.

8.  Select Cloud Provisioning and Governance and, search and add the response action from the drop down.

9.  Select relevant values from the **Data Pill Picker**, for the inputs in the action.

    **Note:** Reuse the `flowcorrelationid` input from the **Data Panel** for every action in the subflow that has a logical end step.

10. If you are using the Terraform Connector for Terraform Enterprise, follow these steps.

    1.  To add actions, flows, subflows, or flow logic, click **Select to add an Action, Flow Logic, or Subflow**.

    2.  Select **Action** &gt; **Cloud Management: Terraform Connector**, and select a default action.

    ![Default actions- terraform Connector](../image/terraform-connector-default-actions.png)

    The action you created sends a response to the Cloud Provisioning and Governance application, updating the order with the status of the subflow's step.


## What to do next

Test the subflow, and publish it when it is ready to be added to a flow or called from a script.

**Note:** You can only test or publish subflows that contain at least one action.

