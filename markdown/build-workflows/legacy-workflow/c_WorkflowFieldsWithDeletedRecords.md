---
title: Workflow fields with deleted records
description: Workflow fields may indicate when a record required by the workflow is deleted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/legacy-workflow/c\_WorkflowFieldsWithDeletedRecords.html
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workflow stages, Workflow management, Classic Workflow, Build workflows]
---

# Workflow fields with deleted records

Workflow fields may indicate when a record required by the workflow is deleted.

After a referenced record is deleted, the reference in the primary record is no longer valid. If the stage renderer detects a reference that is no longer valid, the stage field displays a message about the deleted record.

Administrators can restore deleted records. For more information, see Use the Deleted Records module to restore a deleted record.

\[Omitted image "600pxWFRenderMissingrecordEdited.png"\] Alt text:

The image shows a list with two workflows. The top request does not have an associated request item. The bottom request has an associated request item, but the item does not have an associated workflow context.

**Parent Topic:**[Workflow stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/c_WorkflowStages.md)

