---
title: Retire a versioned article
description: You can retire the latest published version of a knowledge article. Retiring a knowledge article doesn’t create a version. It simply marks the article as Retired.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use article versioning, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Retire a versioned article

You can retire the latest published version of a knowledge article. Retiring a knowledge article doesn’t create a version. It simply marks the article as **Retired**.

## Before you begin

Role required: knowledge administrator, knowledge manager, and latest publisher of the versioned knowledge article \(not available for kcs\_candidate or kcs\_contributor\)

## About this task

You can only retire an article, which has no checked out version. If a version has been checked out, the **Retire** button doesn’t appear on the Knowledge form header.

**Note:** For the Knowledge - Approval Retire workflow, this happens only when the retire request is approved.

You can still access outdated articles that have been attached to incidents by navigating to the article view page with the sys\_id of the article. Outdated articles include a message that an updated article is available.

If versioning is disabled, only the latest version of the article is shown in search results and list views.

Retired knowledge articles can’t be searched by external users or customers. To reuse a retired article, create an article with the same content, which is published once approved.

Beginning with the Utah release, you can give a replacement article while retiring a knowledge article. When the retired article is accessed, you will automatically be redirected to the replacement article with a display message `The article KBxxx is retired and has been replaced with the knowledge article KBxxx`. If no replacement article is available, the page displays the message `Knowledge record not found`.

-   Article with replacement returns a 301 code.
-   Article without any replacement returns a 404 code.
-   By default, the **glide.knowman.enable\_article\_replacement\_on\_retire** system property is set to true to give a replacement article for a retired article. The setup to redirect an article to a replacement article is set by default.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **Published**.

2.  Select an article.

3.  Click **Retire** in the Knowledge form header.

    The system returns to the Knowledge list. The state of the article changes to **Pending retirement** and the state of previously published versions change to **Outdated**.

    **Note:** You can’t check out or edit a retired article.


## Result

The selected article is retired and can be accessed from **Knowledge** &gt; **Articles** &gt; **Retired**

**Parent Topic:**[Use article versioning](../../../use-article-versioning_0.md)

