---
title: Decision tables workflow
description: Learn how to create and maintain decision tables in Workflow Studio for use in flows, subflows, playbooks, and anywhere on the ServiceNow AI Platform where you write code.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Decision tables, Explore, Workflow Studio, Build workflows]
---

# Decision tables workflow

Learn how to create and maintain decision tables in Workflow Studio for use in flows, subflows, playbooks,and anywhere on the ServiceNow AI Platform where you write code.

Decision tables enable you to decouple decision logic from your code. This means that you can create a decision table in Workflow Studio with your application logic and then reference the decision table to execute the logic elsewhere, such as in a flow, playbook, or script. This decoupling enables you to create more efficient and maintainable flows and scripts and allows the decision logic to be managed directly by the relevant business subject matter expert.

## Workflow for creating decision tables

The following illustration depicts the process for creating decision tables in Workflow Studio.

![Infographic depicting the process of creating a decision table in Workflow Studio](../image/db-workflow.png "Process for creating decision tables")

The workflow for creating decision tables in Workflow Studio is as follows:

1.  A developer is writing a script or authoring a flow or subflow and realizes there is a need for a decision table. Decision tables are a more maintainable solution than hard-coded logic for the following scenarios:
    -   There is a complex set of conditional, nested if/else or switch statements in the code.
    -   The logic powering the code might change frequently.
    -   There is a need to share the application logic with non-developers in a readable format.
    -   There is a need for application logic to be managed independently from where it is implemented.
    -   There is a need for application logic to be managed by non-developers.
    -   There is a need to apply the same logic in more than one flow, subflow, or script.
    -   There is application or business logic the developer wants to manage separately from the code.
2.  The developer creates the decision table in Workflow Studio and adds inputs and result columns \(outputs for the decisions\).
3.  A developer or a business subject matter expert \(SME\) can perform the next steps.
    1.  Add condition columns to structure the rules.
    2.  Add decision rows to build conditional rules and corresponding results.
    3.  Test the decision table.
    4.  Publish the decision table.
4.  The developer can use the decision table in a few ways.
    -   They can create a code snippet of the decision table and insert it into their code.
    -   They can add **Make a decision** logic in their flow or subflow and reference the decision table.
    -   They can add a decision table to a playbook using the **Make a Decision - First Match** activity.
5.  If the decision table must be updated to reflect new logic, the developer or business SME can create a new draft of the table. They can test the table using the new logic and then publish the new version. To create a Decision Table, See [Create decision tables in Workflow Studio](../task/create-decision-table-in-decision-designer.md).

    **Note:** For any decision table that doesn't use draft authoring, any change the developer or business SME makes is automatically active.


**Parent Topic:**[Exploring Decision Tables](decision-designer-overview.md)

