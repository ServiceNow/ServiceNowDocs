---
title: Extension points for batch processing in Service Operations Workspace
description: Use the implementation extension point to create implementations and execute batch processing to update multiple records, which improves the performance of the system.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Extension points for batch processing in Service Operations Workspace

Use the implementation extension point to create implementations and execute batch processing to update multiple records, which improves the performance of the system.

The Multiple Record Associator \(MRA\) component enables you to create implementation extension points for batch processing of multiple records.

To view the extension points that are available by default, navigate to **All** &gt; **System Extension Points ** &gt; **Scripted Extension Points**. You can select the **Create implementation** option to create an implementation extension point.

When you have multiple records to update, a business rule executes and updates once for each record, which can affect the performance of the system. Instead of executing the business rule for each record, you can use the `RelatedListIncidentItemUpdateHandler` script include to execute batch processing for updating multiple records.

You can use the `RelatedListIncidentItemUpdateHandler` script include to update multiple records with batch processing. For example, you could use this script include when associating and updating multiple child incidents with a parent incident.

The **RelatedListIncidentItemUpdateHandler** script include contains the `global.RelatedListItemUpdateHandler` implementation extension point and is used when batch processing multiple records on a related list.

The extension point used in the **related\_list\_edit\_helper** script include uses API to facilitate invoking custom code. This extension point overrides the execution of the business rule to ensure that the implementation extension point is executed when updating multiple records instead of the business rule. You can also add a business rule that must be overridden. When multiple records are updated, this script include is triggered, and batch processing occurs that bypasses that business rule.

The `RelatedListIncidentItemUpdateHandler` script include contains the following functions:

-   Initialize – Executes before multiple records are updated.
-   Post update – Executes after multiple records are updated.

![RelatedListIncidentItemUpdateHandler script includes](../image/related_list_handler_scriptinclude.png)

**Parent Topic:**[Service Operations Workspace for ITSM reference](../concept/sow-reference.md)

**Related topics**  


[Service Operations Workspace for ITSM data model](sow-itsm-data-model.md)

[Components installed with Service Operations Workspace ITSM Applications](components-installed-with-sow.md)

[Components installed with Agent Client Collector for Investigation](components-installed-investigate.md)

[Components installed with Microsoft Endpoint Configuration Manager for Investigation](components-installed-mecm-adapter.md)

[Components installed with Remedial Actions Framework](components-installed-with-remediation-fw.md)

[Components installed with Metrics and CI Actions Framework](components-installed-metrics-ci-action-fw.md)

[Recommendation rules for an incident in Service Operations Workspace](recommendation-rules.md)

[Recommended Actions for ITSM reference](../concept/recommended-actions-for-itsm-reference.md)

[Reference section for Problem Management in Service Operations Workspace](../concept/reference-problem-management-sow.md)

[Features of the Investigation tab](features-of-investigation-tab.md)

[Quick start tests for Incident Management in Service Operations Workspace](../../../administer/atf-quick-start-tests/reference/quick-start-tests-im-sow.md)

[Components installed with Universal Request for Service Operations Workspace](components-installed-ur-sow.md)

[Components installed with Universal Task for Service Operations Workspace](components-installed-ut-sow.md)

[Password Reset Reference](pr-sow-reference.md)

