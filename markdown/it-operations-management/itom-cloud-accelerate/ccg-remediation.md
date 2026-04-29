---
title: Remediation
description: Use the Cloud Configuration Governance remediation actions to fix the non-compliant cloud resource configurations identified during the scan runs.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Remediation

Use the Cloud Configuration Governance remediation actions to fix the non-compliant cloud resource configurations identified during the scan runs.

The Remediations module displays a list of all the available remediation actions for the set of violation types \(violation definitions\). Cloud Configuration Governance offers several base system remediation actions. If the application doesn’t contain the required remediation action, you can create custom actions. For more information, see [Create a remediation catalog item](../task/ccg-create-remediation-catalog-item.md) and [Create a remediation action](../task/ccg-create-remediation.md).

Because Cloud Configuration Governance performs the remediation actions on the cloud resources, you can optionally enforce additional approval requirements for the action. Whenever sn\_itom\_ccg.ccg\_operator submits a remediation request that requires approval, the application creates a change request to track the approval. You can review the list of all the change requests in the Remediation Requests module.

**Note:** Starting with Cloud Configuration Governance version 1.3.7, the base system contents are moved to the CCG Content Pack. Install the CCG Content Pack to access the base system Cloud Configuration Governance contents.

