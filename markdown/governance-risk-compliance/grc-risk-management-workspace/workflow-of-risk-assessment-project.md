---
title: Workflow of risk assessment project
description: The risk assessment project workflow is a structured process to assess multiple risks and controls simultaneously using Risk Workspace.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-10-26"
reading_time_minutes: 2
breadcrumb: [Risk assessment project, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of risk assessment project

The risk assessment project workflow is a structured process to assess multiple risks and controls simultaneously using Risk Workspace.

## Exploring the user journey for a risk assessment project

The following diagram shows the workflow of a risk assessment project.

![Workflow of a risk assessment project.](../image/risk-assessment-project-workflow.png "Risk assessment project workflow")

The stages of a risk assessment project are as follows:

1.  **Define**: In this stage, the risk assessment project is created. A risk assessment project user \(\[sn\_risk\_advanced.risk\_asmt\_project\_user\]\) or a risk assessment project manager \(\[sn\_risk\_advanced.risk\_asmt\_project\_manager\]\) can create a risk assessment project and complete the following tasks:
    1.  Define the context by including the assessable entity and the risk assessment methodology \(RAM\).
    2.  Specify the project name and description.
    3.  Identify and add the relevant stakeholders, including the project owner, assessors, and watchlist users.
2.  **Risk scoping**: In this stage, the risk assessment project owner is responsible for defining the risks to be assessed. The following options are available to map risks for the selected composite or single entity:
    -   **Create risks from upstream entities**

        Option to add risks based on underlying relationships with selected entities. Risks are automatically mapped from the underlying entities. You can remove them without deleting them from the underlying entities. This option is specific to composite entities.

    -   **Create ad-hoc risk**

        Option to add a risk that is not in the library.

    -   **Create risk from risk statements**

        Option to add risks from the risk statement.

3.  **Assessment**: In this stage, the assessor evaluates each scoped risk using the defined RAM. Throughout the assessment, the assessor can access a summary of the assessment. Automated error handling enables assessors to validate risk assessment projects, reducing the likelihood of errors and inconsistencies. After the assessment is completed, the assessor submits the assessment for approval.

    **Note:** Assessors can also add risks and controls during the assessment stage.

4.  **Approval**: In this stage, the approvers configured in the approval configurator review the assessment summary. Based on the approvers' satisfaction with the assessment, the approver can do one of the following:
    -   **Approve**

        The project moves to the Completed stage.

    -   **Reject**

        The project moves to the Assessment stage for the assessor to address identified issues and make necessary revisions.


**Note:** After the project reaches the Completed state, you can create a new project with the same RAM and entity. When the new project reaches the Completed state, the old project moves to the Archived state.

**Parent Topic:**[Risk assessment project](risk-assessment-project.md)

