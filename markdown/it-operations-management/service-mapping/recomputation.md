---
title: Service Mapping Recomputation
description: Keep application services up to date and track changes to services through the recomputation capability of the Application Service feature of Service Mapping. Recomputation jobs recalculate mapped application services when changes occur to an associated configuration item \(CI\) within the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping Recomputation

Keep application services up to date and track changes to services through the recomputation capability of the Application Service feature of Service Mapping. Recomputation jobs recalculate mapped application services when changes occur to an associated configuration item \(CI\) within the Configuration Management Database \(CMDB\).

The most common changes that can cause recomputation are:

-   Topology changes: The relationship of the associated CI to other CIs changes. These changes might include the addition of a new relationship or the removal of a previous one.
-   CI changes: A field value of the CI changes.

These changes might be caused by horizontal discovery, top-down discovery, service graph connectors, or manual operations. If the CI change doesn't affect the topology or service associations, the recomptuation process stops with no changes to the service.

Two types of recomputation jobs are available in the system scheduler: Service Mapping recomputation and Service Mapping fast recomputation. Fast recomputation selects services with only CI changes as part of their most recent batch and doesn’t include topology changes.

Recomputation jobs are configured to run every five seconds. After the jobs are initiated, they begin with the service that has waited the longest. When the job is complete, the effect of topology changes might be reflected in the topology of the map or a change in the service associations. You can view CI changes by selecting the map node of the CI. Successful recomputations appear as a single checkpoint on the application service timeline regardless of whether it represents one change or a batch of changes.

You can configure the recomputation type, frequency, and other factors as needed. For more information about Service Mapping, see the [Service Mapping Recomputation Jobs: Configuration and Best Practices \[KB1001151\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1001151) article in the Now Support Knowledge Base.

**Parent Topic:**[Service Mapping reference](../reference/service-mapping-reference.md)

