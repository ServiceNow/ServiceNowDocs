---
title: Usage Insights release notes
description: The ServiceNow Usage Insights application, formerly known as User Experience Analytics, enables you to monitor how users interact with your ServiceNow Core UI, Next Experience, Mobile, and Service Portal applications so product managers and applicationners can gain insight into application usage and adoption. Usage Insights was enhanced and updated in the Australia release.The ServiceNow Usage Insights applications, enables you to monitor how users interact with the Core UI, Next Experience, Mobile, and Service Portal applications so product managers and applicationners can gain insight into application usage and adoption. Usage Insights was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Usage Insights release notes

The ServiceNow® Usage Insights application, formerly known as User Experience Analytics, enables you to monitor how users interact with your ServiceNow Core UI, Next Experience, Mobile, and Service Portal applications so product managers and applicationners can gain insight into application usage and adoption. Usage Insights was enhanced and updated in the Australia release.

## About Usage Insights

-   User Experience Analytics is now known as Usage Insights.
-   Usage Insight Data Export is delivered as a store app that adds a REST API endpoint to your instance and provisions a dedicated messaging topic for result delivery.
-   Tag and create events and update event descriptions.
-   View funnels you create in Usage Insights directly in Platform Analytics.
-   Create dashboards for Platform Analytics directly in Usage Insights.

See [Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/user-exp-analytics-landing.md) for more information.

## Activation and other requirements

**Important:** Usage Insights is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Usage Insights is a ServiceNow AI Platform feature that is active by default.


**Parent Topic:**[Platform Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/analytics-intel-report-rn-landing.md)

## Australia

The ServiceNow® Usage Insights applications, enables you to monitor how users interact with the Core UI, Next Experience, Mobile, and Service Portal applications so product managers and applicationners can gain insight into application usage and adoption. Usage Insights was enhanced and updated in the Australia release.

### What's new

-   **[Conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/conversations.md)**

    Explore the conversations view by ServiceNow Otto chat activity. It reports engagement metrics such as total chat users and live agent transfers, chat-related events, from starting a conversation to rendering a chat response to selecting a chat action.

-   **[Create cross-application conversion funnels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-conversion-funnel-for-cross-application.md)**

    Create and use cross-application conversion funnels to target all applications or one specific application, so that consecutive steps can follow from one application into another.

-   **[Page properties analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/page-properties-analytics.md)**

    Filter a page detail page by one or more page properties to analyse how usage differs across page attributes such as owner, category, or load time.

-   **[Bulk export of Usage Insights data via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/data-export-restapi.md)**

    Use Usage Insights data export store app to deliver an asynchronous REST API endpoint that processes export requests in the background and streams results as JSON batches to a dedicated Kafka topic. Unlike manual export from the Usage Insights dashboard, data export is designed for programmatic, large-volume, recurring data movement scenarios.

-   **[Creating custom events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/tagged-events.md)**

    Create custom events without code directly in your application using the Usage Insights page overlay. Use event descriptions to provide greater visibility and clarity on Usage Insights events.

-   **[Access Funnels from Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-funnel.md)**

    Access funnels you create in Usage Insights directly in the Platform Analytics UI to view this data along with your organization's other business metrics.

-   **[Customize Dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/uxa-dashboards.md)**

    Customize dashboards or pages for Platform Analytics directly in Usage Insights.


### What's deprecated or removed

-   **[Usage Insights in Xanadu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/user-exp-analytics-landing.md)**

    Usage Insights is no longer supported in the Xanadu release. Upgrade to Yokohama, Zurich, or Australia to continue using Usage Insights.


