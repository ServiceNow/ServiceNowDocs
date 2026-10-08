---
title: Configure a page card in AI Control Tower
description: Change how a card presents its data so that a page matches the terminology, level of detail, and reporting focus your organization works with.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configure-widget.html
release: australia
topic_type: task
last_updated: "2026-09-21"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring pages, Configure, AI Control Tower, Enable AI experiences]
---

# Configure a page card in AI Control Tower

Change how a card presents its data so that a page matches the terminology, level of detail, and reporting focus your organization works with.

## Before you begin

Role required: workspace administrator \[sn\_ai\_governance.workspace\_admin\]

## About this task

The settings available for a card depend on how that card gets its data. Cards that read directly from tables on your instance provide a condition builder in addition to their presentation settings. Cards that retrieve their data from an API provide presentation settings only. Saved changes apply to every user on the instance.

You can configure cards on all pages and tabs except Activity Center, the Inventory list views, the Policies tab, and Settings.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to the page that you want to configure.

3.  Select the edit icon \(\[Omitted image "aict-edit-widget.png"\] Alt text:\) to enter editor mode.

    A configuration control appears on each card that you can change.

4.  Select the configuration control on the card that you want to change.

5.  Change the settings for one or more cards.

    Leave a text field empty to keep the value that the card ships with.

<table><thead><tr><th align="left" id="d44815e132">

Common configuration options

</th><th align="left" id="d44815e135">

Description

</th></tr></thead><tbody><tr><td id="d44815e141">

**Title override**

</td><td>

Enter the text that you want to display in the title of the card.

</td></tr><tr><td id="d44815e150">

**Subtitle override**

</td><td>

Enter the text that you want to display in the subtitle of the card.

</td></tr><tr><td id="d44815e159">

**Empty-state message**

</td><td>

Enter the message that you want users to read when the card has no data to display.

</td></tr><tr><td id="d44815e171">

**Chart type**

</td><td>

Select the chart type that presents the data most clearly for your organization. For example, change a donut chart to a pie chart or a semi-donut chart or show a trend chart as an area chart.

</td></tr><tr><td id="d44815e184">

**Labels**

</td><td>

Adjust the label text to match the terms your organization uses.

</td></tr><tr><td id="d44815e193">

**Show category legend**

</td><td>

Show or hide the legend, depending on whether the labels repeat information that the chart already conveys.

</td></tr><tr><td id="d44815e202">

**Number of rows and sort order**

</td><td>

1.  Set the number of rows that you want a ranked list to display.
2.  Select the sort order so that the list opens on the records you want to review first, such as the lowest scores rather than the highest.


</td></tr><tr><td id="d44815e220">

**Additional filter**

</td><td>

1.  In the condition builder, select the field, operator, and value that limit the card to the records you want it to report on.
2.  Add more conditions as needed.
 The condition builder is available only for cards that read directly from tables on your instance. The condition also applies to the page that the card navigates to.

</td></tr><tr><td id="d44815e241">

**Show view-all arrow**

</td><td>

Show or hide the arrow icon to view all items.

</td></tr><tr><td id="d44815e250">

**View-all URL**

</td><td>

Enter the URL that you want the arrow icon to open, so that users move to the list or page your organization works from.

 This setting is available only for cards that already include an icon for navigating to another page.

</td></tr><tr><td id="d44815e266">

**Optional card elements**

</td><td>

Turn off the elements that your organization doesn't track, to reduce the amount of information on a page. For example, you might hide token statistics, trend lines, a filter dropdown, or the chart in a card that also displays a total.

</td></tr></tbody>
</table>    \[Omitted image "aict-edit-widget-example.png"\] Alt text: Configuration options shown when editing the Inventory card on the AI Control Tower Home page.

6.  Return a card to the settings it ships with by selecting **Reset**.

    You can reset a card whether or not you have already saved your changes to it. Resetting a saved configuration removes it for every user.

7.  Close the edit card panel.

8.  Save the configuration changes that you made for all cards in the current session by selecting **Save**.


## Result

AI Control Tower users see the configured cards the next time the page loads.

**Parent Topic:**[Configuring pages in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-page-widgets.md)

**Related topics**  


[Configuring pages in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-page-widgets.md)

[Creating or extending pages with pro-code tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-create-extend-pages-pro-code-tools.md)

