---
title: Index sites for search
description: Configure the SharePoint Online Search Connector to crawl the content from the eligible sites, subsites, drives, and more.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [SharePoint Online Search Connector, Employee Service Management]
---

# Index sites for search

Configure the SharePoint Online Search Connector to crawl the content from the eligible sites, subsites, drives, and more.

## Before you begin

-   Verify that you have a basic knowledge of Microsoft Azure and Microsoft SharePoint functionality.
-   Work with a Microsoft SharePoint administrator to understand the set of sites for indexing.
-   Activate SharePoint Online Search Connector from the ServiceNow store.

Role required: sn\_sp\_con.admin or admin

## Procedure

1.  Navigate to **SharePoint Online Search Connector** &gt; **SharePoint Connectors**.

2.  Click **New**.

    ![Options of site permission display for REST connection setup.](../image/site-permission-spoc.png "Connector details")

3.  On the form, fill in the fields.

<table id="table_ykv_cfz_f2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Graph connection

</td><td>

Connection for graph. Use the graph tenant record.

</td></tr><tr><td>

REST connection

</td><td>

Connection for REST. Use the Rest tenant record.

</td></tr><tr><td>

Site URL Path

</td><td>

Value of the relative URL of the Microsoft SharePoint site for indexing. For example, if your site URL is [https://sncplatform.sharepoint.com/Company/Medicalbenefits](https://sncplatform.sharepoint.com/Company/Hr), the relative URL of the site is `Company/Medicalbenefits`. **Note:** This URL is case-sensitive.

Subsites are automatically indexed. See [SharePoint Online Search Connector search results](../reference/using-search.md).

</td></tr><tr><td>

State

</td><td>

State of the indexing.

</td></tr><tr><td>

REST Site Permission

</td><td>

Use one of the following site permissions to manage access to the SharePoint.-   **Sites.FullControl.All**: Provides the full control to SharePoint sites for the signed-in user. Sites, subsites, files, and user groups are indexed with this option.
-   **Sites.Read.All**: Provides only the read access to the files for the signed-in user. This option is the default value. Only files and user groups are indexed with this option.
-   **Sites.Selected**: Provides selected site control with selected roles to users. Only files and user groups are indexed with this option.


</td></tr><tr><td>

Site role

</td><td>

Use one of the following options to manage access control.-   **Full control**
-   **Read**
-   **Write**

This field appears only when **Sites.Selected** is selected from **REST Site Permission**.

</td></tr><tr><td>

Exclude Subsites

</td><td>

List of URLs that are excluded from indexing. These URLs are not indexed by the AI Search and are not displayed in the search results. You can add multiple sites with **\|** as a separator. Enter the URLs of any subsites you don't want to index.

**Note:** Ensure you specify the complete URLs and not relative URLs.

</td></tr></tbody>
</table>4.  Click **Submit &amp; Index** to validate and start indexing the site.

    When you submit the site, the indexing includes the related subsites.

5.  Track the indexing progress from the **Search connector** record state.

6.  Proceed to see the **Indexed Sites** related list.

    The indexed site list contains the following information:

    |Field|Description|
    |-----|-----------|
    |Name|Subsite name.|
    |Display name|Subsite display name.|
    |Web URL|Web URL of the Microsoft SharePoint site.|
    |Description|Description of the subsite.|
    |Subsites fetch state|Status of the subsite crawl, such as, **Pending** and **Complete**.|
    |Drives fetch state|Status of the drives crawl, such as, **In progress** and **Complete**.|
    |State|Overall crawl status.|
    |Marked for deletion|Value is **False** to keep the subsite. Value is **True** to delete the subsite.|

    To know more about how to exclude sites, see [Exclude sites from indexing](../task/how-to-exclude-sites-indexing.md).


## Result

The sites, subsites, folders, and files are indexed and displayed in your search results. Use filters to verify the progress and manage the indexing status by navigating to **SharePoint Online Search Connector** &gt; **SharePoint Sites**.

After site indexing is complete, you can search and discover the site content from multiple channels, like Employee Service Center, Service Portal, Now Mobile app, and Virtual Agent. For more information, see [SharePoint Online Search Connector search results](../reference/using-search.md).

## What to do next

**Remove Index**: Select the indexed site and click Remove Index to remove the site from indexing. On success, all the sites, drivers, and files are removed from the respective tables and the connector is updated to read only with the Deleted status.

