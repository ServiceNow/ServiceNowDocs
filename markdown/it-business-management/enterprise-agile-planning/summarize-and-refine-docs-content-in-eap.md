---
title: Summarize and refine Docs content in EAP using Now Assist for SPM
description: Use Now Assist capabilities to elaborate, shorten, and summarize selected content in Docs, or to get a summary of the whole document in Enterprise Agile Planning \(EAP\).
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Refine records, Now Assist skill, Now Assist, Gen AI, Generative AI, Strategic Portfolio Management, SPM]
breadcrumb: [Collaborate using Docs, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Summarize and refine Docs content in EAP using Now Assist for SPM

Use Now Assist capabilities to elaborate, shorten, and summarize selected content in Docs, or to get a summary of the whole document in Enterprise Agile Planning \(EAP\).

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

-   [Create a Doc in EAP](create-a-doc-in-eap.md).
-   Activate the EAP doc summarization Now Assist skill. See .

Role required: sn\_apw\_advanced.eap\_user

If you have custom roles that require access to this skill, update the ACLs for those roles that require access. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  Navigate to your Doc.

<table id="choicetable_wz1_jq3_bcc"><thead><tr><th align="left" id="d125925e177">

Type

</th><th align="left" id="d125925e180">

Actions

</th></tr></thead><tbody><tr><td id="d125925e186">

**Team Doc**

</td><td>

1.  Use the Agile structure in the navigation panel to open your team.
2.  Select the Docs tab and open your Doc.


</td></tr><tr><td id="d125925e204">

**Planning item Doc**

</td><td>

1.  From the Backlog or Planning board pages of a team, select a planning item.
2.  Select **Full details**.
3.  Select the Docs tab and open your Doc.


</td></tr></tbody>
</table>3.  From your Doc, open the page you want to summarize or refine.

4.  Choose to summarize the selected text on the page or the whole page.

    -   To refine the selected text:
        1.  Select a single block or multiple blocks of content on the page.
        2.  Select **Now Assist** and choose an option.

            1.  **Summarize** to summarize the selected text.
            2.  **Elaborate** to lengthen the selected text based on the existing context.
            3.  **Shorten** to make the selected text concise.
            ![Summarize, elaborate, or shorten the selected text](../images/eap-now-assist-selected-content.png)

    -   To summarize the entire content on the page, select **Now Assist** from the Doc header and select **Summarize**.

        ![Summarize the entire content on the page](../images/eap-now-assist-doc-summarize.png)

    **Tip:** If there’s more content to summarize, you can remove some text and retry.

    Now Assist analyzes the text and generates an output in a separate pop-up.

5.  Based on the output generated, you can further refine the result or insert the generated content into the Doc.

    ![Summarize selected content.](../images/eap-na-doc-summarization.png)

6.  Copy the generated output by selecting the Copy to clipboard icon \(![](../../now-assist-spm/images/icon-copy-spm.png)\) to use it for purposes such as sending an email, saving to notes, and others.

    **Important:** Because the output is AI-generated, review it to ensure accuracy.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../../now-assist-spm/concept/using-now-assist-for-spm.md)

