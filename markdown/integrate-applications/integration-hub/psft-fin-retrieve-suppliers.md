---
title: Retrieve daily supplier data from Oracle PeopleSoft
description: Set the date up to which the Oracle Peoplesoft Financial spoke retrieves daily supplier data, and then view the retrieved records in the PSFT Data module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/psft-fin-retrieve-suppliers.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-16"
reading_time_minutes: 1
breadcrumb: [Oracle Peoplesoft Financial Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Retrieve daily supplier data from Oracle PeopleSoft

Set the date up to which the Oracle Peoplesoft Financial spoke retrieves daily supplier data, and then view the retrieved records in the PSFT Data module.

## Before you begin

-   [Configure a connection for the Oracle Peoplesoft Financial spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/psft-fin-conctn-config.md).
-   Configure the trigger for the Polling Suppliers subflow.
-   Role required: admin.

## Procedure

1.  Navigate to **PSFT Flow Execution** &gt; **PSFT Flow Executions**.

2.  Click **New**.

3.  Select the date up to which you want to retrieve the daily suppliers data in **Last Successfull Execution**.

4.  Click **Submit**.


## Result

Based on the trigger you have configured in the Polling Suppliers subflow, data is retrieved periodically. To view the data, navigate to **PSFT** &gt; **PSFT Data**.

