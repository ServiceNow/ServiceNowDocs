---
title: Cloud Request Retry Configuration
description: If a request is throttled by a cloud provider during Discovery, Cloud Request Retry Configuration provides a customizable method to retry requests. Discovery and Service Mapping Patterns includes a retry configuration for AWS and Azure. You can customize the included configuration or create your own.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install and configure MID Servers to access cloud environments, Access to cloud environments for ITOM products, IT Operations Management]
---

# Cloud Request Retry Configuration

If a request is throttled by a cloud provider during Discovery, Cloud Request Retry Configuration provides a customizable method to retry requests. Discovery and Service Mapping Patterns includes a retry configuration for AWS and Azure. You can customize the included configuration or create your own.

Discovery admins and Cloud admins can access the request retry configuration at **All** &gt; **Discovery** &gt; **Cloud Request Retry Configuration**. You can create one configuration for each provider.

When a request is throttled, the retry framework uses retry configuration defined for the provider to handle retries before returning the final response to the ApiCommand classes:

-   AwsApiCommand
-   AzureApiCommand

The retry configurations are synced with the MID Servers through the MID Server property, **mid.cloud.discovery.retry.configuration**.

There are the following retry strategies:

-   Exponential backoff
-   Response header backoff
-   Custom backoff

## Exponential backoff

For the following example configuration:

|Setting|Value|
|-------|-----|
|Max retries|3|
|Response codes|429|
|Base delay in ms|1000|
|Max delay in ms|10000|
|Additional delay window in ms|1500|

The Exponential backoff retry strategy works as follows:

-   1st retry—the backoff multiplier is randomly selected between 0 and 1. The max delay value is 400 ms \(400 \* 1\).
-   2nd retry—the backoff multiplier is randomly selected between 0 and 3. The max delay value is 1200 ms \(400 \* 3\).
-   3rd retry—the backoff multiplier is randomly selected between 0 and 7. The max delay value is 2800 ms \(400 \* 7\).

On subsequent retries, if the delay exceeds 10000 \(the max delay\), 10000 will be used as initial delay.

Once the initial delay is generated, jitter is added to the delay. The jitter window is defined by the **Additional delay window in ms** field. The system selects a random value between 0 and 1500 and adds it to the initial delay.

If the initial delay is 500, the final delay \(with jitter\) can be a value between 500 and 2000 ms.

## Response header backoff

For the following example configuration:

|Setting|Value|
|-------|-----|
|Max retries|3|
|Response codes|429|
|Response header|Retry-After|
|Response header delay unit|Seconds|
|Additional delay window in ms|1500|

The Response header backoff strategy works as follows:

-   Fetch the value of header **Retry-After** from the server response.
-   Convert the **Retry-After** to milliseconds by multiplying by 1000.

Once the initial delay is generated, jitter is added to the delay. The jitter window is defined by the **Additional delay window in ms** field. The system selects a random value between 0 and 1500 and adds it to the initial delay.

If the initial delay is 2000, the final delay \(with jitter\) can be a value between 2000 and 3500 ms.

## Custom backoff

With a custom backoff retry strategy, you define the **Max retries** and **Response codes** and create your own **Mid script include** that defines how requests are retried using the **getDelay\(\)** function. For more information, see Script includes.

**Parent Topic:**[Install and configure MID Servers to access cloud environments](../task/mid-server-configuration-cloud.md)

