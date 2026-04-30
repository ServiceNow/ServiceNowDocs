---
title: Configure a video authorization
description: Configure a content processor to enable employees to view private videos without providing credentials.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Video hosting integrations framework, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure a video authorization

Configure a content processor to enable employees to view private videos without providing credentials.

## Before you begin

-   Role required: sn\_cd.content\_admin and fd\_read\_flows
-   [Create a subflow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-subflow&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) with the following inputs and outputs:

    ![necessary inputs and outputs for the authorization subflow](../images/subflows-auth.png)

-   [Configure content provider and mapping](configure-content-provider.md)

## About this task

The authorize action makes authentication API calls to the video hosting service. The authorization method varies based on the provider and is determined by their supported embed iframe.

Content Publishing appends the authentication token as a query parameter along with its corresponding value to the embedded URL. The configured subflow inputs and outputs manage the query parameters and response body.

**Note:** The JSON Web Token \(JWT\) and access token authentication methods are proven to work. To use a different method, ensure you configure the subflow to return a token. The video hosting service must support auto-authentication via the token in the URL.

## Procedure

1.  If you have already opened a Content Provider, click the Content Provider Mapping **Preview record** icon then click **Open Record**.

    Navigate to **All** &gt; **Content Publishing** &gt; **Content Provider Configs** &gt; **Content Processors**.

2.  Click **New**.

    Fill in the form fields:

    |Field|Description|
    |-----|-----------|
    |Action|Select **Authorize**|
    |Provider mapping|Select the Content provider that connects Content Publishing to the video hosting service|
    |Processor subflow|Select the flow that performs the authorization API call|
    |Active|Makes this action available to employees|

3.  Click **Submit**.

    The new Content processor appears in the Content Provider related list.


## What to do next

-   Enable content managers to view thumbnails of available videos: [Configure video content search](configure-content-search.md)
-   Add interface elements to the Content Library video picker: [Configure content rendering parameter](configure-content-rendering-parameter.md)

