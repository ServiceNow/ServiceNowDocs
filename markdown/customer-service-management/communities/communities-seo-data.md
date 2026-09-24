---
title: Community pages that support SEO data
description: To improve search results for community members using external search engines, the Communities application generates SEO meta tags and injects the tags into questions, topics, forums, and other page types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/communities-seo-data.html
release: brazil
product: Communities
classification: communities
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Community Service Portal, Configuring communities, Communities, Customer Service Management]
---

# Community pages that support SEO data

To improve search results for community members using external search engines, the Communities application generates SEO meta tags and injects the tags into questions, topics, forums, and other page types.

**Important:**

Starting with the Brazil release, Communities is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

**Note:** If the auto-generated SEO tags in a page does not meet your needs, you can change the SEO tags. See [Modify SEO in community pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/seo-communities-modify.md).

## Pages that include auto-generated SEO data

The Communities application auto-generates SEO meta tags for the following pages in the Community service portal. The table provides details on the data that is generated.

-   community\_question
-   community\_blog
-   community\_document
-   community\_video
-   community\_event
-   community\_forum
-   community\_topic

<table id="table_otj_2qj_hbb"><thead><tr><th>

Searchable page type

</th><th>

Auto-generated tags in the page

</th></tr></thead><tbody><tr><td>

Question, Blog, Document, Video, and Event

</td><td>

-   The **title** meta tag is populated with the text “&lt;forum name&gt; - &lt;content short description&gt;"
-   The **description** meta tag is populated with the text “&lt;forum name&gt; - &lt;topic names&gt; - &lt;first 100 characters of the body of the content&gt;"

</td></tr><tr><td>

Forum

</td><td>

-   The **title** meta tag is populated with the text “&lt;forum name&gt;"
-   The **description** meta tag is populated with the text “&lt;forum description&gt;"

</td></tr><tr><td>

Topic

</td><td>

-   The **title** meta tag is populated with the text “&lt;topic name&gt;“
-   The **description** meta tag is populated with the text “&lt;topic description&gt;"

</td></tr><tr><td>

Leaderboard page

</td><td>

The Title meta tag is populated with the text “&lt;community name&gt;”

</td></tr></tbody>
</table>-   **[Modify SEO in community pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/seo-communities-modify.md)**  
If an auto-generated SEO meta tag does not meet your needs, you can modify or replace the tag.

**Parent Topic:**[Community Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/community-service-portal.md)

