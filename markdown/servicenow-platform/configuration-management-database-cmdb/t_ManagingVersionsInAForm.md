---
title: Manage a filter version in a form
description: You can view and manage all versions of a filter from the Certification Filter form.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certification filters, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage a filter version in a form

You can view and manage all versions of a filter from the Certification Filter form.

## Before you begin

Role required: none

## About this task

Versions can be displayed in a list. The default list of filters displays only the active version of each filter. To see all filter versions in the list view, select **All** in the breadcrumbs.

## Procedure

1.  Open any version of a filter.

    The Other Versions related list displays all other versions of this filter, both active and inactive. The system prevents you from editing either the filter version or the record number in the list view.

2.  Click any version in the related list to display the record for that version.

3.  To make an inactive filter the current version, open the filter, edit it if desired, and then click **Revert**.

    This action:

    -   Deactivates the previous active version of the filter.
    -   Copies the inactive filter.
    -   Makes this new copy current and active.

