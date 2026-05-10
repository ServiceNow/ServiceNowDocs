---
title: Generate search results using Q&amp;A Genius Results in Now Assist for Legal Service Delivery \(LSD\)
description: Generate actionable search results from knowledge article results in Legal Counsel Center, Employee Center, and global search by using Q&amp;A Genius Results in Now Assist for Legal Service Delivery \(LSD\).
locale: en-US
release: australia
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Use, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Generate search results using Q&amp;A Genius Results in Now Assist for Legal Service Delivery \(LSD\)

Generate actionable search results from knowledge article results in Legal Counsel Center, Employee Center, and global search by using Q&amp;A Genius Results in Now Assist for Legal Service Delivery \(LSD\).

## Before you begin

For Legal Counsel Center, Q&amp;A Genius Results is activated by default when you install and activate AI Search and Legal Service Delivery - Prime plugin \(sn\_lg\_ai\_prime\).

For global search and Employee Center, you must enable Q&amp;A Genius Results manually. For more information, see [Enabling Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/enabling-now-assist-qa-grs.md) and [Enable Now Assist genius results](../../employee-center/task/na-qa-activate.md).

Ensure you have configured the Q&amp;A Genius skill. For more information, see [Configuring Q&amp;A Genius Results in Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-cofig-gen-results.md).

For more information on the other supported search engines, see [Search in Legal Service Delivery](../concept/lsd-search-overview.md).

Role required:

-   sn\_lg\_ops.legal\_fulfiller for Legal Counsel Center
-   sn\_lg\_ops.legal\_user for Employee Center
-   No specific role is required to access global search.

## Procedure

1.  Navigate to the workspace through either the Legal Counsel Center, Employee Center, or Global Search.

    |Option|Description|
    |------|-----------|
    |**Legal Counsel Center with the sn\_lg\_ops.legal\_fulfiller role**|Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.|
    |**Employee Center with the sn\_lg\_ops.legal\_user role**|Navigate to **All** &gt; **Employee Center**|
    |**Global search**|Navigate to landing page of a ServiceNow instance.|

2.  In the **Search** field, enter your query.


## Result

With your search results, you also see an answer card with a topic snippet and an answer snippet extracted from a single knowledge article. You can view the full article directly from the answer card.

![Q&A Genius Results in Legal Counsel Center.](../image/lsd-na-genius-result.png)

**Parent Topic:**[Using Now Assist for Legal Service Delivery \(LSD\)](../concept/now-assist-lsd-using.md)

