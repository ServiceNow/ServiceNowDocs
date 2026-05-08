---
title: Page navigation in Service Portal by URL
description: You can navigate to a portal or a page in Service Portal using a URL.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Understanding Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Page navigation in Service Portal by URL

You can navigate to a portal or a page in Service Portal using a URL.

Service Portal URLs have the following structure:

```
https://<instance>/<portal suffix>/<guest language>/<keywords>?id=<page id>&lang=<language>&<page parameters>
```

<table id="table_sbr_fnd_r1b"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

instance

</td><td>

Unique, secure web address for each instance. The default format is `https://<instance name>.service-now.com`.

</td></tr><tr><td>

portal suffix

</td><td>

Suffix established for the portal. For example, `/sp`.

</td></tr><tr><td>

guest language

</td><td>

The language ID of the portal language. For example, `es` for Spanish. The page returns in the language specified if the language is active and the user accessing the page is a guest user.

</td></tr><tr><td>

keywords

</td><td>

Human readable keywords that improve search engine optimization \(SEO\) and click-through rates for public pages. Human readable URLs also help users understand what to expect on a page for public and non-public pages. For example, `https://<instance>/kb/en/faq/what-is-a-cookie?id=kb_article_view&sysparm_article=KB0000007`.

 For more information, see [Add human readable keywords to page URLs](../task/add-human-readable-keywords-page-urls.md).

</td></tr><tr><td>

id

</td><td>

The ID of the page to navigate to within the portal frame. For example, `?id=index`.

</td></tr><tr><td>

language

</td><td>

The language ID of the portal language. For example, `lang=es` for Spanish. The page returns in the language requested if the language is active and the user accessing the page is a guest user or an authenticated user without a language preference set.

</td></tr><tr><td>

page parameters

</td><td>

Additional parameters are required by some pages to load dynamic content by looking up a record \(table, sys\_id\). Find the `$sp.getParameter` calls in a widget server script to see the parameters that a widget uses. For more detail on this method, see [GlideSPScriptable - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSPScriptableScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 If you don’t include these additional parameters when required, you might get a `You are either not authorized or record is not valid` error message.

</td></tr></tbody>
</table>For example, the URL for a public knowledge base page in Spanish in Service Portal could be `https://<instance>/sp/es/faq/what-is-a-cookie?id=kb_article&sys_id=KB0000007`.

**Note:** If you use article versioning with the Knowledge Management - Service Portal \(com.snc.knowledge\_serviceportal\) plugin, you must add the article version number to the URL to open a knowledge article in the base system or knowledge portals. For example, instead of accessing an article using the URL `https://<instance>/sp?id=kb_article&sys_id=KB0000005`, you must include the article version number: `https://<instance>/sp?id=kb_article&sys_id=KB0000005%20V1.0`. To learn more, see [Article versioning](https://www.servicenow.com/docs/access?context=article-versioning&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Referencing a page ID

Widgets and widget instance options reference Service Portal pages using the page ID. For example, a link to the sc\_home page within a widget HTML template might appear as follows:

```
<div><a href="?id=sc_home">${Order something...}</a></div>
```

**Parent Topic:**[Understanding Service Portal](sp-what-to-know.md)

**Related topics**  


[Add human readable keywords to page URLs](../task/add-human-readable-keywords-page-urls.md)

