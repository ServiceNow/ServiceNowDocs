---
title: Testing common control and implementing results on multiple reliant entities
description: Instead of generating controls for individual entities and testing each entity separately with an individual control, you can use a common control and associate a primary entity to it.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage controls using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Testing common control and implementing results on multiple reliant entities

Instead of generating controls for individual entities and testing each entity separately with an individual control, you can use a common control and associate a primary entity to it.

Test the common control for control tests, indicators, attestations, issues, and policy exceptions. Use the test results that are inheritable and implement them on all the reliant entities associated to the common control.

![Multiple entities linked to a common control.](../image/CommonControlOverview.png "Multiple entities linked to a common control")

Using common controls gives you the ability to:

-   Mark a control as common and associate reliant entities to it.
-   Associate entities of existing controls as reliant entities to a common control.
-   Save time and effort in testing. The result of the common control tests can be inherited by other reliant entities, especially when a new system is deployed and pre-validation audits are conducted within an organization or environment.
-   Reduce redundancy of workforce in documenting test results.

Requirements and use case:

-   Create a control and convert a control to common.
-   Associate reliant entities to a common control to inherit test results.
-   Associate entity types to a common control.
-   Test the common control once and apply results to multiple entities.
-   Can convert a common control back to standard.
-   Avoid voluminous increase in controls.

For more information, see:

-   [Tables installed](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#) for descriptions of the common item m2m tables.
-   [Control form changes](../task/create-control-ws.md) with respect to common controls.
-   [Convert standard control to common control](../task/convert-standard-control-common.md) to add reliant entities.
-   [Action handler components](../../grc-common/reference/components-item-gen-process.md#table_cgt_f4d_ftb) for common controls.
-   [Operational changes in item generation of common controls](../../grc-common/reference/item-gen-action-types.md).
-   [Impact of common control on compliance score calculation](compliance-score-common-control.md).

