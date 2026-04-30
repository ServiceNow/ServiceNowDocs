---
title: Discovery's contribution to Tag Governance
description: The Discovery and Cloud Discovery features discover all resources in the CMDB as well as cloud resources from cloud providers such as Amazon AWS Cloud, Microsoft Azure Cloud, and Google Cloud Platform \(GCP\).
locale: en-US
release: zurich
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Discovery's contribution to Tag Governance

The Discovery and Cloud Discovery features discover all resources in the CMDB as well as cloud resources from cloud providers such as Amazon AWS Cloud, Microsoft Azure Cloud, and Google Cloud Platform \(GCP\).

## The role of discovery

Discovery and Cloud Provisioning and Governance can discover tags that are used by all major cloud providers and container ecosystems through Service Mapping patterns. Once the tags are discovered, Service Mapping can create application services that are based on the tags. Typically, organizations use tagging in virtualized, hyper-converged, or multi-cloud infrastructures. For examples of the infrastructure types and tags used for them, see [Tag-based discovery in Service Mapping](../../service-mapping/concept/tag-based-mapping.md).

Discovery also collects cloud tags that are specific to each virtual machine \(VM\) and saves them to the Key Value \[cmdb\_key\_value\] table.

The discovery process also detects tags that are associated with CIs. If your organization does not use consistent tagging standards or terms \(key-value pairs\), however, managing CIs with tags becomes difficult.

