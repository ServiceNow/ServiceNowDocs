---
title: Content lookup portal for Software Asset Management
description: The Content lookup portal gives you visibility into the data stored in the Content Library as part of the IT Asset Management Content Service via an intuitive user interface.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Content lookup portal for Software Asset Management

The Content lookup portal gives you visibility into the data stored in the Content Library as part of the IT Asset Management Content Service via an intuitive user interface.

The Content Library is a repository of software product names and all additional information such as software product lifecycle dates, discovery maps, and publisher part numbers \(PPNs\). This information is stored in different tables in the Content Library. For more details on the Content Service, see [Software Asset Management Content Service](c_SAMContentService.md).

The Content library portal application is available in the ServiceNow Store. After you install the application, verify that the AI Search \(com.glide.ais\) plugin is activated. For details on installing the Content library portal application, see [Install Content library portal for Software Asset Management](../task/install-contentlookup.md).

The Content lookup portal enables you to do the following:

-   Search for a speciﬁc software publisher, product, Discovery Map, life cycle, and PPN.
-   View the entire list of software publishers, products, lifecycles, PPNs, and Discovery Maps in the Content Service.
-   View additional details related to software products such as software version, and software product life cycles.
-   View the days remaining for the next content update.

Access the Content lookup portal by navigating to **Software Asset Workspace** &gt; **Content lookup**.

**Note:** After installing the Content library portal application, when you access Content lookup portal for the first time, the charts aren’t populated on the page due to the absence of historical data. To load the charts, execute the Historical Data Collection jobs. For details, see the [Historical Data Collection job](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2229665) article in the Now Support Knowledge Base.

![Software Content library portal displaying software content information](../image/contentlookup.png "Content lookup portal for Software Asset Management")

On the Content lookup portal, you can view the information based on the applications that are installed.

-   If only the Software Asset Management Professional application is installed and you have the sam\_user role, you can view the following tabs showing the data stored in the Software Asset Management Content Service:
    -   Software Overview
    -   Software Publishers
    -   Software Products
    -   Software DMAPs
    -   Software Lifecycles
    -   Software PPNs
-   If both Software Asset Management Professional and Hardware Asset Management applications are installed and you have both sam\_user and asset roles, you can view both software and hardware content tabs. For more information about the Hardware Asset Management Content lookup portal, see the [Content lookup portal for Hardware Asset Management](../../hardware-asset-management/concept/content-lookup-ham.md#).

The Content lookup portal uses the AI search functionality and helps you to search for a specific software publisher, product, Discovery Maps, life cycles, and PPNs.

After you enter your search criteria in the search bar, the search results are listed with the most relevant matches at the top. Using the Filters section, you narrow down the result further.

Based on your search criteria, the information in the Content Service is pulled from multiple tables, such as:

-   Software Products \[samp\_sw\_product\]
-   Discovery Maps \[samp\_sw\_entitlement\_definition\]
-   Software Product Definitions \[samp\_sw\_product\_definition\]
-   Software Publishers \[samp\_sw\_publisher\]
-   Software Product Lifecycles \[sam\_sw\_product\_lifecycle\]

Select the search result that matches your criteria to display the details page along with the related lists. The details page opens in read-only mode. For example, if you select the Microsoft SQL Server 2008 Enterprise product result, the Microsoft SQL Server 2008 Enterprise page appears with the related lists such as software version, software life cycle data, and PPN.

## Software Overview tab

The **Software Overview** tab is by default displayed when you navigate to the Content library portal. View the following software widgets on this page.

<table id="table_vhj_f1v_jfc"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Publishers

</td><td>

Software Publishers \[samp\_sw\_publisher\]

</td><td>

Total number of software publishers stored in the Content Library.Select the number of publishers to view the list of Software publishers. By default, all active records are populated on the list.

</td></tr><tr><td>

Software Products

</td><td>

Software Products \[samp\_sw\_product\]

</td><td>

Total number of software products stored in the Content Library.Select the number of products to view the list of Software products. By default, all active records are populated on the list.

</td></tr><tr><td>

Software DMAPs

</td><td>

Discovery Maps \[samp\_sw\_entitlement\_definition\]

</td><td>

Total number of software discovery maps stored in the Content Library.Select the number of DMAPs to view the list of Software DMAPs. By default, all active records are populated on the list.

</td></tr><tr><td>

Software Lifecycles

</td><td>

Software Product Lifecycles \[sam\_sw\_product\_lifecycle\]

</td><td>

Total number of life cycle records of software products stored in the Content Library.Select the number of lifecycles to view the list of software product lifecycles. By default, all active records are populated on the list.

</td></tr><tr><td>

Software PPN

</td><td>

Software Product Definitions \[samp\_sw\_product\_definition\]

</td><td>

Total number of the software publisher part numbers stored in the Content Library.Select the number of PPNs to view the list of Software PPNs. By default, all active records are populated on the list.

</td></tr><tr><td>

Software overview by content version

</td><td>

-   Software Publishers \[samp\_sw\_publisher\]
-   Software Products \[samp\_sw\_product\]
-   Discovery Maps \[samp\_sw\_entitlement\_definition\]
-   Software Product Lifecycles \[sam\_sw\_product\_lifecycle\]
-   Software Product Definitions \[samp\_sw\_product\_definition\]

</td><td>

Graphical representation of the count of the software content released across various content versions. The information is grouped by the content version.Select a specific bar on the chart to view the detailed list of the software content. You can view the software content released in that particular content version on the list page.

</td></tr><tr><td>

Cumulative Trend for Software Content

</td><td>

-   Software Publishers \[samp\_sw\_publisher\]
-   Software Products \[samp\_sw\_product\]
-   Discovery Maps \[samp\_sw\_entitlement\_definition\]
-   Software Product Lifecycles \[sam\_sw\_product\_lifecycle\]
-   Software Product Definitions \[samp\_sw\_product\_definition\]

</td><td>

Graphical representation of cumulative trend of software content released every month.Cumulative trend chart for the following software content is displayed:

-   Software Publishers
-   Software Products
-   Software DMAPs
-   Software Lifecycles
-   Software PPNs

Select a speciﬁc point on the trend line to view a detailed list of the software content. On the list page, you can view the cumulative software content released for that particular content until the 1st of that month. For example, you selected the July 2025 trend point on the Software Products chart. The Software Products list table displays software products released till 1st July 2025.

</td></tr></tbody>
</table>## Software Publishers tab

View a list of software publishers released in the Content Library. On the Software publishers list, only active publishers are displayed with a default filter condition applied. Select the publisher's name to view the publisher's details.

## Software Products tab

View a list of software products released in the Content Library. On the Software products list, only active products are displayed with a default filter condition applied. Select the product name to view the product details.

## Software DMAPs tab

View a list of software discovery MAPs released in the Content Library. On the Software DMAPs list, only active DMAPs are displayed with a default filter condition applied. Select the DMAP number to view the details.

## Software Lifecycles tab

View a list of life cycle records of software products released in the Content Library. On the Software lifecycles list, only active lifecycles are displayed with a default filter condition applied. Select the version to view the software product lifecycle details.

## Software PPNs tab

View a list of software publisher part numbers released in the Content Library. On the Software PPNs list, only active PPNs are displayed with a default filter condition applied. Select the publisher's part number to view the software part number details.

