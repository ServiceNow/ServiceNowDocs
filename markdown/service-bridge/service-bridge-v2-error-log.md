---
title: Service Exchange error log
description: Track errors on recent transactions, provide connection status, run health checks, and provide recommendations.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Exchange reference, Service Exchange]
---

# Service Exchange error log

Track errors on recent transactions, provide connection status, run health checks, and provide recommendations.

## About this task

**Note:** The Xanadu release, includes a framework to capture Service Exchange errors. Currently, the table displays the following known errors:

1.  Global Script Include check: Checks if this script has been installed and if it is the latest version.
2.  During registration for provider: Captures errors from the creation of the registration task through closed complete. An email notification with the list of errors captured in the last one hour along with the cause and solution is sent to the Service Exchange administrator.
3.  During Registration for consumer: Captures errors from the creation of the Provider Connection record through closed complete. An email notification with the list of errors captured in the last one hour along with the cause and solution is sent to the Service Exchange administrator.
4.  Remote system inbound and outbound errors
5.  Heartbeat connection

You can view and diagnose errors and follow the steps provided to resolve the errors. Errors are logged as they occur, and if there have been any new ones in the last hour, an email notification is sent to the Service Exchange administrators. Each error record provides the following details:

-   A detailed description of the error.
-   Reason the error has occurred.
-   Steps to resolve the error.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Error Log**.

    The list of errors that have occurred is displayed.

    **Note:** You can view errors on the consumer instance. To do so, login to consumer instance, and navigate to **All** &gt; **Service Exchange Consumer** &gt; **Administration** &gt; **Error Log**.

2.  Click on the Number link to view the error.

3.  The following details are displayed.

    |Field|Description|
    |-----|-----------|
    |Number|The number assigned to the error.|
    |Known error|Detailed information about the error and how to resolve it. This information is displayed in the fields below.|
    |Error|A detailed description of the error.|
    |Cause|Reason the error has occurred. If this is not a known issue, the Cause is set to **Unknown**.|
    |Solution|A link is provided to the Knowledge Base article that contains the steps that need to be followed to resolve the error.|
    |Connection|This field is populated if the error is caused by connection issue.|
    |Created|Date and time at which the error occurred.|


