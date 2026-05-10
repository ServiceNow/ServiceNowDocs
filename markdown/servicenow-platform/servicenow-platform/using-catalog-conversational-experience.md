---
title: Catalog Conversational Coverage
description: ServiceNow Catalog Conversational Coverage provides a dashboard to view a high-level overview of the conversational and non-conversational catalog items.The dashboard shows the information that you need in graphs and a table.View the details page for your catalog item. If your item is non-conversational, view why your catalog item isn’t conversational and review the suggestions to know what you can do to make the item conversational.Use the ServiceNow AI Platform to view the dashboard that shows the catalog items that are conversational or non-conversational. Understand why catalog items aren't conversational, and explore the potential suggestions that might help make the items conversational.Use Catalog Builder to view the dashboard that shows the catalog items that are conversational or non-conversational. Understand why catalog items aren’t conversational, and explore the potential suggestions that might help make the items conversational.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# Catalog Conversational Coverage

ServiceNow® Catalog Conversational Coverage provides a dashboard to view a high-level overview of the conversational and non-conversational catalog items.

You can view this information in the Conversational catalog overview dashboard. The dashboard displays a graphical representation of various reports, such as the number of conversational and non-conversational catalog items, reasons that make the items non-conversational, and popular request channels. It also shows a list of the catalog items, their conversational status, and other details.

**Note:** You can access the conversational catalog dashboard only if you’ve installed the Now Assist in Conversational Catalog Request app. Conversational catalog dashboard can’t be installed separately as it's bundled with Now Assist in Conversational Catalog Request.

Drilling down the catalog items, you can view the details, for example, whether they’re conversational or non-conversational and why the items are non-conversational. Explore the potential suggestions for non-conversational items that might help you make items conversational.

If you have any of the following roles, you can view the dashboard:

-   Catalog administrator \[catalog\_admin\]
-   Catalog manager \[catalog\_manager\]
-   Catalog editor \[catalog\_editor\]

To access and view the dashboard, you must install and activate the Catalog Conversational Experience plugin \(sn\_catalog\_con\_cov\). You can find the plugin in the ServiceNow® Store.

**Note:** If you've installed Now Assist for conversation request submission plugin, you get the Catalog Conversational Experience plugin \(sn\_catalog\_con\_cov\) by default.

The **Update catalog items conversational status** scheduled job pulls conversational data of catalog items. This scheduled job updates the reasons for the catalog items. The scheduled job runs once in three days automatically. But to get the latest data when you need, run this job manually.

**Related topics**  


[Configure Now Assist in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-gen-ai-catalog-item.md)

[View the conversational catalog overview dashboard using Catalog Builder](using-catalog-conversational-experience.md#)

## Conversational catalog overview dashboard

The dashboard shows the information that you need in graphs and a table.

You can view the data of only those catalog items you have edit access to.

**Note:** You can access the conversational catalog dashboard only if you’ve installed the Now Assist in Conversational Catalog Request app. Conversational catalog dashboard can’t be installed separately as it's bundled with Now Assist in Conversational Catalog Request.

In the graphical representation of reports, you can view the following information:

<table id="table_m2w_jr3_d1c"><thead><tr><th>

Graphical representation of reports

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conversational and non-conversational item count

</td><td>

The number of catalog items that are conversational and non- conversational.

</td></tr><tr><td>

Reasons that make items non-conversational

</td><td>

Reasons for catalog items to be non-conversational. For example, having unsupported questions or scripted UI policies make the item non-conversational.

</td></tr><tr><td>

Popular request channels - last 6 months

</td><td>

The channel distribution of catalog item requests that have been submitted in the last six months.

</td></tr></tbody>
</table>The Catalog items section shows the following information:

<table id="table_ht4_rr3_d1c"><thead><tr><th>

Column name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog item

</td><td>

Name of the catalog item.

 You can select the name to open the catalog item details page.

</td></tr><tr><td>

Conversational status

</td><td>

Conversational or non-conversational status of the catalog item.

</td></tr><tr><td>

VA render type

</td><td>

Type of catalog item rendering. Based on the configuration of the catalog item, the render type is determined to be conversation, window, or popup.

</td></tr><tr><td>

Number of requests

</td><td>

Number of requests that corresponds to the requests submitted in the last six months.

</td></tr><tr><td>

Number of recommendations

</td><td>

The recommendations to enable or further improve the catalog item to target the conversational channel.

</td></tr><tr><td>

State

</td><td>

The status of the catalog item.

</td></tr><tr><td>

Owner

</td><td>

Name of the owner of the catalog item.

</td></tr><tr><td>

Updated

</td><td>

Date and time when the catalog item was last edited.

</td></tr></tbody>
</table>**Related topics**  


[View the conversational catalog overview dashboard using Catalog Builder](using-catalog-conversational-experience.md#)

[View the conversational catalog overview dashboard using the ServiceNow AI Platform](using-catalog-conversational-experience.md#)

[Catalog item conversational details page overview](using-catalog-conversational-experience.md#)

[Catalog Conversational Coverage](using-catalog-conversational-experience.md#)

## Catalog item conversational details page overview

View the details page for your catalog item. If your item is non-conversational, view why your catalog item isn’t conversational and review the suggestions to know what you can do to make the item conversational.

You can view this page only if you have any of the following roles:

-   Catalog administrator \[catalog\_admin\]
-   Catalog manager \[catalog\_manager\]
-   Catalog editor \[catalog\_editor\]
-   Catalog builder editor \[catalog\_builder\_editor\]

**Note:** The catalog manager, catalog editor, and catalog builder editor can view the details page only if they have edit access to the catalog item.

The page displays the following information related to conversational or non-conversational catalog items:

-   Name of the catalog item
-   Conversational status and render type
-   Date and time when the catalog item was last updated
-   The **Conversational readiness** and **Item details** tabs

    The **Conversational readiness** tab shows the Recommended Actions and the Required Actions \(If required actions are available\) sections. The recommended actions are useful to improve your catalog item for conversational channel. Required actions are useful to make your catalog items conversational.

    The **Item details** tab shows the details, such as a short description, description, and image of the item if available.

    **Note:** If any action is required to make a catalog item conversational, the action is displayed in the Required Actions section.


After going over the recommendations to make the item conversational, select **Edit in advanced view** if you want to make changes. The catalog item opens in the ServiceNow AI Platform for editing.

**Note:**

-   Only the catalog admin, catalog manager, and catalog editor can view the **Edit in advanced view** button.
-   If you're viewing a catalog item that's in the checked out state, you view its data that corresponds to the published version of the item. Any changes to the draft of the catalog item won’t be reflected here until it’s published.

By default, all catalog items are conversational. To make the catalog item non-conversational, select the **Make the item non-conversational in VA** check box in ServiceNow AI Platform®.

**Important:** Select the **Turn off Now Assist \(LLM\)** check box if you don't want the data of the catalog item \(and user responses\) to be sent to the LLM for security reasons, in case the catalog item contains sensitive data. Selecting this option ensures that this item will invoke the NLU topic block if it’s compatible, otherwise, it will show up either as a pop-up or as a link depending on the item's configuration. Restrictions on the NLU topic block are stricter than the LLM topic block and therefore a conversational item in the LLM topic block \(as shown in the Conversational Catalog Overview dashboard\) may not be conversational in the NLU topic block.

**Related topics**  


[Conversational catalog overview dashboard](using-catalog-conversational-experience.md#)

[View the conversational catalog overview dashboard using Catalog Builder](using-catalog-conversational-experience.md#)

[View the conversational catalog overview dashboard using the ServiceNow AI Platform](using-catalog-conversational-experience.md#)

[Catalog Conversational Coverage](using-catalog-conversational-experience.md#)

[Topic blocks to request catalog items through conversational experience](request-topic-blocks-va-llm.md)

## View the conversational catalog overview dashboard using the ServiceNow AI Platform

Use the ServiceNow AI Platform to view the dashboard that shows the catalog items that are conversational or non-conversational. Understand why catalog items aren't conversational, and explore the potential suggestions that might help make the items conversational.

### Before you begin

Verify that you’ve installed the Catalog Conversational Experience plugin \(sn\_catalog\_con\_cov\).

Role required: catalog\_admin, catalog\_manager, and catalog\_editor

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  On the Catalog Items list page, select **Conversational Overview**.

    The Conversational catalog overview dashboard opens, and you can view only those catalog items you own or can edit.

    **Note:**

    -   To view the dashboard, you can also navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Conversational catalog overview**.
    -   On a specific catalog item page, select **View conversational details** to open the catalog item’s details page, which shows the reasons and suggestions.

## View the conversational catalog overview dashboard using Catalog Builder

Use Catalog Builder to view the dashboard that shows the catalog items that are conversational or non-conversational. Understand why catalog items aren’t conversational, and explore the potential suggestions that might help make the items conversational.

### Before you begin

Verify that you’ve installed the Catalog Conversational Experience plugin \(sn\_catalog\_con\_cov\).

Role required: catalog\_admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.

2.  Select the **Dashboard** tab.

3.  In the Conversational Coverage in VA section, select **View conversational coverage**.

    The Conversational catalog overview dashboard opens. To view the conversational details page for a specific catalog item, on the dashboard, select the catalog item name. The details page opens.

    **Note:** You can also open a catalog item details page to view its conversational details. To do so, select the **Catalog items** tab, select an item that you want to view the details for, and select **View conversational details**.


**Related topics**  


[Edit a catalog item in Catalog Builder](../task/edit-cat-item-cat-builder.md)

