---
title: Decorations
description: Reference decorations are icons that appear next to a reference field on a form, providing quick access to related records and actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/c\_Decorations.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 1
breadcrumb: [Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Decorations

Reference decorations are icons that appear next to a reference field on a form, providing quick access to related records and actions.

Four decoration types can appear next to a reference field. Each decoration serves a distinct purpose and appears under different conditions.

-   **Reference lookup**

    Appears next to editable reference fields. Selecting the reference lookup icon opens a list of records from the referenced table, letting you select a record to populate the field. For more information, see [Reference lookup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceLookup.md).

-   **Reference icon**

    Appears next to populated reference fields. Selecting the reference icon opens a read-only preview of the referenced record. Select **Open Record** in the preview to navigate to the full record. For more information, see [Reference field icon](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceIcon.md).

-   **Related incidents icon**

    Displays incidents related to the record referenced in the field. This decoration requires a dictionary attribute and is not enabled by default. For configuration instructions, see [Configure the related incidents icon](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ConfigureRelatedIncidentsIcon.md).

-   **Show workflow icon**

    Appears next to a workflow field and opens the related workflow in the Workflow Editor. This decoration requires a dictionary attribute and is not enabled by default. For configuration instructions, see [Configure the show workflow icon](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ConfigureShowWorkflowIcon.md).


The reference lookup icon is visible whenever the reference field is editable. Other decorations appear only after a record is selected in the field.

