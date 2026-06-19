---
title: Review a savings opportunity and create a pipeline project
description: Open a savings opportunity discovered by the Savings Opportunity Discovery agentic workflow and create a pipeline project that tracks the savings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-create-pipeline.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 4
keywords: [Savings Opportunities, pipeline project, Now Assist Panel, savings opportunity details]
breadcrumb: [Action or dismiss an opportunity, Using Spend and Savings Management, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Review a savings opportunity and create a pipeline project

Open a savings opportunity discovered by the Savings Opportunity Discovery agentic workflow and create a pipeline project that tracks the savings.

## Before you begin

The Now Assist Panel deployment for the relevant Opportunity Finder agent must be active. The weekly Savings Opportunity Finder Agents Scheduled Job uses the same check before running each agent.

Role required: sn\_spend\_mgmt.sourcing\_category\_manager, sn\_spend\_mgmt.category\_manager\_admin, and sn\_spend\_pipeline.sourcing\_pipeline\_user

## About this task

Three agents create opportunity records: the Contract Optimization Opportunity Finder Agent, the Supplier Optimization Opportunity Finder Agent, and the Spend Optimization Opportunity Finder Agent. The **Learn more** action on an open opportunity card launches the Savings Opportunity Discovery use case, which routes to the correct agent based on the opportunity's lever.

While pipeline project creation is in progress, the opportunity status moves to **In progress** and the record is locked from changes by other users until the flow completes or is cancelled.

## Procedure

1.  From the **Workspaces** tab, select **Source-to-Pay Workspace**.

2.  Select the **Category management** tab.

3.  Do one of the following:

    -   In the Potential savings opportunities section, in the opportunity card you want to work on, select the three dots menu, and then select **Learn more**.

        \[Omitted image "spend-dismiss-learn-more-card.png"\] Alt text: Three dots menu on an opportunity card showing the Dismiss and Learn more options.

    -   In the Potential savings opportunities section, select **View all**. Then, in the Potential Savings Opportunities page, select **Learn more** for the opportunity you want to act on.

        \[Omitted image "spend-dismiss-learn-more.png"\] Alt text: Potential Savings Opportunities page showing the Learn more option on an opportunity card.

4.  Review the content in each section of the Now Assist Panel.

    -   **Opportunity Summary**: A narrative paragraph summarizing the total estimated savings, the supplier, the spend categories covered, the baseline contract spend, and the savings levers that produced the opportunity.
    -   **Key Insights**: A list of specific findings that support the opportunity, such as the current and proposed values for each savings lever and the cumulative savings attributable to each. The insights also include observations about contract utilization or spend patterns relevant to the finding.
    -   **Recommended Next Steps**: A list of suggested actions to progress the opportunity, such as reviewing the relevant contract clauses, engaging the supplier to confirm negotiated rates, or validating the savings calculation against actual spend.
    -   **What would you like to do next?**: Predefined options such as **Create pipeline project**, **How are savings calculated**, and **Ask anything** appear . The predefined options vary according to the opportunity type. Select an option or type directly in the chat input to continue the conversation.
    \[Omitted image "spend-nap-output.png"\] Alt text: Now Assist Panel showing Opportunity Summary, Key Insights, Recommended Next Steps, and follow-up options.

5.  Ask follow-up questions about the opportunity in the chat.

    For example, ask `How were the savings calculated?` , `Show the related contracts` , or `List the pipeline projects linked to this opportunity` . The agent calls the results appear in the chat without ending the conversation .

6.  Select **Create pipeline project**.

    The following pre-filled project details appear: **State** \(Draft\), **Short description**, **Estimated spend**, **Estimated savings**, **Start date** \(today\), **End date** \(contract end date for Contract Optimization; otherwise empty\), and **Project type** \(Supplier, Contract, or Spend Optimization\). \[Omitted image "spend-create-pipeline.png"\] Alt text: Now Assist Panel showing pre-filled pipeline project details for review.

7.  Review the pre-filled values and reply **Yes** to make changes or **No** to proceed.

    If you reply **Yes**, enter the field to change in the chat . The revised summary appears for confirmation before proceeding.

8.  Select a priority when prompted: **1 - Critical**, **2 - High**, **3 - Moderate**, **4 - Low**, or **5 - Planning**.

    Only values 1 through 5 are accepted; the agent re-prompts for an invalid value.

9.  Wait for the agent to create the pipeline project.

    The agent calls the pipeline project creation flow .

    On success, the agent returns the pipeline project number as a hyperlink along with the state, priority, and project type.

    If the pipeline project creation fails, an error message appears with an option to retry .

10. Choose whether to generate a chat summary when prompted with **Yes** or **No**.

    If you select **Yes**, the agent generates a 3–5 sentence work note covering the project description, estimated savings, start date, and recommended next steps.

11. Review the draft summary and reply **Yes** to make changes or **No** to confirm.

    If you reply **Yes**, provide the revisions in chat and confirm the updated summary before proceeding.

12. Select **Post to work notes** to attach the summary to the new pipeline project, or **End chat** to close the conversation.


## Result

A pipeline project record is created and linked to the opportunity, contracts, suppliers, and purchase orders referenced by the opportunity. The opportunity record is updated to reflect the action.

## What to do next

The following fields on the draft pipeline project are prefilled from the opportunity. Review and update any values before progressing the project.

|Field|Description|
|-----|-----------|
|**Short description**|Opportunity type and the related spend categories.|
|**Estimated spend**|Baseline or consolidated spend captured for the opportunity.|
|**Estimated savings**|Savings value calculated for the opportunity.|
|**Estimated start date**|Current date.|
|**Estimated end date**|Renewal start date when the opportunity is based on a contract. The contract end date is used as a fallback.|
|**Project type**|Determined by the opportunity type.|
|**Previous records**|Source records linked by opportunity type: contracts for contract optimization, purchase orders for spend optimization, and suppliers for supplier optimization.|

**Parent Topic:**[Action or dismiss a savings opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/action-or-dismiss-savings-opportunity.md)

