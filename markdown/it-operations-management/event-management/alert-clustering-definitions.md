---
title: Create an alert clustering definition
description: Define alert clustering conditions to trigger one or more alert clustering tags, which help create alert groups from fewer alerts. Creating alert groups from fewer alerts reduces noise, making it easier to identify critical incidents, prioritize responses, and manage issues effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/alert-clustering-definitions.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tag cluster alert grouping, Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an alert clustering definition

Define alert clustering conditions to trigger one or more alert clustering tags, which help create alert groups from fewer alerts. Creating alert groups from fewer alerts reduces noise, making it easier to identify critical incidents, prioritize responses, and manage issues effectively.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

To create a tag definition, users need to use a filter to define which alerts the definition will apply to. They then define a grouping criteria by specifying which field values should be compared to create a group.

**Note:** To group alerts using tag-based grouping, create a grouping automation in Service Operations Workspace. For more information, see [Create Group automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/group-alert-sow-itom.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Tag Based Alert Clustering Engine** &gt; **Alert Clustering Definitions**.

2.  Select **New**.

3.  Configure the fields on the [Event Management tag based alert grouping definition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/tag-based-alert-clustering-definition-form.md).

4.  Select **Save**.

    The definition appears in the Tag Based Alert Clustering Definitions table.


