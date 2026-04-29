---
title: Troubleshooting tools for Cloud Provisioning and Governance
description: The Cloud Provisioning and Governance application provides several tools to help you troubleshoot errors you might encounter during the Discovery of cloud accounts, the provisioning and managing of cloud resources, and the updating of the CMDB.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Troubleshooting tools for Cloud Provisioning and Governance

The Cloud Provisioning and Governance application provides several tools to help you troubleshoot errors you might encounter during the Discovery of cloud accounts, the provisioning and managing of cloud resources, and the updating of the CMDB.

These troubleshooting tools are available:

-   **Cloud Orchestration Trail**

    The Cloud Orchestration Trail is an activity log for all cloud resource activity on the instance. Use the Cloud Orchestration Trail to find errors that occur with cloud resources, such as credential errors during Discovery or API execution errors.

    See [Open the Cloud Orchestration Trail](../task/open-cloud-orch-api-trail.md) for instructions.

-   **Cloud API Trail**

    The Cloud API Trail is an activity log for all activity that uses the Cloud API and goes through the MID Server. Use the Cloud API Trail to see API invocations and errors related to the route data, specific API route errors, and Java runtime exceptions.

    See [Open the Cloud API Trail](cloud-api-trail.md#) for instructions.

-   **Root Cause Analysis Dashboard**

    The Root Cause Analysis Dashboard brings together records from the cloud orchestration trail and cloud API trail and presents them in useful, filterable, lists and charts.

    See [Use Cloud Root Cause Analysis reports](../task/use-cloud-root-call-analysis.md) for instructions.

-   **Cloud Orchestrations**

    Cloud Orchestrations are the orders that your instance processed for each attempted operation on a stack. Use Cloud Orchestration records to view status messages for operations that are run on cloud resources and for details about each API step.

    See [Open cloud orchestrations](../task/open-cloud-orchestrations.md) for instructions.


