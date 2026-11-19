---
title: Delete a CI relationship
description: Maintain the integrity of the CMDB by deleting any CI relationships that are no longer relevant or needed for a CI. Use the relationship editor to delete CI relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/delete-ci-relationship.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CI relationship editor, CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Delete a CI relationship

Maintain the integrity of the CMDB by deleting any CI relationships that are no longer relevant or needed for a CI. Use the relationship editor to delete CI relationships.

## About this task

As an alternative to the CI relationship editor, [Unified Map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/unified-map/cmdb-workspace-unified-map.md) in the [CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md) provides the latest functionality for editing CI relationships. For more information, see [Edit relationships in Unified Map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/unified-map/unified-map-edit-connection.md).

## Before you begin

Role required: ITIL or asset

**Note:** Deleting a relationship to a dependent CI can result in identification problems as the dependent CI will no longer have a relationship to the CI it depends on.

## Procedure

1.  Launch the relationship editor:

    1.  Open the CI form of the CI for which you want to delete a relationship.

    2.  Locate the **Related Items** section near the center of the form.

    3.  Click the plus \(+\) icon on the **Related items** section.

2.  In the Relationship Editor, in the Relationships section, select the relationships that you want to delete for the CI.

3.  Click the **Delete selected relationships** icon.

4.  Click **Save** or **Save and Exit**.


**Parent Topic:**[CI relationship editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_RelationshipEditor.md)

