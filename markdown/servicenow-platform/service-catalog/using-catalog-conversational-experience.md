---
title: Catalog Conversational Coverage
description: ServiceNow Catalog Conversational Coverage provides a dashboard to view a high-level overview of the conversational and non-conversational catalog items.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
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

-   **[Conversational catalog overview dashboard](../reference/conversational-coverage-overview-dashboard.md)**  
The dashboard shows the information that you need in graphs and a table.
-   **[Catalog item conversational details page overview](../reference/catalog-item-conv-details-page-overview.md)**  
View the details page for your catalog item. If your item is non-conversational, view why your catalog item isn’t conversational and review the suggestions to know what you can do to make the item conversational.
-   **[View the conversational catalog overview dashboard using Catalog Builder](../task/view-conversational-dashboard.md)**  
Use Catalog Builder to view the dashboard that shows the catalog items that are conversational or non-conversational. Understand why catalog items aren’t conversational, and explore the potential suggestions that might help make the items conversational.
-   **[View the conversational catalog overview dashboard using the ServiceNow AI Platform](../task/view-conv-cov-view-dashboard-platform.md)**  
Use the ServiceNow AI Platform to view the dashboard that shows the catalog items that are conversational or non-conversational. Understand why catalog items aren't conversational, and explore the potential suggestions that might help make the items conversational.
-   **[Service Catalog topic blocks in Virtual Agent powered by NLU](request-topic-blocks-va.md)**  
You can design a topic conversation in the Virtual Agent powered by Natural Language Understanding \(NLU\) by including reusable topic blocks to perform request submission tasks.
-   **[Service Catalog topic blocks in Virtual Agent powered by Now LLM](request-topic-blocks-va-llm.md)**  
You can design a topic conversation in Virtual Agent powered Now LLM by including reusable topic blocks to perform request submission tasks.

**Parent Topic:**[Service Catalog](service-catalog.md)

**Related topics**  


[Configure Now Assist in Conversational Catalog Request](https://www.servicenow.com/docs/access?context=configure-gen-ai-catalog-item&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

[View the conversational catalog overview dashboard using Catalog Builder](../task/view-conversational-dashboard.md)

