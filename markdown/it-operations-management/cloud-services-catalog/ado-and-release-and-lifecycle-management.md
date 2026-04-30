---
title: Stages of Azure DevOps in Release life cycle management
description: The components and stages of an Azure DevOps pipeline are comprehensive and highly customizable. You can define multiple stages, tasks, and integrations based on your specific requirements and technology stack using Cloud Services Catalog.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CSC references, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Stages of Azure DevOps in Release life cycle management

The components and stages of an Azure DevOps pipeline are comprehensive and highly customizable. You can define multiple stages, tasks, and integrations based on your specific requirements and technology stack using Cloud Services Catalog.

<table id="simpletable_lz2_bfp_fyb"><thead><tr><th>

Day 0 support

</th><th>

Day 1 support

</th><th>

Day 2 support

</th></tr></thead><tbody><tr><td>

1.  Scan the projects and pipelines
2.  Gather pipeline variables from Azure DevOps

</td><td>

1.  Order from Service Catalog
2.  Reference from discovered Azure DevOps projects and pipelines
3.  Select inputs needed for the release deployment pipeline
4.  Submit catalog

</td><td>

1.  SRE operations – patching, backup, etc, on production resources
2.  Daily maintenance – restart, reboot, suspend, etc.
3.  Tagging resources, Running hardening, etc.

</td></tr><tr><td>

Store in CMDB as referable objects

</td><td>

1.  Wait for approval
2.  Track the progress
3.  Update CMDB with deployed resources

</td><td>

1.  Ensure resilience in production.
2.  Switch between blue and green environment

</td></tr></tbody>
</table>**Parent Topic:**[CSC references](csc-reference.md)

