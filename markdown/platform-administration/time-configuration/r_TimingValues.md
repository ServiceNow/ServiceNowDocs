---
title: Timing values
description: Timing values are broken down into several sections.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client transaction timings, Time configuration references, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Timing values

Timing values are broken down into several sections.

![](../image/ClientTransactionTimingDiagram.png "Client Transaction Timing")

The variables in this diagram are defined as follows:

|Variable|Description|
|--------|-----------|
|start\_time|Date and time the user requests a page \(the user clicks on a link\). This value is set by hooking into the before unload event of the previous page. WebKit browsers do not properly support the beforeunload event, which is why the client timings are not supported i Safari or Chrome.|
|load\_time|Date and time that the current page starts loading in the browser. An inline javascript that runs as the first script in the HTML body sets this value.|
|server\_time|Time in ms spent by the server processing the transaction. The server reports this value to the client.|
|load\_completion\_time|Date and time that the page is fully rendered in the browser. This operation is performed as the last script on the page and identifies the time the page completed loading.|

The following timings are reported at the bottom right of many forms and lists:

|Label|Element|Description|Calculation|
|-----|-------|-----------|-----------|
|Response Time|client\_response\_time|Overall time to deliver the page by subtracting the time the user requests the page from the time the page is fully rendered in the browser.|load\_completion\_time - start\_time|
|Server Time|client\_server\_time|Time the server takes to process the transaction.|server\_time|
|Network Time|client\_network\_time|Time the network takes to process the request. Calculated by subtracting the time of the user's request, from the time the page starts loading in the browser, and then subtracting the server processing time.|load\_time - start\_time - server\_time|
|Browser Time|browser\_time|Time the browser takes to deliver the page by subtracting the time the page is fully rendered from the time the page starts loading in the browser.|load\_completion\_time - load\_time|

**Parent Topic:**[Client transaction timings](r_ClientTransactionTimings.md)

