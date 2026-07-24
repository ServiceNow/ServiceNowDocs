---
title: Preparing for the Usage Insights data export via REST API
description: Submit an export request to the Usage Insights data export API to extract usage data asynchronously and consume results from a Kafka topic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/data-export-submit-request.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Bulk export of Usage Insights data via REST API, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Preparing for the Usage Insights data export via REST API

Submit an export request to the Usage Insights data export API to extract usage data asynchronously and consume results from a Kafka topic.

## Before you begin

Role required: sn\_uxa\_data\_export.user

Activate Usage Insights data export:

-   Install Usage Insights Data Export store app \(`sn_uxa_data_export`\) on your instance.

    **Note:** Installing the app activates the data export REST API endpoint and provisions the managed Hermes topic used to deliver results.

-   Prepare the Kafka consumer environment that can connect to your managed Hermes cluster.

    **Note:** Before setting up your export request parameters, verify that your Kafka environment is fully prepared and configured.


**Important:** Not yet available in some regulated markets. Check the Store listing for availability in your region.

## About this task

This task involves preparing the export request parameters, managing API request submitted and response received, securing Hermes and consuming export results.

## Procedure

1.  Have your instance URL and user credentials ready for authentication.

2.  Navigate to the Usage Insights dashboard.

3.  Search and select the application you would like to export data from.

4.  Navigate to **Events** to explore various event names.

5.  Review and select the column and available data before you submit the export request.

6.  Prepare your export request parameters.

    See [UXA Data Export Service API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/usage-insight-data-exp-api.md) to learn more.

    1.  Submit the export request via the REST API.

    2.  Export request response.

    3.  Capture the response and job ID.


## What to do next

Set up a secure connection to Hermes, to start consuming data export results. See [Setting up a secure connection to Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/data-export-setup-hermes.md).

**Parent Topic:**[Bulk export of Usage Insights data via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/data-export-restapi.md)

