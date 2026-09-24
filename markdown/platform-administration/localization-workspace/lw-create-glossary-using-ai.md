---
title: Create a glossary using AI
description: In Language Asset Management, generate a glossary containing terms extracted from Knowledge Base articles. The Globalization Terminology Agent uses an AI skill to scan your article content and create a list of suggested terms and definitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-create-glossary-using-ai.html
release: brazil
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Globalization Terminology Agent, Language Asset Management, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a glossary using AI

In Language Asset Management, generate a glossary containing terms extracted from Knowledge Base articles. The Globalization Terminology Agent uses an AI skill to scan your article content and create a list of suggested terms and definitions.

## Before you begin

Activate the generate glossary skill. For information, see [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-a-now-assist-skill.md).

Confirm the articles you want included in the scan. Articles must be labeled as English language and published in the Knowledge Base. For information see [Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/knowledge-center.md).

Role required: sn\_lw.terminology\_manager \(default\)

## About this task

The following procedure is divided into two broad stages:

-   First, a search retrieves a list of possible knowledge articles. You can select articles from this list.
-   Next, the generate glossary skill analyzes your selected articles to extract suggested terms and definitions. You can review and edit the suggestions.

Both stages may take some time, depending on the count of articles and words. When each stage finishes the system sends an email to let you know that the results are ready for your review.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language Asset Management**.

2.  With the Glossaries tab open, select **Create glossary**.

    **Note:** This button is available only when the generate glossary skill has been activated.

3.  In the **Create AI-powered Glossary** modal window, enter a unique name for your glossary and \(optionally\) a description.

    \[Omitted image "lw-create-glossary-using-ai-glossname.png"\] Alt text: In the Create AI-powered Glossary modal window, the Glossary name and Description fields contain example values.

4.  Select **Next**.

5.  In the **Use the optional filters to refine your search** step, you can adjust the following filters to limit the KB articles retrieved.

<table id="choicetable_hjn_rxs_hkc"><tbody><tr><td id="d365761e162">

**Updated from**

</td><td>

You can choose a date range using the calendar picker or by entering specific dates. -   This limits the articles by the Updated date in the Knowledge \[kb\_knowledge\] table.
-   If you don't apply a date filter, all published articles are candidates.


</td></tr><tr><td id="d365761e179">

**Search my articles only**

</td><td>

When the check box is selected \(checked\), the search retrieves only articles authored by the current user.

</td></tr><tr><td id="d365761e188">

**Minimum number of views**

</td><td>

You can enter a view count number. The search retrieves only articles with a view count greater than or equal to this number. The default of 0 \(zero\) means that the search also retrieves articles that have never been viewed.

</td></tr></tbody>
</table>    \[Omitted image "lw-create-glossary-using-ai-searchfilters.png"\] Alt text: In the Create AI-powered Glossary modal window, optional filters are available. You can filter by updated date, whether authored by you, or view count.

6.  Select **Search for items** to retrieve KB articles.

    \[Omitted image "lw-create-glossary-using-ai-searchingitems.png"\] Alt text: After selecting Search for items, the modal window closes and the list of Glossaries is displayed. A banner announces "Searching for items: you will receive an email when the search is complete".

    The **Create AI-powered Glossary** modal window closes during the retrieval of KB articles. The search may take some time, so the system sends you an email when finished.

    -   In the list of Glossaries, the State of your glossary displays as **Searching items** while searching.
    -   The State changes to **Items available for selection** when the search is finished and the list of KB articles is ready.
7.  Select the name of your glossary from the list when its State has changed to **Items available for selection**.

8.  In the **Create AI-powered Glossary** modal window, choose articles for scanning by selecting their check boxes in the Filter column.

    **Tip:** You can bulk select all articles with the **Select all rows** check box in the header. You can also filter articles by terms in the article title, by view count, or by word count, using the column filter row.

    \[Omitted image "lw-create-glossary-using-ai-selectarticles.png"\] Alt text: The Create AI-powered Glossary window opens again when you select your glossary name after the search is finished. You can select specific articles from the retrieved list, or you can bulk select all articles.

9.  Adjust the articles you select according to the maximum word limit for terminology extraction.

    The default maximum word limit for scanning is 25,000. The modal window provides a running total of words based on the articles you have selected, and also the remaining balance. \[Omitted image "lw-create-glossary-using-ai-wordcount.png"\] Alt text: After you select some knowledge articles, the modal window displays the total word count and the balance remaining. In this example, the number of words selected is 14017, and the number of words remaining is 10983.

10. Select **Create AI Glossary**.

    The Create AI-powered Glossary modal window closes during the process of analysis. The State of your glossary displays as **Creating terms** in the Glossaries list. A banner informs you that you will receive an email when the process is complete.\[Omitted image "lw-create-glossary-using-ai-extracting.png"\] Alt text: The modal window is closed. On the list of Glossaries, a banner displays "Extracting term candidates: you will receive an email when the extraction process is complete, and the terms are ready for review."

11. When the email arrives and the State of your glossary changes to **Terms available for approval**, select the Glossary Name to open the **Review AI-Generated Terms** modal window.

    Initially all terms display **Pending Review** in the Status column.

12. Edit values in the Term, Definition, or Part of Speech columns by double clicking the text, modifying, then selecting **Apply**.

13. Reject rows by selecting their check boxes, then selecting **Reject Selected**.

    The Status changes to `Rejected`. Rejected rows aren't included in the final glossary. If all rows are rejected, the **Publish** button disappears.

14. Approve rows by selecting their check boxes, then selecting **Approve Selected**.

    Only approved rows are included in the published glossary. The Publish button appears when at least one row is approved.

15. Select **Publish** to finalize.

    \[Omitted image "lw-create-glossary-using-ai-publish.png"\] Alt text: In the Review AI-Generated Terms, several example rows show both Approved and Rejected in the status column. The Publish button is highlighted.

    The Status of your glossary changes to **Completed**.


## Result

Your published glossary is listed in the Glossaries table in Language Asset Management. You can access the list of terms from the Glossary Sources tab.

## What to do next

You can modify your glossary, including adding translations to the terms. For information see [Edit a glossary in Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-edit-glossary.md).

You can export your glossary for review by stakeholders. For information see [Export a glossary from Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-export-glossary.md).

**Parent Topic:**[Globalization Terminology Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-terminology-agent.md)

**Related topics**  


[Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-a-now-assist-skill.md)

[Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/knowledge-center.md)

