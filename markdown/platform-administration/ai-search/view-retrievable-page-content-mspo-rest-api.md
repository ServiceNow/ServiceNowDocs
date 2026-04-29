---
title: View retrievable page content using the Microsoft SharePoint Online REST API
description: Review the elements of of a Microsoft SharePoint Online page's content that can be retrieved by the Microsoft SharePoint Online external content connector.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Microsoft SharePoint Online external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# View retrievable page content using the Microsoft SharePoint Online REST API

Review the elements of of a Microsoft SharePoint Online page's content that can be retrieved by the Microsoft SharePoint Online external content connector.

## Before you begin

You need the following details about each Microsoft SharePoint Online page that you want to view retrievable content for:

-   Your site URL. This is typically in the format `https://<tenant-name>.sharepoint.com/sites/<site-name>`, where `<tenant-name>` is the hostname for your tenant and `<site-name>` is the name of the site in which the page resides. As an example, your site URL might be `https://example.sharepoint.com/sites/my-site`.
-   The `.aspx` page's filename, without the extension. As an example, if the URL for your page is `https://example.sharepoint.com/sites/my-site/SitePages/sample-page.aspx`, the page's filename is `sample-age`.

    **Note:** Microsoft SharePoint Online page filenames are case-sensitive, so copy the filename exactly as it appears in the URL field of your web browser.


Role required: none

## About this task

Perform this procedure to review the contents of a Microsoft SharePoint Online page's CanvasContent1 and WikiFields metadata fields. These fields contain the static content that the connector retrieves and makes searchable in your AI Search applications.

Microsoft SharePoint Online pages are stored as `.aspx` files in a site's Site Pages library. These files include static content in their CanvasContent1 and WikiFields metadata fields, but they also include scripts that call a server-side engine to dynamically render viewable content at request time. The exact content rendered depends on user context, permissions, and web parts loaded as part of the page request.

Rendering a page's full viewable content requires an authenticated user session. The Microsoft SharePoint Online connector can't impersonate a user to trigger this rendering process. As a result, the connector cannot capture the final HTML output that a web browser would display.

For each page retrieved, the Microsoft SharePoint Online connector queries the SharePoint REST API to access the page's underlying list item. The API endpoint used is `_api/web/lists('<list-id>')/items(<item-id>)`, where `<list-id>` and `<item-id>` are dynamically substituted values. The connector retrieves content primarily from the page's CanvasContent1 and WikiFields metadata fields, and also captures the page's other metadata fields such as title, author, and modification date where available. Page content stored exclusively in dynamic web parts may be retrieved only partially or not at all, since that content doesn't exist in the list item metadata.

The upshot of this limitation is that pages built primarily with static text content authored in the Microsoft SharePoint Online editor produce searchable content that more closely matches what users see in a web browser. By contrast, pages that rely on dynamic web parts may not contain all of the content that users see in a web browser.

## Procedure

1.  Retrieve the ID for your site's Site Pages list.

    1.  In a web browser, navigate to your Microsoft SharePoint Online tenant and log in.

    2.  In the browser, navigate to `<site-url>/_api/web/lists?$select=ID,Title&$filter=Title%20eq%20%27Site%20Pages%27`, replacing `<site-url>` with your Microsoft SharePoint Online site URL.

        If this request does not return an XML response describing the Site Pages list, navigate to `<site-url>/_api/web/lists?$select=ID,Title` instead, then find the entry for the Site Pages list in the unfiltered response.

    3.  In the XML response, locate the `<d:Id>` element and copy the list GUID given as its value.

        As an example, the list GUID might be `4acc128d-166d-441d-a7a6-d96ae2e8b46f`.

2.  View static content for your selected page.

    1.  In your web browser, navigate to `<site-url>/_api/web/lists('<list-id>')/items?$filter=FileLeafRef%20eq%20%27<filename>.aspx%27`, replacing `<site-url>` with your site URL, `<list-id>` with the GUID that you copied in step [1.c](view-retrievable-page-content-mspo-rest-api.md#copy-list-guid-step), and `<filename>` with the filename of the page you want to view searchable content for.

    2.  In the XML response, locate the CanvasContent1 and WikiField metadata fields and examine their values.

        These fields contain the static content that the Microsoft SharePoint Online connector makes searchable when the page is retrieved.

        **Note:** If the CanvasContent1 and WikiField metadata fields are missing or empty, the page is likely rendered entirely via dynamic web parts and does not contain static content that can be retrieved by the Microsoft SharePoint Online external content connector.


**Parent Topic:**[Microsoft SharePoint Online external content connector](../concept/microsoft-sharepoint-online-external-content-connector.md)

