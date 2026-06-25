---
title: Sourcing intake guided experience with playbooks
description: As sourcing managers, you can use the sourcing intake and negotiation setup playbooks to guide you through the complex request intake process so that you can focus on actual productive work such as negotiating savings from suppliers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/sourcing-intake-guided-exp.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Working with playbooks, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing intake guided experience with playbooks

As sourcing managers, you can use the sourcing intake and negotiation setup playbooks to guide you through the complex request intake process so that you can focus on actual productive work such as negotiating savings from suppliers.

The sourcing intake playbook and the negotiation setup playbook embedded in the sourcing intake playbook as a flow, guide you through these actions with clear steps to view your progress​.

Here's a quick breakdown of the playbooks and their associated tasks.

## Sourcing intake playbook

The sourcing request playbook, also known as the sourcing intake playbook, enables you to:

-   Review an employee or requester’s requirements, which include details of the sourcing intake, purchase lines, and approvals.
-   Request clarifications or more information from the requester, if necessary.
-   Collaborate with cross-functional teams and create other work such as tasks and cases for them, if necessary.​

    For more information on how to perform these actions on the sourcing intake playbook, see [Review details and request clarification on a sourcing request in playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/review-details-request-clari-sr.md).

-   Decide if you should negotiate in a sourcing event or not.

    Here, as the sourcing manager, you can select a sourcing approach to source with similar employee requests. You can decide whether to work on negotiations with suppliers right away or at a later stage. In case of the former, you must add the sourcing request to a new or existing sourcing event​ to proceed.

    For more information on how to perform these actions on the sourcing intake playbook, see [Select a sourcing approach in playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/select-sourcing-approach.md).

    **Note:** If you have skipped negotiations at this stage, you have the option to work on negotiations after the qualification is complete. You can add the sourcing request to an exiting sourcing event or create a new sourcing event as required, before working with the sourcing event.


## Negotiation setup playbook

The sourcing event playbook, also known as the negotiation setup playbook, enables you to:

-   Review and add sourcing requests and purchase lines, if necessary.
-   Review and add suppliers, if necessary.
-   Manage qualification work.

    For more information on this, see [Set up negotiations with suppliers and manage qualifications in playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/nego-with-suppliers-through-qual.md).

    **Note:** This action in available in both the playbooks, depending on when you want to get started with managing qualification work.


## Configurations

The playbook stages and activities of sourcing requests and sourcing events can be modified by the customer from Playbooks. ​The Declarative Actions can be edited or newly created, and their mappings modified in the Activity Definition section. The look and feel of the activities can also be configured from Activity Experience in the Activity Definition section.​

For details on how administrators, agents, and fulfillers can configure playbooks, see [Running Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-agents-and-fulfillers.md). For more information on Playbooks stages and activities, see [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-lanes-activities.md).

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

-   **[Review details and request clarification on a sourcing request in playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/review-details-request-clari-sr.md)**  
Get complete clarity on a sourcing request by reviewing the intake details, purchase lines, and approvals, and requesting clarification on the request, if necessary. You can perform these actions from the Request details section of the sourcing intake playbook.
-   **[Select a sourcing approach in playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/select-sourcing-approach.md)**  
Decide if you want to negotiate with suppliers right away, or skip this step and start qualifying the sourcing request instead. You can perform these actions from the Sourcing approach section of the sourcing intake playbook.
-   **[Set up negotiations with suppliers and manage qualifications in playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/nego-with-suppliers-through-qual.md)**  
Work on a negotiation setup playbook to manage qualification work, and review the sourcing requests, suppliers, and purchase lines, all within the premises of a sourcing event.

**Parent Topic:**[Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/work-playbooks-spo.md)

**Related topics**  


[Process a purchase order edit in playbook]()

[Process a purchase requisition edit request in playbook]()

[Process a return request in playbook]()

[Process a replacement request in playbook]()

[Process an edit receipt request in playbook]()

[Fulfilling request for copy of contract in playbook]()

[Routing NDAs to suppliers]()

[Verifying delivery addresses in playbook]()

[Reviewing and updating general ledger details in playbook]()

[Streamlining the supplier risk assessment workflow]()

