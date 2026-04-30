---
title: Workflow of risk assessment project in AI Risk and Compliance
description: The risk assessment project workflow is a structured process to assess multiple risks and controls of an AI asset simultaneously.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Risk assessment project in AI Risk and Compliance, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Workflow of risk assessment project in AI Risk and Compliance

The risk assessment project workflow is a structured process to assess multiple risks and controls of an AI asset simultaneously.

## Exploring the user journey for AI asset risk assessment projects

The stages of a risk assessment project are as follows:

1.  **Define**: In this stage, the risk assessment project is created. Users with sn\_risk\_advanced.risk\_asmt\_project\_user can create a risk assessment project and complete the following tasks:
    1.  Define the related assessable entity and the risk assessment methodology \(RAM\).
    2.  Specify the project name and description.
    3.  Identify and add the relevant stakeholders, including the risk assessment project owner, assessors, and watchlist users.
2.  **Risk scoping**: In this stage, the risk assessment project owner is responsible for defining the risks to be assessed. The following options are available to map risks for the selected composite or single entity:
    -   **Create risk from risk statements**

        Option to add risks from the risk statement.

    -   **Create ad-hoc risk**

        Option to add a risk that is not in the library.

    -   **Add risk**

        Option to create risks from the internal risk library.

3.  **Assessment**: In this stage, the assessor evaluates each scoped risk using the defined RAM. Throughout the assessment, the assessor can access a summary of the assessment. Automated error handling enables assessors to validate risk assessment projects, reducing the likelihood of errors and inconsistencies. After the assessment is completed, the assessor submits the assessment for approval. Assessors can also add risks during the assessment stage.

    **Note:** If any risk assessment has a High inherent rating, the approval is sent to the risk assessment project owner. If the project owner and assessor are the same user, the approval is skipped. To use this approval flow, you must activate the default approval configuration 'Bulk risk assessment approval config.'

4.  **Approval**: In this stage, the approvers configured in the approval configurator review the assessment summary. Based on the approvers' satisfaction with the assessment, the approver can do one of the following:
    -   **Approve**

        The project moves to the Completed stage.

    -   **Reject**

        The project moves to the Assessment stage for the assessor to address identified issues and make necessary revisions.


**Note:** After the project reaches the Completed state, you can create a new project with the same RAM and entity. When the new project reaches the Completed state, the old project moves to the Archived state.

