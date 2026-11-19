---
title: Preview and test a Lifecycle Events case
description: Preview and test a Lifecycle Events case for different audience types. You can preview a Lifecycle Events case to validate the activities that trigger for a particular audience. You can then create a test Lifecycle Events case for different users and select which activities to include or exclude in your test.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/lifecycle-events/test-lifecycle-event.html
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the Test Activity Sets tool for a lifecycle event activity set, Building a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Preview and test a Lifecycle Events case

Preview and test a Lifecycle Events case for different audience types. You can preview a Lifecycle Events case to validate the activities that trigger for a particular audience. You can then create a test Lifecycle Events case for different users and select which activities to include or exclude in your test.

## Before you begin

Role required: sn\_hr\_le.admin

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**, and open a record.

2.  Click the **Activity Sets** tab to access the lifecycle event builder.

3.  Select the **Test Activity Sets** icon.

    \[Omitted image "test-lifecycle-event-icon.png"\] Alt text: Open the Test side panel in the Manage Lifecycle Event page.

    The Test side panel appears.

4.  In the **Test** side panel, use the **Subject person** field to select a subject person.

    **Note:** To select a subject person based on audience criteria, select **Advanced Search** to find and select a user based on the criteria you specify.

    \[Omitted image "test-lifecycle-event-side-panel.png"\] Alt text: In the Test side panel, select a subject person for the test and whether to include the inapplicable or indeterminate activities in the test.

5.  Select the **Show inapplicable activities and sets** button to show all activities and activity sets that are not applicable for the subject person.

6.  Select the **Show indeterminate activities and sets** button to show all activities and activity sets that can’t be determined for the subject person.

7.  Select **Preview** to preview the workflow.

8.  Select **Test** to create a Lifecycle Events case based on the workflow that you previewed.

    A Lifecycle Events case for the subject person you selected is created.


**Parent Topic:**[Using the Test Activity Sets tool for a lifecycle event activity set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/lifecycle-events/hr-lifecycle-event-test-tool.md)

