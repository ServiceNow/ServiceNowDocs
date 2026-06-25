---
title: Enable Nutanix event discovery
description: Activate the Nutanix events scheduled job to trigger rediscovery of Nutanix components when a state change is detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/enable-nutanix-event-job.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 1
breadcrumb: [Nutanix Acropolis, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable Nutanix event discovery

Activate the Nutanix events scheduled job to trigger rediscovery of Nutanix components when a state change is detected.

## Before you begin

-   Verify that Nutanix Components discovery has run and that the Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\] table is populated.
-   Verify that the MID Servers for Nutanix event discovery have **All** or **Nutanix** capability.
-   For Nutanix v4 event discovery, verify that you have at least version 1.31.0 of Discovery and Service Mapping Patterns.

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Name** column, search for the scheduled job.

    -   For API v1–3, search for `Nutanix-Events-job`.
    -   For API v4, search for `Nutanix-Events-job-V4`.
3.  Select the scheduled job.

4.  Select the **Active** check box.

    The job runs every five minutes by default. You can change the run frequency using the **Run** field.

5.  Select an option to run the job:

    -   Select **Update** to enable the job to run on its configured schedule.
    -   Select **Execute Now** to run the job immediately.

**Parent Topic:**[Nutanix Acropolis discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nutanix-pattern.md)

**Related topics**  


[Nutanix Acropolis discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nutanix-pattern.md)

