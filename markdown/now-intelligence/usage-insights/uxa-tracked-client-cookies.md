---
title: Usage Insights client-side storage cookies
description: To track client-side user activity, Usage Insights uses the SNAnalytics JavaScript SDK that is embedded in Platform Analytics, Core UI, and the Service Portal.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Tracked analytics fields and cookies, User privacy, tracking, and consent, Configuring Usage Insights, Usage Insights, Platform Analytics]
---

# Usage Insights client-side storage cookies

To track client-side user activity, Usage Insights uses the SNAnalytics JavaScript SDK that is embedded in Platform Analytics, Core UI, and the Service Portal.

The SNAnalytics SDK uses a combination of session storage and local storage variables to track the information required to facilitate the analytics tracking.

For more information on session storage and local storage, refer to the [JavaScript.Info](https://javascript.info/localstorage) documentation.

For more information on SNAnalytics SDK, see [SNAnalytics - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/SNAnalyticsClientAPI.md)  and [SNAnalytics ](https://developer.servicenow.com/dev.do#!/reference/api/xanadu/client/SNAnalyticsClientAPI)– in the Developer community.

## Key structure

All locally stored keys are stored using the following structure: `sn:{API_KEY}:{KEY NAME}`

Each tracked portal has a unique API\_KEY that is stored on the instance. For example, for the portal with an API key `abcd` and a key name `tab`, the local key value would be: `sn:abc:tab`

## Session storage

Session storage is used to maintain the flow of information between web page refreshes and user navigations. Information in session storage is transient and kept available only during the lifespan of the current tab. When a tab is closed, the session storage information is removed.

The table lists the keys and values stored on session storage.

|Key|Description|
|---|-----------|
|srt|Server Response Time. The last time SNAnalytics successfully communicated with the Usage Insights server.|
|data|Queue of temporary stored analytics data points, which is periodically flushed to the backend.|
|page|The name of the current page, automatically captured by the Usage Insights server.|
|tab|Randomly generated unique identifier for the current tab.|

## Local storage

Local storage is used to maintain tracking consent information, hashed identification of the user \(which is cleared when consent is revoked\), and randomly generated identifiers for the browser. Local storage variables are persistent locally and are deleted when you clear your browsing data.

The table lists the keys and values stored on local storage.

|Key|Description|
|---|-----------|
|browser|Randomly generated unique identifier for the current browser.|
|client|The server assigned ID mapped to the browser key value.|
|user|Hashed user id, supplied by the customer.|
|consent|A Boolean \(yes/no\) value that indicates whether the user consents to be tracked.|

## Deleting local storage

To delete local storage variables, you must clear the browsing data. For example, in the Chrome browser, select **History** &gt; **Show Full History** &gt; **Clear browsing data**. In the Clear browsing data window, select **Cookies and other site data** and then select **Clear data**.

![Settings to clear local storage cookies.](../image/clear-local-storage-cookies.png)

## Data storage

Data is encrypted at rest. It’s stored in a central ServiceNow® multitenant repository closest to the instance's region, in either AMS \(Canada\), EMEA \(Germany\), or APAC \(Japan\).

Data is anonymized before it’s sent to storage, and deleted at the database level after a retention period of two years.

**Parent Topic:**[Tracked analytics fields and cookies](../concept/uxa-tracked-fields-and-cookies.md)

