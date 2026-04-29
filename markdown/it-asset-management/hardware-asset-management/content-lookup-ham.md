---
title: Content lookup portal for Hardware Asset Management
description: The Content lookup portal gives you visibility into the data stored in the Content Library as part of the IT Asset Management Content Service via an intuitive user interface.Install the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application to view the data stored in the Hardware Asset Management Content Service.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Content lookup portal for Hardware Asset Management

The Content lookup portal gives you visibility into the data stored in the Content Library as part of the IT Asset Management Content Service via an intuitive user interface.

The Content Library is a repository of hardware product names and all additional information such as hardware product lifecycle dates and model numbers. This information is stored in different tables in the Content Library.

The Content library portal application is available in the ServiceNow Store. After you install the application, verify that the AI Search \(com.glide.ais\) plugin is activated. For more information about installing Content library portal application, see [Install Content lookup to view Hardware Asset Management data](content-lookup-ham.md#).

The Content lookup portal enables you to do the following:

-   Search for hardware products, manufacturers, lifecycles, or model numbers.
-   View the entire list of hardware products, manufacturers, lifecycles, and model numbers in the Content Service.
-   View additional details related to hardware products such as model numbers, and life cycle phases of hardware models.
-   View the cumulative days remaining for the next content update.

Access the Content lookup portal by navigating to **Hardware Asset Workspace** &gt; **Content lookup**.

**Note:** After installing the Content library portal application, when you access Content lookup portal for the first time, the charts aren’t populated on the page due to the absence of historical data. To load the charts, execute the Historical Data Collection jobs. For details, see the [Historical Data Collection job](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2229665) article in the Now Support Knowledge Base.

![Hardware content lookup portal displaying product names and model numbers.](../image/hw-content-lookup.png "Content lookup portal for Hardware Asset Management")

On the Content lookup portal, you can view the information based on the applications that are installed.

-   If only the Hardware Asset Management application is installed and you have the asset role, you can view the following tabs showing the data stored in the Hardware Asset Management Content Service:
    -   Hardware Overview
    -   Hardware Manufacturers
    -   Hardware Products
    -   Hardware Models
    -   Hardware Lifecycles
-   If both Software Asset Management Professional and Hardware Asset Management applications are installed and you have both asset and sam\_user roles, you can view both hardware and software content tabs. For more information about the Software Asset Management Content library portal, see the [Content lookup portal for Software Asset Management](../../software-asset-management2/concept/content-search-portal.md).

The Content lookup portal uses the AI search functionality and helps you to search for a specific hardware manufacturer, product, and model number. After you enter your search criteria in the search bar, the search results are listed with the most relevant matches at the top. Using the Filters section, you can further narrow down the result.

Based on your search criteria, the information in the Content Service is pulled from the following tables.

-   Hardware Product \[sn\_hamp\_hw\_product\]
-   Hardware Model Libraries \[sn\_hamp\_hw\_product\_model\]
-   Hardware Manufacturer \[sn\_hamp\_hw\_manufacturer\]
-   Hardware Lifecycle Definition \[sn\_hamp\_lifecycle\_definition\]

Select the search result that matches your criteria to display the details of the content record and related lists. The content record page opens in read-only mode.

## Hardware Overview tab

The **Hardware Overview** tab is by default displayed when you navigate to the Content library portal. View the following hardware widgets on this page:

<table id="table_nj1_k3b_kfc"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hardware Manufacturers

</td><td>

Hardware Manufacturers \[sn\_hamp\_hw\_manufacturer\]

</td><td>

Total number of hardware manufacturers stored in the Content Library.Select the number of manufacturers to view the list of manufacturers. By default, all active records are populated on the list.

</td></tr><tr><td>

Hardware Products

</td><td>

Hardware Products \[sn\_hamp\_hw\_product\]

</td><td>

Total number of hardware products stored in the Content Library.Select the number of products to view the list of Hardware products. By default, all active records are populated on the list.

</td></tr><tr><td>

Hardware Models

</td><td>

Hardware Model Libraries \[sn\_hamp\_hw\_product\_model\]

</td><td>

Total number of hardware models stored in the Content Library.Select the number of models to view the list of Hardware models. By default, all active records are populated on the list.

</td></tr><tr><td>

Hardware Lifecycles

</td><td>

Hardware Lifecycle Deﬁnitions \[sn\_hamp\_lifecycle\_definition\]

</td><td>

Total number of life cycle records of hardware models stored in the Content Library.Select the count of lifecycles to view the list of hardware model lifecycle phases. By default, all active records are populated on the list.

</td></tr><tr><td>

Hardware overview by content version

</td><td>

-   Hardware Products \[sn\_hamp\_hw\_product\]
-   Hardware Model Libraries \[sn\_hamp\_hw\_product\_model\]
-   Hardware Manufacturers \[sn\_hamp\_hw\_manufacturer\]
-   Hardware Lifecycle Deﬁnitions \[sn\_hamp\_lifecycle\_definition\]

</td><td>

Graphical representation of count of the hardware content released across various content versions. The information is grouped by the content version.Select a specific bar on the chart to view the detailed list of the hardware content. You can view the hardware content released in that particular content version on the list page.

</td></tr><tr><td>

Cumulative Trend for Hardware Content

</td><td>

-   Hardware Products \[sn\_hamp\_hw\_product\]
-   Hardware Model Libraries \[sn\_hamp\_hw\_product\_model\]
-   Hardware Manufacturers \[sn\_hamp\_hw\_manufacturer\]
-   Hardware Lifecycle Deﬁnitions \[sn\_hamp\_lifecycle\_definition\]

</td><td>

Graphical representation of cumulative trend of hardware content released every month.Cumulative trend chart for the following hardware content is displayed:

-   Hardware Manufacturers
-   Hardware Products
-   Hardware Models
-   Hardware Lifecycles

Select a speciﬁc point on the trend line to view a detailed list of the hardware content. On the list page, you can view the cumulative software content released for that particular content until the 1st of that month. For example, you selected the July 2025 trend point on the Hardware Products chart. The Hardware Products list table displays hardware products released until 1st July 2025.

</td></tr></tbody>
</table>## Hardware Manufacturers tab

View a list of hardware manufacturers released in the Content Library. On the Hardware manufacturers list, only active manufacturers are displayed with a default filter condition applied. Select the manufacturer's name to view the manufacturer details.

## Hardware Products tab

View a list of hardware products released in the Content Library. On the Hardware products list, only active products are displayed with a default filter condition applied. Select the product's name to view the product details.

## Hardware Models tab

View a list of hardware models released in the Content Library. On the Hardware models list, only active models are displayed with a default filter condition applied. Select the Model number to view the model details.

On the Hardware Model form, the **Copy model details** option enables you to copy the details of a model and add a model entry to the Product Model \[cmdb\_model\] table. For more information about copying model details, see [Copy a hardware model from the Content lookup portal](../task/copy-hardware-model.md).

## Hardware Lifecycles tab

View a list of life cycle records of hardware models released in the Content Library. On the Hardware lifecycles list, only active lifecycles are displayed with a default filter condition applied. Select the Product model to view the hardware product lifecycle details.

## Install Content lookup to view Hardware Asset Management data

Install the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application to view the data stored in the Hardware Asset Management Content Service.

### Before you begin

-   Install Hardware Asset Management Professional \(com.sn\_hamp\) from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Activate the AI Search \(com.glide.ais\) plugin.

Role required: asset

### About this task

If you have installed the Software Asset Management Professional \(com.sn\_samp\_master\) plugin, you can view data stored in the Software Asset Management Content service. If you have installed both Software Asset Management Professional \(com.sn\_samp\_master\) and Hardware Asset Management \(com.sn\_hamp\) plugins, you can view both their content data on the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application. You can also filter your search results based on the content type, such as software or hardware. For more information about installing the Content lookup portal for Software Asset Management, see [Install Content lookup portal for Software Asset Management](../../software-asset-management2/task/install-contentlookup.md).

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application using the filter criteria, search bar, and product tabs.

    You can search for the application by its name or ID. If you can’t find the application, request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

4.  Select **Install**.


