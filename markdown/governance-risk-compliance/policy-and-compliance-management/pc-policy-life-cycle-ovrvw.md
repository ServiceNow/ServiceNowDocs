---
title: An overview of policy life cycle in Policy and Compliance Management
description: Policies ensure compliance and reduce exposure to risks. A policy can be of any type – it can be a policy, procedure, standard, plan, checklist, framework, or template. Publishing a policy is within its approval process.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Structural overview of Policy and Compliance Management, Exploring Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# An overview of policy life cycle in Policy and Compliance Management

Policies ensure compliance and reduce exposure to risks. A policy can be of any type – it can be a policy, procedure, standard, plan, checklist, framework, or template. Publishing a policy is within its approval process.

When you create a policy, it is in a Draft state, and all the required information about the policy are defined and captured in the record. The required information that you capture are the attributes that drive the process flow of the policy.

![Process flow diagram of Policy and Compliance Management.](../image/process-flow-infograph-pol-comp.png)

The life cycle of a policy record passes through different states. This is designed to understand where the record currently resides and to display its progress. Each state has a specific set of related activities before it moves to the next state. A policy may also move to the previous state, if required, which is configured and identified according to the current state.

-   **Draft**

    A compliance admin, compliance manager, or a compliance user can create a policy, define and capture its related information. In this draft state, reviewers are identified, who have the ability to edit the policy in its review state, and approvers who can approve the policy. Control objectives that already exist can be added to the policy or new ones can be created. Each policy has a Valid to period, within which it is updated, reviewed, republished, or retired. In this state, the actions that are available for you to perform on the policy are Update, Ready for Review, and Delete.

-   **Review**

    Only the policy reviewers can Update the policy in this state to ensure that it satisfies all regulatory requirements. They review the control objectives, its associated entities, controls, and citations, and add additional information, remove unnecessary mappings, or create new control objectives. The reviewer can move the policy Back to Draft state if the policy does not fulfil the requirements or if more details are needed. The reviewer can also Request Approval for the policy or Delete if no longer needed.

-   **Awaiting approval**

    If a policy approver is assigned to the policy, the policy moves to the Awaiting approval state. Otherwise, it moves to the Published state. In this state, the approver can Delete the policy as well. In the Awaiting approval state, a policy approval task is created and assigned to the approver. The task is in Requested state, and the approver can change it to any of the following states:

    -   Requested
    -   Approved
    -   Rejected
    -   Cancelled
    -   No longer required
-   **Published**

    When the policy moves to the Published state the system automatically generates a Knowledge Base article. The policy becomes a mandate for all users to follow its guidelines and requirements, which is through the controls that are mapped to the policy. In this state, the policy can also be sent Back to Review, Retired, or Deleted.

-   **Retired**

    A policy may be retired if no longer required, or when it no longer serves a business purpose. The Knowledge Base article that was created is removed, but the policy stays in retired state for audit purpose. If the policy is needed again, it can be sent back to the Draft stage, and the policy's life cycle begins again.


