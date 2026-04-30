---
title: Importing historical metric data
description: Import historical metric data by using a pre-defined import template with instructions. This process helps with updating and managing metric data within an organization, helping ensure that all data complies with established business rules and maintains integrity throughout the process.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Importing historical metric data

Import historical metric data by using a pre-defined import template with instructions. This process helps with updating and managing metric data within an organization, helping ensure that all data complies with established business rules and maintains integrity throughout the process.

## Importing data and task creation

The metric import process involves you downloading a template, filling it out with required data per the instructions, and you importing it back to the system. As shown in the following example, you can download the template by navigating to the list of Metric import templates, selecting the Metric data template, and then selecting the download icon ![Download icon.](../../esg-management-reporting/images/download-icon.png) to download the Metric data upload template.xlsx file.

![Downloading the template. For the text description, refer to the text that preceded this example.](../image/metric-download-template.png "Example of downloading a template")

You can import the completed template by navigating to the Metric import jobs list, selecting **New**, providing a name and description for the job, attaching the completed template by selecting the attachment icon ![Attachment icon.](../../esg-management-reporting/images/attachment-icon.png), and then selecting the .xlsx file from your file browser. The following example shows an import job and how to attach the completed template.

![Importing the template. For the text description, refer to the text that preceded this example.](../image/metric-import.png "Example of importing a template")

The system then performs validations to check for mandatory fields like metric start date, end date, and state, as well as duplicate records. If the data meets these criteria, it is imported into the metric data table, and corresponding metric data tasks are created if you specified a task as required in the template. You can review import job details such as metrics that were ignored, skipped or updated as well as import log information by navigating to the transform history and import log tabs as shown in the following example.

![Completed import job. For the text description, refer to the text that preceded this example.](../image/metric-import-complete.png "Example of complete import job")

**Note:** When the due date for metric data tasks are calculated during an import job, non-working days are not included.

To learn more about importing historical data, see:

-   **[Download a metric import template](../task/create-metric-data-template.md)**  
Download and populate a metric import template that you can use for importing historical metric data and tasks. This template includes directions and is formatted specifically for this type of data import.
-   **[Import historical metric data and tasks](../task/import-metric-data.md)**  
Import historical metric data with or without corresponding metric data tasks.

**Parent Topic:**[Configuring GRC: Metrics](configuring-grc-metrics.md)

