---
title: Now Assist for Software Asset Management \(SAM\) AI agent collection to evaluate software removal candidate agentic workflow
description: Use the Evaluate software removal candidate agentic workflow to assess installed or subscription-based software for potential removal by analyzing their usage over a specified period and determining the total number eligible for removal. After user confirmation, the workflow proceeds to reclaim the eligible software, effectively removing them.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Now Assist for Software Asset Management \(SAM\) AI agent collection to evaluate software removal candidate agentic workflow

Use the Evaluate software removal candidate agentic workflow to assess installed or subscription-based software for potential removal by analyzing their usage over a specified period and determining the total number eligible for removal. After user confirmation, the workflow proceeds to reclaim the eligible software, effectively removing them.

## Evaluate software removal candidate overview

Use the Evaluate software removal candidate agentic workflow to identify and evaluate genuine software removal candidates and recommend software installations for reclamation, based on a series of intelligent checks that ensures sufficient context for safe removal actions.

Ensure that you have the following prerequisites for running the Evaluate software removal candidate agentic workflow:

-   Your organization has a software asset management system integrated with AI agents.
-   Access an AI-driven now-asset panel.
-   AI agents have access to reclamation rules, removal candidates, products, and license metric results.

## Evaluate software removal candidate agentic workflow

By automatically examining and verifying software removal candidates, the Evaluate software removal candidate agentic workflow helps in reducing manual effort, minimizing compliance risk, and unlocking measurable license cost savings.

Any removal candidates that is in the **Ready** state can be reclaimed

To initiate the agentic workflow, perform the following steps:

1.  In the Software Asset Workspace, navigate to one of these pages:
    -   **License usage** &gt; **Removal candidates**
    -   **License usage** &gt; **Publishers** &gt; **Removal candidates tab**
2.  Select **Evaluate removal candidates**.
3.  Select the sparkle icon on the top right side of the workspace.

    The Now Assist Panel prompts you to select a product for evaluating software removal candidates.

    The prompt changes based on the page from where you initiated the agentic workflow:

    -   If you start from the Removal candidates page, you are prompted to choose a product from all the available publishers.
    -   If you start from the Publisher details page, the products are narrowed down to the specific publisher.
    -   If you start from the software model results tab within the Publisher details page, you are prompted to select removal candidates only for that particular product.
4.  Select a product and then select **Submit**.

    The AI agent initiates a series of checks using multiple criteria, assessing factors such as the product ID, whether it's installed or subscription-based software, and its last usage, among other metrics. If any check fails, the Now Assist Panel displays an error message indicating that the workflow cannot continue. If all the checks are successful, a message appears indicating the number of removal candidates identified for the particular product. You are then asked if you would like to reclaim the software. If you confirm, the reclamation process begins. After the process is complete, you are informed about all the removal candidates that were successfully reclaimed for the specific product.

    Once a removal candidate has been reclaimed by the agentic workflow, the Activity tab in the removal candidate record is updated with relevant work notes.


## AI agents used in the Evaluate software removal candidate agentic workflow

|AI agent|AI agent role|
|--------|-------------|
|Software removal candidate evaluation AI agent.|Identifies or proposes users for removal from a software product by assessing their usage within a set time frame and ensuring that the total number of eligible candidates for reclamation is notified to the user, while excluding any VIP users.|

**Parent Topic:**[Using agentic workflows in Now Assist for SAM](using-now-assist-sam-ai-agents-usecases.md)

