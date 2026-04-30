---
title: Verify the Vulnerability Response Integration with Palo Alto Prisma Cloud import run status
description: Use the Vulnerability Response Integration with Palo Alto Prisma Cloud import run status to verify the success of your integration runs and to identify any issues.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Verify the Vulnerability Response Integration with Palo Alto Prisma Cloud import run status

Use the Vulnerability Response Integration with Palo Alto Prisma Cloud import run status to verify the success of your integration runs and to identify any issues.

## Before you begin

Role required: admin

## About this task

During integration execution, multiple processes are generated, and data is received in the form of pages. Each process can contain one or more import queue entries with attached data in pages. These entries must process the data within the one-hour time limit. However, if the payload size is large, the processing time may exceed one hour or get stuck, resulting in an integration timeout error. The integration continues to process the data despite the timeout error. To avoid this miscommunication, starting from version 14.8.5 of Configuration Compliance, timestamps \(heartbeats\) are sent periodically to indicate if the queue is active and processing data. The **Last Record Processed** field in the Import Queue Entry page is updated based on the count of records the import queue creates or updates. In case an import queue entry exceeds the one-hour time limit, the system checks the **Last Record Processed** field to see if it is also older than one hour. If it is, this indicates that the import queue entry is stuck, and it is timed out to prevent any further delays in processing.

**Note:** The **Last Record Processed** field is updated based on what is defined in the following system properties:

-   **sn\_sec\_cmn.record\_threshold\_heartbeat**: Defines the number of processed records, after which the heartbeat \(timestamp\) is sent to the import queue entry.
-   **sn\_sec\_cmn.maximum\_heartbeat\_delay**: Defines the time after which the import queue entry must be timed out.

## Procedure

1.  Navigate to **Prisma Cloud Integration** &gt; **Integrations**.

2.  Click **Prisma Policies Integration**.

3.  Click **Execute Now**.

    When this integration is run, the following tables are populated in this order:

    1.  sn\_vulc\_test.list \(Configuration Tests\)
    2.  sn\_vulc\_auth\_src \(Authoritative Source
    3.  sn\_vulc\_citation \(Citations\)
4.  Under the **Items** tab, view the number of new tests created, updated, and ignored by clicking the vulnerability integration run.

    **Note:** Policies are defined in Prisma Cloud for the selected cloud instance. The instance is scanned based on the defined policies.

5.  Click **Prisma Alerts Integration**.

6.  Click **Execute Now**.

    The following tables are populated based on the integration:

    -   Test Results
    -   Discovered Items: If the configuration items are unavailable in the system, they are created. The class is always Cloud Resource. On the Discovered Item page, three new fields are created: **Cloud resource type**, **Cloud service provider**, and **Asset Category**.

        Under the **Items** tab, click the vulnerability integration run to view the number of new tests results imported, updated, and ignored. The **Configuration Items** tab also gets populated based on the number of test results created.


