---
title: Catalog item conversational details page overview
description: View the details page for your catalog item. If your item is non-conversational, view why your catalog item isn’t conversational and review the suggestions to know what you can do to make the item conversational.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Catalog Conversational Coverage, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog item conversational details page overview

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
-   The **Reasons and suggestions** and **Item details** tabs

    The **Reasons and suggestions** tab shows one or more reasons for the item being non-conversational and suggestions that might make the item conversational. If there’s more than one reason, you can select each reason to view the suggestions for that particular reason.

    The **Item details** tab shows the details, such as a short description, description, and image of the item if available.


After going over the reasons and suggestions for the non-conversational items, select **Edit in advanced view** if you want to make changes. The catalog item opens in the ServiceNow AI Platform for editing.

**Note:**

-   Only the catalog admin, catalog manager, and catalog editor can view the **Edit in advanced view** button.
-   If you're viewing a catalog item that's in the checked out state, you view its data that corresponds to the published version of the item. Any changes to the draft of the catalog item won’t be reflected here until it’s published.

By default, all catalog items are conversational. To make the catalog item non-conversational, select the **Make the item non-conversational in VA** check box.

![Make the item non-conversational in VA check box.](../image/non-conv-checkbox.png)

**Important:** Select the **Turn off Now Assist \(LLM\)** check box if you don't want the data of the catalog item \(and user responses\) to be sent to the LLM for security reasons, in case the catalog item contains sensitive data. Selecting this option ensures that this item will invoke the NLU topic block if it’s compatible, otherwise, it will show up either as a pop-up or as a link depending on the item's configuration. Restrictions on the NLU topic block are stricter than the LLM topic block and therefore a conversational item in the LLM topic block \(as shown in the Conversational Catalog Overview dashboard\) may not be conversational in the NLU topic block.

**Parent Topic:**[Catalog Conversational Coverage](../concept/using-catalog-conversational-experience.md)

**Related topics**  


[Conversational catalog overview dashboard](conversational-coverage-overview-dashboard.md)

[View the conversational catalog overview dashboard using Catalog Builder](../task/view-conversational-dashboard.md)

[View the conversational catalog overview dashboard using the ServiceNow AI Platform](../task/view-conv-cov-view-dashboard-platform.md)

[Catalog Conversational Coverage](../concept/using-catalog-conversational-experience.md)

[Service Catalog topic blocks in Virtual Agent powered by Now LLM](../concept/request-topic-blocks-va-llm.md)

