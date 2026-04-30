---
title: Application Insights detail graphs and metrics
description: The Application Insights detail graphs provide views of individual metrics at the node level.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with Application Insights graphs, Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application Insights detail graphs and metrics

The Application Insights detail graphs provide views of individual metrics at the node level.

|Metric|Source|Description|
|------|------|-----------|
|Events Processed|**events\_processed** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of events processed|
|Events Logged|**event\_logs** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of events logged|

|Metric|Source|Description|
|------|------|-----------|
|Ready on Output|ECC Queue Statistics \[ecc\_queue\_stats\_by\_ecc\_agent\] table|Average number of entries in the Ready state in the ECC output queue|
|Ready on Input|ECC Queue Statistics \[ecc\_queue\_stats\_by\_ecc\_agent\] table|Average number of entries in the Ready state in the ECC input queue|
|Processing on Output|ECC Queue Statistics \[ecc\_queue\_stats\_by\_ecc\_agent\] table|Average number of entries in the Processing state in the ECC output queue|
|Processing on Input|ECC Queue Statistics \[ecc\_queue\_stats\_by\_ecc\_agent\] table|Average number of entries in the Processing state in the ECC input queue|
|Processed on Output|ECC Queue Statistics \[ecc\_queue\_stats\_by\_ecc\_agent\] table|Average number of entries in the Processed state in the ECC output queue|
|Processed on Input|ECC Queue Statistics \[ecc\_queue\_stats\_by\_ecc\_agent\] table|Average number of entries in the Processed state in the ECC input queue|

|Metric|Source|Description|
|------|------|-----------|
|Average Transaction Response Time|**transactions** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Average transaction processing time in seconds|
|Transaction Count|**transactions** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Load of transactions on the instance|
|Logged in Users|**sessionsummary** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of users logged in to the instance over time|
|Semaphore API\_INT Queue Depth|**semaphores** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions in the API Integrations semaphore queue|
|Semaphore Default Queue Depth|**semaphores** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions in the Default semaphore queue|
|Semaphore AMB Send Queue Depth|**semaphores** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of messages in the AMB Send queue being sent to the client|
|Semaphore AMB Receive Queue Depth|**semaphores** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of messages in the AMB Send queue being received from the client|
|Semaphore API\_INT Rejections|**semaphore\_api\_int\_rejection** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions rejected by the API Integrations semaphore queue|
|Semaphore Default Rejections|**semaphore\_default\_rejected** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions rejected by the Default semaphore queue|
|Semaphore AMB Send Rejections|**semaphore\_amb\_send\_rejected** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions rejected by the AMB Send queue|
|Semaphore AMB Receive Rejections|**semaphore\_amb\_receive\_rejected** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions rejected by the AMB Receive queue|
|Average Database Response Time|**sql\_response** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Average response time \(in milliseconds\) for database operations|
|Database Throughput|**database\_throughput** key in the Stats column in the Node stats \[sys\_cluster\_node\_stats\] table|Number of transactions processed per second.|

**Parent Topic:**[Working with Application Insights graphs](working-with-application-insights-graphs.md)

