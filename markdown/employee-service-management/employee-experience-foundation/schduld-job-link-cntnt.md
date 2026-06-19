---
title: Run the scheduled job for content association
description: Change the scheduled job frequency, as required, to ensure that the notification of new content availability to add to the topic pages is regular and uninterrupted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/schduld-job-link-cntnt.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage connected content from topic pages, Taxonomy and connected content, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Run the scheduled job for content association

Change the scheduled job frequency, as required, to ensure that the notification of new content availability to add to the topic pages is regular and uninterrupted.

## Before you begin

Role required: admin

## About this task

**Surface New Unconnected Content of Categories** helps you identify the new unconnected content.

-   Use the scheduled job for manual additions and removals of content.
-   [Enable connected content autosync system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/may-system-properties-taxonomy-autosync.md) for automatic additions and removals of content.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Surface New Unconnected Content of Categories**.

2.  Select your preferred **Run** time option, for the scheduled job, from the available list on the field.

    \[Omitted image "schdled-job-runtime.png"\] Alt text: This field, Run, lists out frequency options for the scheduled job to execute periodically.

    **Note:** The default scheduled job run-time is weekly. Edit and update the frequency of execution, as required.

3.  Select **View Details** on the pop-up notification displayed on the topic page to see the new content available for association or removal..

    \[Omitted image "new-content-available.jpg"\] Alt text: The notification states new content is available for association with a link for view details.

4.  View **Associated catalog and kb categories** to see the **update type**, such as Added or Removed.

    \[Omitted image "connected-content-view-add-remove.png"\] Alt text: Associated catalog and kb categories addition and removal updates

5.  Add or dismiss content, as required, with **Update topic with content** or **Dismiss content** respectively.


**Parent Topic:**[Manage connected content from topic pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/mnge-content-topics.md)

