---
title: AI driven supplier onboarding using Now Assist for SLO
description: Use the AI driven supplier onboarding playbook to automate onboarding tasks such as supplier registration, information validation, and task list generation.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, generative AI, AI Agents, agentic AI, SLO AI Agent, SLO agentic AI]
breadcrumb: [Use, Now Assist for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# AI driven supplier onboarding using Now Assist for SLO

Use the AI driven supplier onboarding playbook to automate onboarding tasks such as supplier registration, information validation, and task list generation.

## Accessing the AI driven supplier onboarding playbook

To access the AI driven supplier onboarding playbook:

1.  In the decision builder, open the Supplier case playbook.
    1.  Change the existing playbook case type from **Onboard new supplier** to **AI driven supplier onboarding**.
    2.  Select **Save**.
2.  Set the default model for the One Extend capabilities.
    1.  Navigate to **Sys\_One\_Extend\_Capability**.
    2.  Open the Generic Prompt record.
        1.  Go to the OneExtend Definition Configs related list.
        2.  In the default column, ensure that at least one model is marked to **True**.
    3.  Open the Summarize record.
        1.  Go to the OneExtend Definition Configs related list.
        2.  In the default column, ensure that at least one model is marked to **True**.

## Available AI agents in AI driven supplier onboarding

The following table lists the agents that are used in the workflow.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** toggle is enabled to activate the AI agent.

<table id="table_i1m_r21_cfc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Supplier data steward AI agent

</td><td>

-   Ensures that the supplier data is accurate, compliant, and continuously maintained across systems. During onboarding, this agent also checks for duplicate supplier records.

**Note:** Duplicate supplier onboarding requests can be resolved from the Now Assist panel by updating the legal name or the email domain of the primary contact's email address.

-   Handles supplier onboarding by creating an invitation case for the supplier contact and assigning the necessary supplier tasks. Additionally, it ensures that the supplier case status is updated appropriately in the system.

</td></tr><tr><td>

Supplier approval AI agent

</td><td>

On approval, confirms supplier activation, activates supplier record and updates supplier company information, sends welcome email to the supplier, notifies the requester on onboarding status, and updates the case status to Closed complete.

 On rejection, provides a reason for rejection, sends an email to the supplier, notifies the requester and supplier about onboarding status, and updates the case to Closed rejected.

</td></tr><tr><td>

Supplier document strategy generator AI agent

</td><td>

-   Generates dynamic onboarding flows that are customized to meet the supplier's compliance and regulatory documentation requirements. Flows are customized based on the following two factors:

    -   The region in which the supplier is based.
    -   The industry in which the supplier operates.
-   Automatically creates tasks for the onboarding flow by referencing all published Knowledge Base \(KB\) articles.


</td></tr></tbody>
</table>**Note:** In the approval stage, supplier managers can also approve or reject supplier onboarding using the Yes and No buttons.

## Activities in the AI driven supplier onboarding playbook

<table id="table_x5f_nlw_h3c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI suggested similar suppliers

</td><td>

This activity is triggered when an onboarding request originates from a sourcing request. When a shopper selects an external supplier to fulfill a purchase request, an onboarding request is created automatically to onboard the external supplier.The AI suggested similar suppliers activity analyzes the sourcing request and suggests similar suppliers, eliminating the need to onboard a new supplier. You can select either of the following options to proceed:

-   Cancel the current onboarding request by selecting the reject button.
-   Continue with the current onboarding request by selecting the continue button.

</td></tr><tr><td>

AI driven primary data validation

</td><td>

This activity is triggered during the registration stage to validate banking details submitted by the supplier contact. It cross-references the banking details against the information in the attached proof and highlights any discrepancies, enabling the supplier relationship manager to resolve them.A supplier task is first created for the supplier contact to submit banking details through the Supplier Collaboration Portal. Once the supplier contact submits the banking details, the AI driven primary data validation activity is triggered. The supplier relationship manager can then choose to update either the record or the attached proof to resolve the discrepancies.

**Note:** Supplier contacts must select the **Extract values from the attachment to auto-populate form fields.** checkbox while completing the supplier banking information task to auto-populate bank name, account holder name, and account number.

</td></tr></tbody>
</table>The AI agent decision log displays the AI agents that are working to resolve the case, and you can watch their interactions, decisions, and thought processes as they happen in real time.

**Related topics**  


[Activate AI agents](../task/activate-ai-agents.md)

[Supplier document strategy generator AI agent](supplier-document-strategy-generator-ai-agent.md)

