---
title: Enable SEO for localized versions of a portal page
description: Allow users to discover portal pages in their preferred language by adding hreflang tags.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable SEO for localized versions of a portal page

Allow users to discover portal pages in their preferred language by adding **hreflang** tags.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages** and open a page record.

    Ensure that **Public** is selected for the page. Pages that are not public are not indexed by external search engines.

2.  On the form, select the **Use SEO script** check box.

    Selecting this check box causes the **SEO script** field to appear. By default, the system uses the SPSEOHeaderTags script include. You can use a different script include by updating this field.

    !["Use SEO script" and "SEO script" fields on the Page form](../image/seo-script.png)

3.  Click **Update**.


## Result

The system adds default **hreflang** tags for each active language in your instance.

## What to do next

You can override the default **hreflang** tags, add a canonical URL, or add custom header tags by updating the script include that is referenced in the **SEO script** field. This needs to be set by the page or content author.

To specify a canonical URL for the page, update the `generateCanonicalURL` function in the script include.

To specify custom header tags for the page, update the `generateCustomTagsForSEO` function in the script include.

For an example of inserting custom SEO tags into the knowledge article view page, see [Configure custom SEO tags for canonical URLs and localized knowledge articles](https://www.servicenow.com/docs/access?context=configure-seo-knowledge&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Improving search engine optimization for portals](../concept/seo-sp.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](t_ConfigureAPage.md#)

