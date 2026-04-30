---
title: Resolve cases with knowledge and community content
description: Enable agents to resolve a case more quickly by searching for information from the knowledge base and community and, if helpful, associating it to the case.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage cases, Using Customer Service Management, Customer Service Management]
---

# Resolve cases with knowledge and community content

Enable agents to resolve a case more quickly by searching for information from the knowledge base and community and, if helpful, associating it to the case.

## Before you begin

Role required: sn\_customerservice\_agent

## About this task

The Case form displays contextual search results based on text entered in the **Short Description** field. These search results provide targeted knowledge articles, pinned articles, and community content to customer service agents.

Customer service agents can search for information that is related to a case when opening a case or in a case that is already open. If the search results in any related content, the agent can preview the content. If the information is relevant, the agent can mark it as helpful. Knowledge articles can be also attached to the case.

By default, search results include knowledge articles, pinned articles, and solved community questions and blogs. Depending on the configuration, search results can also include other types of information, such as open and resolved cases and problems. With the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\), you can also view similar cases and similar knowledge articles.

Customer service case managers can use the Demand Insights for Cases dashboard to identify which cases have no or insufficient knowledge coverage. For more information, see [Demand Insights for Cases dashboard](https://www.servicenow.com/docs/access?context=demand-insights-cases-dashboard&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Cases**.

2.  Perform one of the following actions.

    -   Open a new case and start typing in the **Short description** field.
    -   Open an existing case and click **Related Search Results**.
    Any matching search results are displayed in the **Related Search Results** section. The content displayed depends on the permissions assigned to the agent in Knowledge and Communities.

3.  Click one of the results to open the content in a pop-up window.

4.  Perform any of the following steps.

<table id="choicetable_i5f_ckh_ndb"><thead><tr><th align="left" id="d154085e123">

To

</th><th align="left" id="d154085e126">

Do this

</th></tr></thead><tbody><tr><td id="d154085e132">

**Attach a knowledge article to the case**

</td><td>

1.  Click **Attach** next to the knowledge article you want to attach to the case.
2.  If you opened the knowledge article, click **Attach to Case** in the pop-up window.

The knowledge article is displayed in **Activities** as a work note and is visible only to customer service agents. A link to the article is also entered in the **Additional comments** field.

3.  To make the article visible to customers, click **Post**.
 **Note:** You cannot attach Communities content to the Case form.

</td></tr><tr><td id="d154085e173">

**Mark the content as helpful for resolving the associated case**

</td><td>

Click **This helped** in the pop-up window.

</td></tr><tr><td id="d154085e185">

**Scroll to previous or next result**

</td><td>

Use the arrow keys to scroll up to the previous or down to the next result.

</td></tr></tbody>
</table>5.  Perform one of the following actions.

    -   If you opened a case, click **Submit**.
    -   If you updated an existing case, click **Update**.

