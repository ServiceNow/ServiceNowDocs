---
title: Run the scheduled job for outdated content
description: Auto-delete the outdated content by marking the schedule job active. Once the schedule job is active, all the outdated content is removed automatically.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage outdated connected content, Taxonomy and connected content, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Run the scheduled job for outdated content

Auto-delete the outdated content by marking the schedule job active. Once the schedule job is active, all the outdated content is removed automatically.

## Before you begin

Role required: admin

## About this task

Reduce maintenance overhead with the scheduled job or alternatively [Manage outdated connected content](may-manage-outdated-content-topics.md) manually.

-   Run the cleanup at a regular interval with a scheduled job.
-   Send email notifications to taxonomy admins about the cleanup.
-   Auto-delete the invalid and outdated content for performance improvement.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Automated Outdated Connected Content Cleanup**.

2.  Mark the state to **Active**.

    **Note:** By default, schedule job is **inactive**.

3.  Select your preferred **Run** time option, for the scheduled job, from the available list on the field.

    **Note:** The default scheduled job run-time is monthly. Edit and update the frequency of execution, as required.


## Result

When the job is complete, the taxonomy admins receive the following email notification with the subject line **Cleanup of Outdated Connected Content** along with the details indicating the total items removed, if any.

![image.outdated-cleanup-email]

When a category has outdated data, that data isn't associated with the topic.

**Note:** When you delete, only the association with the topic and taxonomies is removed. The actual catalog item or the knowledge article is not deleted.

**Parent Topic:**[Manage outdated connected content](may-manage-outdated-content-topics.md)

