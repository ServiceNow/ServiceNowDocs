---
title: Add human readable keywords to page URLs
description: Add human readable keywords to the URLs of portal pages to improve search engine optimization \(SEO\) and click-through rates and help users understand what to expect on the page.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Add human readable keywords to page URLs

Add human readable keywords to the URLs of portal pages to improve search engine optimization \(SEO\) and click-through rates and help users understand what to expect on the page.

## Before you begin

Role required: sp\_admin or admin

## About this task

Human readable keywords are added to URLs in the following format:

`https://<instance>/<portal suffix>/<guest language>/<keywords>?id=<page id>&<page parameters>`

Keywords can be populated using static content or dynamic page variables and can include a single slash \(/\). Dynamic page variables load keywords that are based on data in a record. The page parameters in the URL specify which record to use. In the following examples, the category and short description of a knowledge article and the category and name of a catalog item are added as keywords:

-   `https://<instance>/kb/en/faq/what-is-a-cookie?id=kb_article_view&sysparm_article=KB0000007`
-   `https://<instance>/sp/es/hardware/developer-laptop-mac?id=sc_cat_item&sys_id=774906834fbb4200086eeed18110c737`

**Note:** To turn off human readable URLs for an instance, add the **glide.service\_portal.enable\_human\_readable\_urls** property to the System Properties \[sys\_properties\] table and set the value to `false`.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  Select a page.

3.  Use keywords that are dynamic based on the page content by adding a dynamic page variable to the page.

    1.  Select the Dynamic page variables related list tab.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|The variable that loads keywords in the page URL from record data. The variable name must begin with `%` and can’t contain spaces. For example, `%short_descr`.|
        |Order|The priority order from lowest to highest for when multiple dynamic page variables with the same name have different URL query parameters.|
        |Page|The page that uses the dynamic page variable to include keywords in the URL.|
        |URL query parameter|The parameter in the page URL that determines which record displays.|
        |Relevant table column|The column in the specified table that includes the values of the URL query parameter. The default value is **Sys ID**.|
        |Table|The table that includes the records used to populate keywords in the URL and the column with the values of the URL query parameter.|
        |Table field|A field from records in the specified table that populates the keywords in the URL.|
        |Query condition|Conditions that filter the records in the table. A record must meet the query conditions for the variable to apply.|

        This example shows the values for a variable that references the short description of a knowledge base article identified by its number for a published workflow.

        |Field|Value|
        |-----|-----|
        |Name|%short\_descr|
        |Page|kb\_article\_view|
        |Order|100|
        |URL query parameter|sysparm\_article|
        |Relevant table column|Number|
        |Table|Knowledge\[kb\_knowledge\]|
        |Table field|Short description|
        |Query condition|\[Workflow\]\[is\]\[Published\]|

4.  Select **Submit**.

5.  In the **Human readable url structure** field of the page record, specify the keywords to populate in the page URL using static content, dynamic page variables, or a combination.

    Keywords can include alphanumeric characters, hyphens \(‐\), one slash \(/\), and percent signs \(%\) for variables.

    |Human readable url structure|Example value|
    |----------------------------|-------------|
    |Static content|`faq/what-is-a-cookie`|
    |Dynamic page variables|`%category/%short_descr`|
    |Static content and dynamic page variable|`faq/%short_descr`|

    Keywords are automatically formatted to use only lowercase letters, replace spaces with hyphens, and remove any disallowed special characters added by dynamic page variables. If the keywords in the URL exceed 75 characters, they’re truncated to be less than or equal to 75 characters.

6.  Select **Update**.


## Result

If users access the page using the URL without human readable keywords, the page URL is updated in one of the following ways:

-   On the initial page load by a guest user, the page redirects to the human readable URL.
-   On the initial page load by an authenticated user, the URL is updated to include the human readable keywords without redirection.
-   On subsequent page loads for all users, the URL is updated to include the human readable keywords without redirection.

## Knowledge article page with human readable keywords in the URL

In this example, the kb\_article\_view page displays knowledge article KB0000007. The knowledge article record has the following fields and values:

-   **Category** is **FAQ**
-   **Short description** is `What is a cookie?`

The page has been configured to add keywords based on these field values to the URL using dynamic page variables such as `%category/%short_descr`. The question mark in the short description isn’t an allowed character in the URL keywords so it’s automatically removed from the URL. The question mark that is in the URL is the query parameter that's always included before the page ID.

The URL that is displayed in the browser appears as: `http://<instance>.com/kb/en/faq/what-is-a-cookie?id=kb_article_view&sysparm_article=KB0000007`.

## What to do next

For pages that have canonical URLs, you must include the human readable keywords in the canonical URL. In the SEO script include that returns canonical URLs for pages, use one of the getHumanReadableUrl methods in the SPSEOUtilsSNC class to return the human readable keywords in page URLs and include them in the canonical URLs.

For more information about including human readable keywords in canonical URLs, refer to the following resources:

-   Configure custom SEO tags for canonical URLs and localized knowledge articles
-   SPSEOUtilsSNC - Global

**Parent Topic:**[Improving search engine optimization for portals](../concept/seo-sp.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](t_ConfigureAPage.md#)

[Page navigation in Service Portal by URL](../concept/navigate-by-portal-url.md)

