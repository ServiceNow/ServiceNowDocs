---
title: Deactivate an issue workflow
description: Stop an active workflow from being evaluated for new issues on its table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/deactivate-an-issue-workflow.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Deactivate an issue workflow

Stop an active workflow from being evaluated for new issues on its table.

## Before you begin

The workflow must be active.

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

Deactivating a workflow does not delete it. You can activate the workflow again later. See [Review and activate a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-activate-a-workflow.md).

Existing issues that are already associated with the workflow continue to use it and aren't affected by deactivation. Deactivation only prevents the workflow from being evaluated for new issues.

**Important:**

If this workflow has no trigger condition and the lowest priority number on its table, it acts as the catch-all for that table. Deactivating it removes that catch-all coverage. New issues on the table are then evaluated against the next active workflow in priority order, or fall back to existing issue behavior if none match. The system does not warn you before deactivation.

## Procedure

1.  Navigate to **All** &gt; **GRC Issue Administration** &gt; **Issue Workflows**.

2.  Open the workflow that you want to deactivate.

3.  Select **Deactivate workflow**.


## Result

The workflow status changes to Inactive. The workflow is no longer evaluated for new issues on its table.

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

