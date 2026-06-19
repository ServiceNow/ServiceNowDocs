---
title: Impact Store Application storage estimation
description: The Impact store app stores data within your ServiceNow instance and contributes to your instance's overall storage footprint. Storage usage varies depending on whether your instance is connected to the Impact Delivery Instance and on the level of collaboration activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/impact-store-app-storage-estimation.html
release: australia
product: Impact
classification: impact
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Impact, Impact Store App, IIP, storage estimation, storage footprint, Impact Delivery Instance, IDI, Product Adoption Roadmap, PAR, data retention, Platform Health]
breadcrumb: [Impact reference, Impact]
---

# Impact Store Application storage estimation

The Impact store app stores data within your ServiceNow instance and contributes to your instance's overall storage footprint. Storage usage varies depending on whether your instance is connected to the Impact Delivery Instance and on the level of collaboration activity.

## Why Impact storage may differ from other applications

Unlike most applications that generate data only within your instance, Impact enables ongoing collaboration between your organization and ServiceNow experts \(squads\). When connected to the Impact Delivery Instance, this collaboration migrates and synchronizes additional data into your instance, increasing its storage footprint beyond what is generated locally.

## How storage usage changes based on connection

Storage behavior differs depending on whether your instance is connected to the Impact Delivery Instance.

-   **Not connected to the Impact Delivery Instance**

    Data is generated only within your instance. For example, running health scans produces reports and findings that consume storage. The storage footprint scales proportionally with feature usage, where more health scans or more generated records result in more storage consumption, similar to other ServiceNow applications.

-   **Connected to the Impact Delivery Instance**

    Data is initially migrated and then periodically synchronized, enabling collaboration between your organization and your Impact squads. Additional data is introduced into your instance, including:

    -   Outcomes defined and tracked jointly
    -   Product Adoption Roadmaps \(PARs\) created by the Squad
    -   Accelerator requests and execution updates
    -   Conversations and collaboration records
    -   Attachments and supporting artifacts shared by the Squad
    This results in an incremental increase in storage usage based on the level of collaboration and activity.


## What drives storage growth

Storage usage in Impact is primarily driven by the following factors:

-   Number of outcomes being tracked
-   Number of Product Adoption Roadmaps \(PARs\)
-   Volume of Accelerator requests and updates
-   Frequency of conversations and collaboration
-   Use and size of attachments and supporting documents, which typically contribute the most to storage growth
-   Duration of data retention, effected by cleanup and archiving rules

## Illustrative storage footprint ranges

The following ranges are indicative examples to help estimate potential storage usage based on typical usage patterns. Actual values may vary based on implementation and usage.

<table id="table-storage-ranges"><thead><tr><th>

Usage tier

</th><th>

Typical characteristics

</th></tr></thead><tbody><tr><td>

Small \(light usage\)

</td><td>

-   Limited outcomes \(for example, 5–10\)
-   Few Product Adoption Roadmaps
-   Minimal Accelerator activity
-   Limited or no attachments
-   Low collaboration volume

</td></tr><tr><td>

Medium \(moderate usage\)

</td><td>

-   Moderate outcomes \(for example, 10–20\)
-   Multiple Product Adoption Roadmaps
-   Regular Accelerator requests and updates
-   Moderate use of attachments
-   Ongoing collaboration and conversations

</td></tr><tr><td>

Large \(high usage / mature adoption\)

</td><td>

-   High number of outcomes \(for example, 25+ across teams\)
-   Extensive Product Adoption Roadmaps
-   Frequent Accelerator usage
-   Significant volume of attachments and artifacts, including large PPTs and images
-   Continuous collaboration with ServiceNow squads

</td></tr></tbody>
</table>## Key considerations

-   Impact data is stored within your instance and contributes to overall database storage usage.
-   Storage growth is directly correlated with feature usage and collaboration levels.
-   Higher engagement with Impact capabilities may result in increased storage consumption.

**Parent Topic:**[Impact reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-reference.md)

