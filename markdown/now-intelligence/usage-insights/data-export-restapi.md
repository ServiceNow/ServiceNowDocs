---
title: Bulk export of Usage Insights data via REST API
description: Usage Insights data export is a store app that enables you to programmatically export Usage Insights usage data from your ServiceNow instance for integration with your enterprise analytics platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/data-export-restapi.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Using Usage Insights, Usage Insights, Platform Analytics]
---

# Bulk export of Usage Insights data via REST API

Usage Insights data export is a store app that enables you to programmatically export Usage Insights usage data from your ServiceNow® instance for integration with your enterprise analytics platform.

## Overview of Usage Insights data export with REST API

Usage Insights data export delivers an asynchronous REST API endpoint that processes export requests in the background and streams results as JSON batches to a dedicated Kafka topic. Unlike manual export from the Usage Insights dashboard, data export is designed for programmatic, large-volume, recurring data movement scenarios.

The data export process follows a request-and-response model:

1.  You submit an export request to the API, specifying the data source, columns, and optional filters.
2.  The instance validates the request and returns a job ID immediately—the data itself is not returned in the API response.
3.  The export is processed asynchronously. As results are produced, they are published in batches to a dedicated Kafka topic provisioned for your instance.
4.  You consume result batches from the topic using a standard Kafka client, secured with SSL certificates.

    **Note:** Usage Insights data export supports events data source.


## Data export compared to Usage Insights dashboard export

The Usage Insights dashboard provides a built-in export function for quick and small-volume data downloads. Bring ServiceNow® usage data into tools like Microsoft Power BI, Tableau, or your enterprise data warehouse so you can analyze it alongside data from other sources.

Create end-to-end views of user behavior that spans ServiceNow and other platforms in your technology stack. Data export is a different capability designed for different use cases:

|Feature|Usage Insights Dashboard Export|Data Export Store App|
|-------|-------------------------------|---------------------|
|Volume|Suitable for small-volume, quick exports|Handles large volumes on a recurring schedule \(up to 100 GB per account per month\)|
|Frequency|Manual export triggered by dashboard user|Programmatic export driven by automated API calls and scheduled jobs so that so data flows directly to your analytics infrastructure without manual intervention.|
|Result format|Downloaded as CSV or JSON file|Streamed as JSON batches to a Kafka topic|
|Integration|User downloads and transfers file manually|Results flow directly into your Kafka consumer environment for real-time ingestion|
|Asynchronous processing|Synchronous response; export completes before download|Asynchronous; results arrive on the topic as processing completes|

## Rate and usage limits

|Limit|Value|Notes|
|-----|-----|-----|
|Requests per hour|60 per instance|Shared across all users and applications on the instance. Additional requests are throttled.|
|Result retention|36 hours|Results remain on the topic for 36 hours. Consume them before they expire.|
|Date range per request|Up to 90 days|A single request can't span more than 90 days.|
|Monthly export volume|100 GB per account/ month|Applies per customer account, aggregated across instances, on a calendar-month basis \(Base tier\).|

**Note:** Select the columns you need and apply filters to keep export volume within the rate and usage limits.

-   **[Preparing for the Usage Insights data export via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/data-export-submit-request.md)**  
Submit an export request to the Usage Insights data export API to extract usage data asynchronously and consume results from a Kafka topic.
-   **[Setting up a secure connection to Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/data-export-setup-hermes.md)**  
Configure SSL encryption for your Kafka consumers by generating an instance-signed certificate and configuring your Kafka client with SSL to securely connect to the managed Hermes cluster and consume data export results.
-   **[Consuming data export results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/consuming-data-export-results.md)**  
Consume the results of usage insights data exported via REST API, from the Kafka topic.

**Parent Topic:**[Using Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/using-uxa.md)

