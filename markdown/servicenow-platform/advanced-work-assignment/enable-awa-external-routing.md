---
title: Enable external routing for queues
description: Configure Advanced Work Assignment to route work items in the queue using external routing.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [External routing overview, Work item queues, Work items, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable external routing for queues

Configure Advanced Work Assignment to route work items in the queue using external routing.

## Before you begin

Verify that you have reviewed the functionality of external routing and configured the necessary APIs. For more information, see [External routing overview](../concept/awa-external-routing-overview.md).

Role required: awa\_external\_user

**Note:** With the installation of the External Routing Support plugin \(com.glide.awa-external\), the awa\_external\_user role is available by default.

## About this task

From Xanadu release, you can add the **External** field to the AWA queue form view. The **External** field is not available by default, but it is available with the installation of the External Routing Support plugin \(com.glide.awa-external\) in Xanadu release. The **External** field can be added to the queue UI form only when the plugin is installed in your instance.

![Queue form displaying the External field to enable third-party routing.](../image/external-routing-ui.png "External third-party routing form")

The installation of the External Routing Support plugin \(com.glide.awa-external\), adds demo data for the following:

-   An AWA External Provider \(awa\_external\_provider\).
-   A sys\_alias representing an endpoint for the external provider API.
-   A set of awa\_external\_event\_definition records demonstration reasonable payloads for each event type.

**Note:**

-   If the customer modifies the default AWA Queue form view, the **External** field is not added to the form even if the external routing plugin is installed as the installation does not override the customer configurations and it must be manually added to the form.
-   Installing AWA without this plugin still enables AWA and Agent Chat to function normally, and does not result in any errors or warning logs due to code attempting to access tables or fields that do not exist.

If External \(with external partner\) and internal AWA queues are mixed up with the respective service channel in an External Partner outbound payload-defined configuration, then a warning message is displayed.

![Warning message displayed if there is a blended configuration when external routing is enabled.](../image/extrnl-route-blend-config-warn.png "Warning Message")

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select **New** for an External Routing Queue form.

3.  Check the **External** check box to use external routing.

    **Note:**

    -   If the **External** field doesn't appear, select the update personalized list icon \(![Update personalized list icon](../../../common/image/gear.png)\) and add the **External** field to the screen.
    -   If you don't want to use external routing, clear the **External** check box.
4.  On the form, fill in the fields.

<table id="table_r24_thw_ccc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

The third-party provider for external routing.**Note:** By default, ServiceNow provides the ServiceNow Demo provider, but you can select a provider of choice.

</td></tr><tr><td>

Provider Queue ID

</td><td>

Queue ID of the external third-party provider.

</td></tr><tr><td>

Document fields to include

</td><td>

Fields of the document that the service channel is on.The work item fields that can be sent out to the external third-party. You can select the required fields.

</td></tr><tr><td>

Provider application ID

</td><td>

Unique application or integration identifier, which is used by the third-party routing system to make requests if necessary.

</td></tr></tbody>
</table>5.  Select **Submit**.


**Parent Topic:**[External routing overview](../concept/awa-external-routing-overview.md)

