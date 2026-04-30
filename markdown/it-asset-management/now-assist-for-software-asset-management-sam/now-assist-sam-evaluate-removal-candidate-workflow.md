---
title: Now Assist for Software Asset Management \(SAM\) AI agent collection to evaluate software removal candidate agentic workflow
description: Use the Evaluate software removal candidate agentic workflow to assess installed or subscription-based software for potential removal by analyzing their usage over a specified period and determining the total number eligible for removal. After user confirmation, the workflow initiates the eligible removal candidate for reclamation.
locale: en-US
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2025-08-05"
reading_time_minutes: 4
breadcrumb: [Use agentic workflows, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Now Assist for Software Asset Management \(SAM\) AI agent collection to evaluate software removal candidate agentic workflow

Use the Evaluate software removal candidate agentic workflow to assess installed or subscription-based software for potential removal by analyzing their usage over a specified period and determining the total number eligible for removal. After user confirmation, the workflow initiates the eligible removal candidate for reclamation.

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Evaluate software removal candidate overview

Use the Evaluate software removal candidate agentic workflow to identify and evaluate genuine software removal candidates and recommend software installations for reclamation, based on a series of intelligent checks that help ensure sufficient context for safe removal actions.

Ensure that you have the following prerequisites for running the Evaluate software removal candidate agentic workflow:

-   Your organization has a software asset management system integrated with AI agents.
-   Access an AI-driven now-asset panel.
-   AI agents have access to reclamation rules, removal candidates, products, and license metric results.

## Role masking

Roles required: sam\_user.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Evaluate software removal candidate agentic workflow

By automatically examining and verifying software removal candidates, the Evaluate software removal candidate agentic workflow helps in reducing manual effort, minimizing compliance risk, and unlocking measurable license cost savings.

Any removal candidates that is in the **Ready** state can be reclaimed.

To start the agentic workflow, you must have the sam\_user role or the sam\_admin role.

The Evaluate removal candidates agentic workflow can be initiated from the following pages:

-   Software asset overview page
-   Publisher details page; both from the publisher level as well as from the product level.

Depending on the page you are on, follow the steps mentioned in the following table:

<table id="table_jgm_jjc_lgc"><thead><tr><th>

Software asset overview page

</th><th>

Publisher details page- publisher level

</th><th>

Publisher details page- product level

</th></tr></thead><tbody><tr><td>

1.  Navigate to the Activity center.
2.  Select **suggestions** in the **Removal candidates** box in the Activity center.
3.  Select the sparkle icon on the top-right side of the workspace to open the Now Assist panel.

If the Now Assist panel is already open, select the hamburger icon.

4.  Select **Evaluate removal candidates** in the Active section in the Now Assist panel.
5.  Select a product from a list of products that need reclamation rules, to initiate the agentic workflow.

</td><td>

1.  Navigate to **License usage** &gt; **Publishers** &gt; **Removal candidates tab**
2.  Select **Evaluate removal candidates**.
3.  Select the sparkle icon on the top-right side of the workspace to open the Now Assist panel.

If the Now Assist panel is already open, select the hamburger icon.

The chat window shows your products narrowed down to the specific publisher.

4.  Select a product from a list of products that need reclamation rules, to initiate the agentic workflow.

</td><td>

1.  Navigate to **License usage** &gt; **Publishers** &gt; **Removal candidates tab**
2.  Select **Evaluate removal candidates**.
3.  Select the sparkle icon on the top-right side of the workspace to open the Now Assist panel.

If the Now Assist panel is already open, select the hamburger icon to initiate the agentic workflow.


</td></tr></tbody>
</table>The AI agent initiates a series of checks using multiple criteria, assessing factors such as the product ID, whether it's installed or subscription-based software, and its last usage, among other metrics. If any check fails, the Now Assist panel displays an error message indicating that the workflow can’t continue. If all the checks are successful, a message appears to indicate the number of removal candidates identified for the particular product. You’re then asked if you would like to reclaim the software. If you confirm, the reclamation process gets initiated and the state of the removal candidates changes from **Ready** to **Awaiting User**. You can navigate to the Removal candidates tab in the License Usage view to see the removal candidates and their current state. After the process is complete, you’re informed about all the removal candidates that were successfully reclaimed for the specific product.

Once a removal candidate has been reclaimed by the agentic workflow, the Activity tab in the removal candidate record is updated with relevant work notes.

## AI agents used in the Evaluate software removal candidate agentic workflow

|AI agent|AI agent role|
|--------|-------------|
|Software removal candidate evaluation AI agent|Identifies or proposes users for removal from a software product by assessing their usage within a set time frame and ensuring that the total number of eligible candidates for reclamation is notified to the user, while excluding any VIP users.|

**Important:** This agent is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Using agentic workflows in Now Assist for SAM](using-now-assist-sam-ai-agents-usecases.md)

