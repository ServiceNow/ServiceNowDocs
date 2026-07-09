---
title: Setting up data export via REST API
description: Submit an export request to the Usage Insights data export API to extract UXA usage data asynchronously and consume results from a Kafka topic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/data-export-submit-request.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [Export data in bulk export via REST API, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Setting up data export via REST API

Submit an export request to the Usage Insights data export API to extract UXA usage data asynchronously and consume results from a Kafka topic.

## Before you begin

Role required: sn\_uxa\_data\_export.user

Activate Usage Insights data export:

-   Install Usage Insights Data Export store app \(`sn_uxa_data_export`\) on your instance.

    **Note:** Installing the app activates the data export REST API endpoint and provisions the managed Hermes topic used to deliver results.

-   Have your instance URL and user credentials ready for authentication.
-   Identify the event names, applications, and columns you want to export.
-   Use the Usage Insights dashboard to review available data before you submit the request.

    **Note:** Availability in some regulated markets may follow general availability. Check the Store listing for availability in your region.


## About this task

The process of Usage Insights data export using REST API involves preparing the export request parameters, managing the API request submitted and response received, securing Hermes and consuming export results.

## Procedure

1.  Prepare your export request parameters.

    See [UXA Data Export Service API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/usage-insight-data-exp-api.md) to learn more.

    1.  Submit the export request via the REST API.

    2.  Export request response.

    3.  Capture the response and job ID.

2.  Prepare the Kafka consumer environment that can connect to your managed Hermes cluster, with the required network ports open and consume the results from the Kafka topic.

    See [Setting up a secure connection to Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/data-export-setup-hermes.md).


**Parent Topic:**[Export data in bulk export via REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/data-export-restapi.md)

