---
title: Define and customize activity stream tags
description: Define and customize the activity stream tags for the record pages in Service Operations Workspace. The tags helps in filtering the activity from the activity streams as required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/define-customize-activity-stream-tags.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring record pages in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Define and customize activity stream tags

Define and customize the activity stream tags for the record pages in Service Operations Workspace. The tags helps in filtering the activity from the activity streams as required.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  Search and select Service Operations Workspace.

3.  On the Service Operations Workspace UX registry record, from the UX Page Properties related list, select **activityStreamProps**.

    By default, the activity stream UX page property record contains no tag information.

4.  Edit the activity stream UX page property record.

5.  Enter the following tag information in the **Value** field to define and customize your tags.

    \[Omitted image "sow-activity-stream-props-data.png"\] Alt text: Activity stream prop UX registry record

    -   Color - Color of the tag.
    -   Icon - Icon type of the tag.
    -   Labels - Label name of the tag.
    -   Tables - Table to which the tag is applied such as incident or interaction.
    For more information on how to use the correct values to customize the tags, see [Configure tags for the Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/tags-activity-stream-admin.md).

6.  Select **Update**.


**Parent Topic:**[Configuring record pages in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configuring-record-pages-sow-itsm.md)

