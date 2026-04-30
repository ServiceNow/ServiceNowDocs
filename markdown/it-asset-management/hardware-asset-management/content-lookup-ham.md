---
title: Content lookup portal for Hardware Asset Management
description: The IT Asset Management Content lookup portal gives you visibility into the data stored in the Hardware Asset Management Content Service via an intuitive user interface.Install the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application to view the data stored in the Hardware Asset Management Content Service.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Hardware Asset Workspace, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Content lookup portal for Hardware Asset Management

The IT Asset Management Content lookup portal gives you visibility into the data stored in the Hardware Asset Management Content Service via an intuitive user interface.

Once you have installed Hardware Asset Management Professional \(sn\_hamp\), the Content lookup portal enables you to do the following:

-   Search for hardware products or model numbers
-   View the entire list of hardware products and model numbers in the Content Service
-   View the cumulative days remaining for the next content update

For more information about installing Content lookup, [Install Content lookup to view Hardware Asset Management data](content-lookup-ham.md#).

![Hardware content lookup portal displaying product names and model numbers.](../image/hw-content-lookup.png "Content lookup portal for Hardware Asset Management")

After you enter your criteria in the search bar, the search results are listed with the most relevant matches at the top. Filters on the left-hand side of the page assist you in further narrowing down your results.

Based on your search criteria the information in the Content Service is pulled from the following tables.

-   Hardware product \[sn\_hamp\_hw\_product\]
-   Hardware Model Library \[sn\_hamp\_hw\_product\_model\]

Select the search result that matches your criteria to display the details of the content record and related lists. The content record page opens in read-only mode.

## Install Content lookup to view Hardware Asset Management data

Install the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application to view the data stored in the Hardware Asset Management Content Service.

### Before you begin

-   Install Hardware Asset Management Professional \(com.sn\_hamp\) from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).
-   Activate the AI Search \(com.glide.ais\) plugin.

Role required: asset

### About this task

If you have installed the Software Asset Management Professional \(com.sn\_samp\_master\) plugin, you can view data stored in the Software Asset Management Content service. If you have installed both Software Asset Management Professional \(com.sn\_samp\_master\) and Hardware Asset Management Professional \(com.sn\_hamp\) plugins, you can view both their content data on the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application. You can also filter your search results based on the content type, such as software or hardware. For more information about installing the Content lookup portal for Software Asset Management, see [Install Content lookup portal for Software Asset Management](../../software-asset-management2/task/install-contentlookup.md).

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the IT Asset Management Content lookup \(sn\_itam\_contlookup\) application using the filter criteria, search bar, and product tabs.

    You can search for the application by its name or ID. If you cannot find the application, request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

4.  Select **Install**.


