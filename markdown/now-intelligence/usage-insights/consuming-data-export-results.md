---
title: Consuming data export results
description: Consume the results of usage data exported via REST API, from the Kafka topic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/usage-insights/consuming-data-export-results.html
release: zurich
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-07-08"
reading_time_minutes: 2
keywords: [Consume data export results]
breadcrumb: [Bulk export of Usage Insights data via REST API, Use, Usage Insights, Platform Analytics]
---

# Consuming data export results

Consume the results of usage data exported via REST API, from the Kafka topic.

## Before you begin

Role required: admin

## Procedure

1.  Get the topic name from the 202 response.

2.  Configure two Kafka consumer processes \(one per Hermes cluster\) with the bootstrap servers, the topic name, and your SSL keystore and truststore.

3.  Use the same Consumer Group ID for both processes.

    This confirms that messages are distributed across the two processes without duplication.

4.  Subscribe to the topic and start consuming.

    Results arrive as JSON batches. Each batch includes the `job_id`, `batch_num`, `total` \(total batches\), column names, and row data.

    |Field|Description|
    |-----|-----------|
    |job\_id|Matches the job\_id returned when you submitted the request.|
    |batch\_num|The number of this batch.|
    |total\_batches|The total number of batches for the job. When batch\_num equals total, all batches have been produced.|
    |columns|The column names, in the same order as the values in each row.|
    |rows|An array of rows. Each row is an array of values matching the column order.|

5.  Use the `hermes_topic_endpoint` value from your data export API response as the topic name.

    For example:

    ```
    
    snc.<instance>.uxa.sn_uxa_data_export.data_export_results
              
    ```

    ```
    
    snc.<instance>.uxa.sn_uxa_data_export.data_export_results
              
    ```

    Start both consumer processes, and they will begin receiving batches as the export job produces results.


## Result

Your Kafka consumer environment is now securely connected to the managed Hermes cluster. You can submit data export requests and consume results from the Kafka topic using your configured consumers. Use a dedicated integration user for automated exports and grant it only the `sn_uxa_data_export.user` role and de-duplicate using the Kafka offset.

**Note:** Schedule recurring exports \(e.g., daily\) so each run stays within the 60-request-per-hour and 100 GB-per-month limits.

**Tip:** Follow these tips, as batch delivery order is not guaranteed and duplicate batches may occasionally be delivered:

-   Reassemble: Sort batches by `batch_num` to reconstruct the full result set.
-   Track completion: When `batch_num` equals `total`, all batches for the job have been produced.
-   Consume within retention window: Results are retained on the topic for 36 hours. Consume all batches before they expire.
-   Each instance has its own dedicated Kafka topic for result delivery. The SSL certificate used to access the topic is scoped to your instance's topics only. Exports are bound to your customer account: data from one account is never accessible from another account's instance.

**Parent Topic:**[Bulk export of Usage Insights data via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/usage-insights/data-export-restapi.md)

