---
title: DEX browser extension permissions and data collection
description: The DEX browser extension requests specific browser permissions to measure the performance, availability, and usage of monitored web applications. Each permission is limited to the minimum access required for that measurement purpose.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/dex-browser-extension-permissions.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 3
keywords: [browser extension permissions, web application usage data, chrome extension permissions, edge extension permissions, host permission, declarative net request, data collection]
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX browser extension permissions and data collection

The DEX browser extension requests specific browser permissions to measure the performance, availability, and usage of monitored web applications. Each permission is limited to the minimum access required for that measurement purpose.

## How web application usage data is collected

Application usage data is collected differently depending on whether the application is installed on the endpoint or accessed through a browser:

-   Installed application usage data is collected by the Agent Client Collector \(ACC\) installed on the endpoint.
-   Web application usage data is collected by the DEX browser extension for Google Chrome and Microsoft Edge. The extension reports the collected data through the same channel used by ACC: data is routed from the browser extension to ACC, and then sent to the ServiceNow shared services and on to your instance.

To collect this data, the browser extension requests the browser permissions described in the following table. Each permission is limited to the minimum access required to measure page performance and availability for monitored applications. The extension does not read page content, form data, cookies, or credentials.

## Permissions requested by the browser extension

|Permission|Purpose|
|----------|-------|
|Storage|Temporarily saves collected performance metrics, such as page load times and session data, on the local device between collection intervals, before the data is sent to your instance.|
|Active Tab|Identifies the currently active tab so the extension can determine which tab to collect and update data for while a user is viewing it.|
|Tabs|Detects when a monitored application's tab is opened, kept open, or closed, to determine what session and usage data to record. This permission applies only to tabs recognized as monitored applications.|
|Alarms|Triggers metric collection and reporting on a recurring schedule instead of continuously, to minimize the impact on browser performance.|
|Web Request|Observes network requests made by monitored applications, specifically counting successful and failed requests, to calculate an application availability score.|
|Declarative Net Request|Adjusts the Origin and Content-Type request headers on requests sent to the extension's own reporting service, so that they meet the security requirements of that service.|
|Declarative Net Request with Host Access|Works with the Declarative Net Request permission, but restricts the header adjustment to a single, specific destination. This ensures the adjustment can't affect requests to any other site.|
|Host Permission \(access to site URLs\)|Reads the URL of open browser tabs, so the extension can determine when a monitored application was opened and how long it remained open. This is the basis for the usage and performance metrics shown in your instance.|

## Scope of data collected

-   The extension extracts only standard browser performance timing data, such as page load, network, and response timings. It does not access page content, form inputs, cookies, or credentials.
-   The Web Request and Declarative Net Request permissions are used narrowly: to count request successes and failures, and to adjust two specific headers on calls to the extension's own reporting service. They aren't used to read or modify the content of requests or responses to any other site.
-   The Host Permission and Tabs permissions require broad tab and URL visibility because the extension can't determine in advance which sites are your monitored applications. That determination happens at runtime, and only recognized monitored applications have their data recorded.
-   Collected metrics are limited to performance and availability statistics, such as load times, session duration, and request success or failure counts, tied to monitored application URLs. The extension reports metrics only to your own instance.

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)

**Related topics**  


[DEX Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-architecture.md)

[Enable DEX browser extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/enable-dex-browser-extension.md)

[Installed with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/components-installed-with-dex.md)

