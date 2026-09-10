---
title: Monitor and optimize Stream Producer performance
description: Monitor Stream Producer performance metrics and change data capture \(CDC\) queue health to identify bottlenecks and optimize for your deployment scale and throughput requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/monitor-sc-performance.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 2
keywords: [performance, monitoring, optimization, CDC queue, lag, statistics]
breadcrumb: [Stream Producer, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Monitor and optimize Stream Producer performance

Monitor Stream Producer performance metrics and change data capture \(CDC\) queue health to identify bottlenecks and optimize for your deployment scale and throughput requirements.

## Before you begin

Role required: admin

## About this task

Stream Producer performance is primarily constrained by CDC queue polling. The queue uses a non-indexed `labels` field for producer identification, which means each polling cycle performs a full-table scan. Monitoring queue depth \(lag\) and job execution time helps identify when you need to optimize.

The Stream Producer Scheduled Job runs automatically every minute \(on each active node\) to process CDC queue changes and send messages to Kafka. Each job execution processes all staged records with their configured keys and headers, formats them according to the selected serialization format \(JSON or Avro\), and publishes them to the target topic. The job has a maximum execution window of 2 minutes per run.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Stream Producers** and open an active Stream Producer.

2.  Scroll to the Stream Producer CDC Statistics related list at the bottom of the form.

    The related list displays recent statistics records showing aggregated metrics per job execution.

3.  Review the following key metrics.

    -   **Total Processing Time**: Total time \(in seconds\) spent processing this producer's labels in this job execution.
    -   **Produced Bytes**: Number of message bytes processed in this job execution.
    -   **Produced Messages**: Count of messages processed in this job execution.
    -   **CDC Depth**: Number of unprocessed changes still in the CDC queue for this producer's labels. High lag indicates the job can't keep up with incoming changes.
4.  Monitor trends over time.

    -   If **CDC Depth** is consistently growing \(each execution shows higher lag than the previous\), the producer is falling behind. Lag increasing over hours/days indicates a bottleneck.
    -   If **Total Processing Time** is approaching 2 minutes \(the job's max execution window\), the job is spending most of its time on this producer and may not have time to process other producers.
    -   If **Produced Messages** is zero but lag is high, the queue may have unprocessable records or filter conditions are too restrictive.
5.  To optimize performance, consider the following approaches.

    -   Reduce scope: On the Table Information section of the Stream Producer form, apply tighter filters to capture fewer changes. Fewer records may mean faster processing.
    -   Select specific fields: On the Stream Producer form, unselect **Capture all fields** to choose specific fields instead of capturing all fields. Smaller payloads may process faster.
    -   Simplify headers: Reduce the number of custom header fields selected. Fewer headers may mean smaller message sizes and faster serialization.
    -   Configure transaction batching: Adjust the Stream Connect property **glide.ih.kafka.stream\_producer.max\_kafka\_transaction\_bytes** to optimize transaction sizes. This property specifies the maximum number of bytes written in a single Kafka transaction. Higher values may improve throughput by batching more messages per transaction but increase memory usage; lower values may reduce latency but increase transaction overhead. Coordinate this setting with your Kafka broker configuration and network capacity.
    -   Monitor multiple producers together: If many producers are active, the job may be busy processing queued changes. Consider spreading them across multiple scheduled times or prioritizing critical producers.
    -   Alert on lag threshold: Create a business rule or alert to notify admins when CDC lag exceeds a threshold \(e.g., &gt; 1000 unprocessed records\).

## Result

You're now monitoring Stream Producer performance and can identify optimization opportunities based on queue lag and processing time trends.

**Parent Topic:**[Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/stream-producer.md)

