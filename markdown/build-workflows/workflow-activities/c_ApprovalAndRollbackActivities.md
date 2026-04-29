---
title: Approval and rollback workflow activities
description: Approval and rollback activities generate and manage approvals.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Approval and rollback workflow activities

Approval and rollback activities generate and manage approvals.

Approval and rollback activities are not available in some workflows.

-   With two exceptions, approval and rollback activities are only available when the workflow runs on a table that extends Task. The exceptions are the [**Approval - User**](https://www.servicenow.com/docs/access?context=r_ApprovalUser&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [**Approval Action**](https://www.servicenow.com/docs/access?context=r_ApprovalAction&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) activities, which are available globally.
-   Approval and rollback activities are available only if approval engines are turned off for the table on which the workflow runs. If approval engines are enabled for the table, approval activities appear greyed out and cannot be selected. To learn more about how workflow and approval engines interact, read [Approval workflow activities and approval engines](../../using-workflows/concept/wf-approvals-n-rollbacks.md#).

