---
title: Configure video content search
description: Configure a content processor to add a button to the Content Library interface that enables a content manager to view thumbnails of available videos from the content provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/configure-content-search.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Video hosting integrations framework, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure video content search

Configure a content processor to add a button to the Content Library interface that enables a content manager to view thumbnails of available videos from the content provider.

## Before you begin

-   Role required: sn\_cd.content\_admin and fd\_read\_flows
-    with the following inputs and outputs:

    \[Omitted image "subflow-search.png"\] Alt text: necessary inputs and outputs for the search subflow

-   [Configure content provider and mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/configure-content-provider.md)

## Procedure

1.  If you have already opened a Content Provider, click the Content Provider Mapping **Preview record** icon then click **Open Record**.

    Navigate to **All** &gt; **Content Publishing** &gt; **Content Provider Configs** &gt; **Content Processors**.

2.  Click **New**.

    Fill in the form fields:

    | | |
    |---|---|
    |Action|Select **Search**|
    |Provider mapping|Select the Content provider that connects Content Publishing to the video hosting service|
    |Processor subflow|Select the flow that performs the search API call|
    |Active|Makes this action available to content managers|

3.  Click **Save**.

    The new Content processor appears in the Content Provider related list.


## What to do next

-   Enable employees to view private videos without providing credentials: [Configure a video authorization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/configure-content-processor.md)
-   Add interface elements to the Content Library video picker: [Configure content rendering parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/configure-content-rendering-parameter.md)

