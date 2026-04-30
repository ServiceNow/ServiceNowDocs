---
title: Performing real-time updates to tags for cloud resources
description: You can set up cloud events processing and map a tag policy to update tags for cloud resources in real time.
locale: en-US
release: zurich
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Performing real-time updates to tags for cloud resources

You can set up cloud events processing and map a tag policy to update tags for cloud resources in real time.

## Prerequisites

-   Cloud events table \[sn\_cmp\_cloud\_events\] table does not have any records in the **processed** state.
-   CIs impacted by tag change events are identified by either CAPI or Discovery and Service Mapping patterns.
-   Configured at least one tag policy.
-   Select the **Run on cloud events** check box in the tag policy you create.

## Instructions depend on the cloud provider

See the following setup instructions for cloud event processing:

-   [Configure the Amazon AWS Config service to auto-update the CMDB](../task/aws-config-service-cloud-mgt.md)
-   [Configure the Microsoft Azure Alert service to auto-update the CMDB](microsoft-azure-alert-driven-discovery.md#)
-   [Configure the Google Cloud's Operations Suite Logging service to auto-update the CMDB](../task/gcp-stackdriver-service.md)

Process cloud events related to changes in tags and execute tag audits on the events in real time.

Unlike regular tag audits, where the audit is performed on all CIs in the CMDB that the tag policy applies to, tag events are processed per CI. Based on the prerequisites, tag event processing occurs on events that are identified with a tag change. The impacted CI is identified and, if the associated policy is applicable to the CI, the tag policy is run on the identified CI.

If the **Run on cloud events** check box is selected during policy creation, the policy is selected to run an audit on tag change events. If the check box is cleared, the audit is not run on the CI even if there are tag change cloud events.

View the change type that applies to the tag \(the change that triggered the audit\) in the Tag Change Log \[sn\_itom\_tag\_change\_log\] table. The records in the table are stored for 90 days by default. The change log records appear whether a remediation run or an event triggered the change on the CI. You can also view tags that were added or updated as part of the change.

## Optimizing performance

High event inflow or a large number of tag policies can decrease performance. You can modify the following system properties to ensure acceptable performance:

-   \[sn\_itom\_tag.azure\_window\_size\] - This system property is configurable \(in minutes\).
-   \[sn\_itom\_tag.max\_audit\_lag\_ratio\] - Specify the lag between tag audits that are already running, before the audit triggers on the records ready for audit.
-   \[sn\_itom\_tag.policy\_batch\_size\] - Batch size on which the tag audit is run.
-   \[sn\_itom\_tag.event\_batch\_size\] - Event batch size to be processed.

