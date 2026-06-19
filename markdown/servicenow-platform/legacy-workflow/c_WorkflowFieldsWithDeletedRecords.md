---
title: Workflow fields with deleted records
description: Workflow fields may indicate when a record required by the workflow is deleted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/legacy-workflow/c\_WorkflowFieldsWithDeletedRecords.html
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow stages, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow fields with deleted records

Workflow fields may indicate when a record required by the workflow is deleted.

After a referenced record is deleted, the reference in the primary record is no longer valid. If the stage renderer detects a reference that is no longer valid, the stage field displays a message about the deleted record.

Administrators can restore deleted records. For more information, see Use the Deleted Records module to restore a deleted record.

\[Omitted image "600pxWFRenderMissingrecordEdited.png"\] Alt text:

The image shows a list with two workflows. The top request does not have an associated request item. The bottom request has an associated request item, but the item does not have an associated workflow context.

**Parent Topic:**[Workflow stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/legacy-workflow/c_WorkflowStages.md)

