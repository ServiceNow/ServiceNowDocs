---
title: Now Assist for Software Asset Management \(SAM\) AI agent collection to create software reclamation rule
description: Use the Create software reclamation rule agentic workflow to automatically create reclamation rules to aggregate usage records and to identify unused software products that lack reclamation rules but are viable candidates.
locale: en-US
release: yokohama
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2025-08-07"
reading_time_minutes: 3
breadcrumb: [Using agentic workflows in Now Assist for SAM, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Now Assist for Software Asset Management \(SAM\) AI agent collection to create software reclamation rule

Use the Create software reclamation rule agentic workflow to automatically create reclamation rules to aggregate usage records and to identify unused software products that lack reclamation rules but are viable candidates.

## Create software reclamation rule overview

Use the Create software reclamation rule agentic workflow to streamline and automate the creation of reclamation rules. Create reclamation rule without having to manually review a product’s utilization and spend thereby improving license utilization, faster turnaround, improved operational efficiency, and enhanced user satisfaction.

## Create software reclamation rule agentic workflow

Automating the creation of reclamation rules helps SAM managers to scale their reclamation efforts by automatically identifying and suggesting reclamation rules for overlooked software.

To start the agentic workflow, you must have the sam\_admin role.

The Create reclamation rule agentic workflow can be initiated from the following pages:

-   Software asset overview page
-   Publisher details page
-   License operations page

Depending on the page, the sam\_admin role is on, follow the steps mentioned in the following table:

<table id="table_jgm_jjc_lgc"><thead><tr><th>

Software asset overview page

</th><th>

Publisher details page

</th><th>

License operations page

</th></tr></thead><tbody><tr><td>

1.  Navigate to the Activity center.
2.  Select **suggestions** in the **Reclamation rules** box in the Activity center.
3.  Select the sparkle icon on the top-right side of the workspace to open the Now Assist panel.

If the Now Assist panel is already open, select the hamburger icon.

4.  Select **Create reclamation rule** in the Active section the Now Assist panel.
5.  Select a product from a list of products that need reclamation rules and then select **Submit**.

The agentic workflow is initiated.


</td><td>

1.  Select a product for the specific publisher.
2.  Select the Removal candidates tab.
3.  Select **Create reclamation rule**.
4.  Select the sparkle icon on the top-right side of the workspace to open the Now Assist panel.

If the Now Assist panel is already open, select the hamburger icon.

The agentic workflow is initiated.


</td><td>

1.  Navigate to **Administration** &gt; **Reclamation Rules**.
2.  Select **Create reclamation rule**
3.  Select the sparkle icon on the top-right side of the workspace to open the Now Assist panel.

If the Now Assist panel is already open, select the hamburger icon.

4.  Select a product from a list of products that need reclamation rules and then select **Submit**.

The agentic workflow is initiated.


</td></tr></tbody>
</table>The AI agent initiates a series of checks assessing factors such as the usage of the product with regard to spend and utilization, among other metrics. After the checks are completed, the AI agent provides you with details such as the name of the reclamation rule name, the assignment group with which the reclamation rules will get created. You’re then asked if you would like to create the reclamation rule with the given details or if you want to modify any parameters such as assignment group in the reclamation rule. Mention any modifications that you want; or else confirm that you want to go ahead with the creation of the reclamation rule. After you confirm, the reclamation rule gets created along with the name of the product and a link to the reclamation rule. The Activity tab in the reclamation rule record gets updated with the relevant work notes.

## AI agents used in the Create software reclamation rule agentic workflow

|AI agent|AI agent role|
|--------|-------------|
|Software reclamation rule creation AI agent|Retrieves reclamation rule suggestions, analyzes the license utilization, and generates a reclamation rule for a software product.|

**Parent Topic:**[Using agentic workflows in Now Assist for SAM](using-now-assist-sam-ai-agents-usecases.md)

