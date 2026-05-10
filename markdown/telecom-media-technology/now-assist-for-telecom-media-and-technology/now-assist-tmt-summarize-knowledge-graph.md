---
title: Generate service summary for a product inventory using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Summarize the service details mentioning the current situation, any critical actions to be taken and find the root cause indicators using the knowledge graph and service summary skill.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Generate service summary for a product inventory using Now Assist for Telecommunications, Media and Technology \(TMT\)

Summarize the service details mentioning the current situation, any critical actions to be taken and find the root cause indicators using the knowledge graph and service summary skill.

## Before you begin

Role required: admin

## About this task

The customer service summary skill provides you with a concise summary of a sold product, including the current situation, root cause indicators, critical actions, resolution tasks, and resolution details.

The customer service summary skill is available in CSM/FSM Configurable Workspace, you use the Service Problem Case service summary skill by Now Assist component to generate a summary.

Install the Customer Service with Service Management \(com.sn\_cs\_sm\) plugin to display the activate button for customer service summary skills.

If there’s enough data, the customer service summary component displays the **Generate service summary** button.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Service Problem Case**.

2.  Open a service problem case.

3.  In the Verify tab, select **Service details**.

4.  In the Service details, select **Generate service summary**.

    ![generate service summary.](../image/now-assist-generate-summary.png)

    **Note:** Generating and displaying the summary may take several seconds.

5.  After you're finished summarizing the service, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d22488e145">

Option

</th><th align="left" id="d22488e148">

Procedure

</th></tr></thead><tbody><tr><td id="d22488e154">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(![Expand card icon.](../image/icon-expand.png)\).
-   To see fewer summary details, select the View less icon \(![Collapse card icon.](../image/icon-collapse.png)\).


</td></tr><tr><td id="d22488e184">

**Provide feedback for the summary**

</td><td>

-   If you think that the service summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d22488e217">

**Copy the service summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the service summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d22488e232">

**View the information about the case summary**

</td><td>

To check some details about the service summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
-   **[Create a knowledge graph schema](now-assist-tmt-create-knowledge-graph.md)**  
Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.
-   **[Customize a summary card for service summary](customize-uib-builder-service-summary.md)**  
Customize the summary card of the service summary and UI actions according to your needs.

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

