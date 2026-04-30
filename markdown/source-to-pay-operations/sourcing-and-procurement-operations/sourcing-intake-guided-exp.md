---
title: Sourcing intake guided experience with playbooks
description: As sourcing managers, you can use the sourcing intake and negotiation setup playbooks to guide you through the complex request intake process so that you can focus on actual productive work such as negotiating savings from suppliers.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing intake guided experience with playbooks

As sourcing managers, you can use the sourcing intake and negotiation setup playbooks to guide you through the complex request intake process so that you can focus on actual productive work such as negotiating savings from suppliers.

The sourcing intake playbook and the negotiation setup playbook embedded in the sourcing intake playbook as a flow, guide you through these actions with clear steps to view your progress​.

Here's a quick breakdown of the playbooks and their associated tasks.

## Sourcing intake playbook

![Sourcing intake playbook](../image/pb-sourcing-intake.png)

The sourcing request playbook, also known as the sourcing intake playbook, enables you to:

-   Review an employee or requester’s requirements, which include details of the sourcing intake, purchase lines, and approvals.
-   Request clarifications or more information from the requester, if necessary.
-   Collaborate with cross-functional teams and create other work such as tasks and cases for them, if necessary.​

    For more information on how to perform these actions on the sourcing intake playbook, see [Review details and request clarification on a sourcing request in playbook](../task/review-details-request-clari-sr.md).

-   Decide if you should negotiate in a sourcing event or not.

    Here, as the sourcing manager, you can select a sourcing approach to source with similar employee requests. You can decide whether to work on negotiations with suppliers right away or at a later stage. In case of the former, you must add the sourcing request to a new or existing sourcing event​ to proceed.

    For more information on how to perform these actions on the sourcing intake playbook, see [Select a sourcing approach in playbook](../task/select-sourcing-approach.md).

    **Note:** If you have skipped negotiations at this stage, you have the option to work on negotiations after the qualification is complete. You can add the sourcing request to an exiting sourcing event or create a new sourcing event as required, before working with the sourcing event.


## Negotiation setup playbook

![Negotiation setup playbook](../image/pb-nego-setup.png)

The sourcing event playbook, also known as the negotiation setup playbook, enables you to:

-   Review and add sourcing requests and purchase lines, if necessary.
-   Review and add suppliers, if necessary.
-   Manage qualification work.

    For more information on this, see [Set up negotiations with suppliers and manage qualifications in playbook](../task/nego-with-suppliers-through-qual.md).

    **Note:** This action in available in both the playbooks, depending on when you want to get started with managing qualification work.


## Configurations

The playbook stages and activities of sourcing requests and sourcing events can be modified by the customer from Playbooks. ​The Declarative Actions can be edited or newly created, and their mappings modified in the Activity Definition section. The look and feel of the activities can also be configured from Activity Experience in the Activity Definition section.​

For details on how administrators, agents, and fulfillers can configure playbooks, see [Running playbooks](https://www.servicenow.com/docs/access?context=playbook-agents-and-fulfillers&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US). For more information on Playbooks stages and activities, see [Stages and activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Troubleshooting

If your playbook activities aren’t working as expected, perform these actions.

1.  Navigate to the respective process in Playbooks. For sourcing requests and sourcing events, the processes are Sourcing Intake and Negotiation Setup respectively.​
2.  Within the process, go to the corresponding activity that is not working as expected.​ For example, in the Sourcing approach section, which is the second stage of the playbook:
    -   If stage 2.1 is skipped, it should go to the Qualification workflow.​
    -   If stage 2.1 is completed, it should go to the Add to an existing negotiation workflow.​
    -   If stage 2.1 is canceled, it should go to the Create new sourcing event workflow.​
3.  Under the **Automation** tab, navigate to the corresponding subflow in Workflow Studio.​
4.  Open the executions of the subflow and check further.​
5.  To check the activity experiences, go to the sys\_pd\_process\_definition table and check the process configurations. This table contains all the activity definition configurations and action mappings for Declarative Actions.​

-   **[Review details and request clarification on a sourcing request in playbook](../task/review-details-request-clari-sr.md)**  
Get complete clarity on a sourcing request by reviewing the intake details, purchase lines, and approvals, and requesting clarification on the request, if necessary. You can perform these actions from the Request details section of the sourcing intake playbook.
-   **[Select a sourcing approach in playbook](../task/select-sourcing-approach.md)**  
Decide if you want to negotiate with suppliers right away, or skip this step and start qualifying the sourcing request instead. You can perform these actions from the Sourcing approach section of the sourcing intake playbook.
-   **[Set up negotiations with suppliers and manage qualifications in playbook](../task/nego-with-suppliers-through-qual.md)**  
Work on a negotiation setup playbook to manage qualification work, and review the sourcing requests, suppliers, and purchase lines, all within the premises of a sourcing event.

**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook](../task/process-purchase-order.md)

[Process a purchase requisition edit request in playbook](../task/playbook-edit-request-flow.md)

[Process a return request in playbook](../task/playbook-return-request.md)

[Process a replacement request in playbook](../task/playbook-replacement-request.md)

[Process an edit receipt request in playbook](../task/playbook-process-edit-receipt.md)

[Fulfilling request for copy of contract in playbook](fulfilling-request-for-contract.md)

[Routing NDAs to suppliers](routing-ndas-to-suppliers.md)

[Verifying delivery addresses in playbook](delivery-address-in-playbook.md)

[Reviewing and updating general ledger details in playbook](general-ledger-details-in-playbook.md)

[Streamlining the supplier risk assessment workflow](simplify-risk-assessment-wf.md)

