---
title: Email notifications for pipeline projects
description: Sourcing managers receive email notifications when a pipeline project is created automatically, and before its estimated start and end dates.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sourcing Pipeline Management, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Email notifications for pipeline projects

Sourcing managers receive email notifications when a pipeline project is created automatically, and before its estimated start and end dates.

The email notification includes the **View pipeline project** option that navigates the sourcing manager to the Source-to-Pay Workspace View, where they can access the pipeline project's **Overview** tab.

## System properties for Sourcing Pipeline Management

The following system properties are used by Sourcing Pipeline Management to notify sourcing managers about upcoming pipeline project deadlines.

<table id="table_ywx_c1g_zfc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_spend\_pipeline.days\_before\_start.notification

</td><td>

Number of days before the estimated start date to trigger an email to the sourcing manager if the project is not in Work in Progress, Closed Complete, or Closed Canceled state.

</td></tr><tr><td>

sn\_spend\_pipeline.days\_before\_end.notification

</td><td>

Number of days before the estimated end date to trigger an email to the sourcing manager if the project is not in Closed Complete or Closed Canceled state.

</td></tr></tbody>
</table>**Note:** You must have the sn\_spend\_pipeline.pipeline\_management\_admin role to update the **Value** field in the system properties. The **Value** field defines the number of days before sending a notification email to the sourcing manager.

To access these properties, navigate to **All** and enter `sys_properties_list.do` in the application navigator. In the **Name** search field, enter the property name to locate it.

-   **Scheduled jobs**

    Sourcing and Pipeline Management includes the following scheduled jobs for sending email notifications:

    -   Trigger Pipeline Start Notification
    -   Trigger Pipeline End Notification
-   **Business rules**

    Sourcing and Pipeline Management includes the `Trigger pipe end or start notification` business rule, which runs in the following scenarios:

    -   When a pipeline project's estimated start date exceeds the value specified in the system property, the Trigger pipe end or start notification business rule runs. This business rule immediately sends email notifications to sourcing managers to keep them informed about project timelines. Email notifications are sent only for pipeline projects in the Draft or Planned state.
    -   When a pipeline project's estimated end date exceeds the value specified in the system property, the Trigger pipe end or start notification business rule runs. It immediately notifies sourcing managers via email. Email notifications are sent only for pipeline projects that are not in the Closed Complete or Closed Canceled state.

**Parent Topic:**[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

