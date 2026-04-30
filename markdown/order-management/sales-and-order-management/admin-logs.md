---
title: The Admin Logs utility
description: Learn how the Admin Logs utility helps you diagnose, monitor, and resolve configuration issues efficiently in your ServiceNow CPQ environment.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 3
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The Admin Logs utility

Learn how the Admin Logs utility helps you diagnose, monitor, and resolve configuration issues efficiently in your ServiceNow CPQ environment.

## Overview of Admin Logs

The Admin Logs utility provides administrators with centralized visibility into system activities, configuration errors, and integration issues. It enables quick diagnosis and resolution of problems by capturing key runtime details, error messages, and contextual data about the environment. Designed with usability and precision in mind, Admin Logs helps administrators identify issues, understand their cause, and act swiftly to maintain system stability.

Whether accessed through the Admin UI or via API, Admin Logs helps provide insights admins can use to optimize configurations and keep users productive.

## Key benefits

|Benefit|Description|
|-------|-----------|
|Centralized visibility|Monitor configuration, runtime, and integration errors in one location.|
|Real-time monitoring|Quickly refresh and filter logs to focus on the most recent or relevant time frames.|
|Faster troubleshooting|Review detailed error codes, contextual messages, and user IDs for precise diagnostics.|
|API accessibility|Retrieve log data programmatically for automation or custom dashboards.|
|Continuous improvement|Access enhanced error reporting and contextual details to help streamline ongoing maintenance and user support.|

## Accessing Admin Logs

Administrators can access Admin Logs from the ServiceNow CPQ Admin interface or via API, depending on their preferred workflow and use case.

In the new Admin experience, access Logs in the Utilities menu. In the legacy Admin experience, click **Logs** in the navigation bar. Both experiences provide the same real-time logging capabilities and enable filtering, refreshing, and viewing detailed error information.

## Refreshing and filtering

The Logs interface supports real-time filtering and refresh options. Choose a time range that best suits your analysis needs:

-   Past 15 minutes
-   Past hour
-   Past 24 hours
-   All logs

**Note:** Use the refresh button to update the view with the latest events without leaving the Logs page.

## Log details format

Each log entry is displayed in a structured format, making it easy to scan and understand issues. This structure enables administrators to efficiently filter, correlate, and resolve errors across different sessions and components. The log data includes the following columns:

-   Date and time: User-friendly date display and exact time in milliseconds \(added February 2025\).
-   Error message: A descriptive summary of the issue encountered.
-   Error code: ServiceNow CPQ unique identifier for quick cross-referencing and support requests.
-   User ID: The user who encountered the error \(added February 2025\).

## Accessing logs via API

Administrators who prefer to query logs programmatically can access the Admin Logs API using a GET request. This is especially useful for environments with large data sets or for integrating logs into external monitoring systems. This flexibility allows admins to retrieve specific log intervals for audit or performance review without loading all historical records.

Example cURL command:

```code

    curl --location '<logikURL>/api/logs/v1/logs' \
    --header 'Content-Type: application/json' \
    --header 'Origin: localhost' \
    --header 'Authorization: <Admin API Key>'
   
```

You can refine results by specifying before and after parameters in ISO 8601 date/time format:

```code

    curl --location '<logikURL>/api/logs/v1/logs?after=YYYY-MM-DDThh%3Amm%3AssZ&before=YYYY-MM-DDThh%3Amm%3AssZ' \
    --header 'Content-Type: application/json' \
    --header 'Origin: localhost' \
    --header 'Authorization: <Admin API Key>'
   
```

## Continuous improvements

Admin Logs continually evolves to provide deeper insights and improve usability. Enhancements introduced in February 2025 include:

-   Enhanced error messages: Save errors now include related configuration errors for faster issue identification.
-   Contextual information: For enrichment script errors, logs now capture the specific enrichment area, affected blueprint, and revision ID for precise debugging.
-   Detailed external connection errors: “Method not supported” HTTP errors now include the path and method used in the external call.
-   Performance metrics: Metrics for external integrations are now tracked and available upon request through ServiceNow CPQ support.

## Best practices

-   Use short time filters when troubleshooting real-time configuration issues.
-   Export relevant log data regularly for long-term tracking or compliance review.
-   Leverage the API to automate log retrieval or integrate with your organization’s monitoring tools.
-   Report unclear error codes or missing context to ServiceNow CPQ support for analysis and improvement.

