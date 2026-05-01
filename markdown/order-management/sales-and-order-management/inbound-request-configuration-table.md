---
title: Inbound Request Configuration
description: Enables you to define the configurations to determine how each flow is processed and tracked within an Inbound Request.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Inbound Request, Sales and Service API Core, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Inbound Request Configuration

Enables you to define the configurations to determine how each flow is processed and tracked within an Inbound Request.

## Overview of the Inbound Request Configuration table

The Sales and Service Core API \(com.sn\_tmt\_core\) plugin is required to use the Inbound Request Configuration table \(sn\_tmt\_core\_inbound\_queue\_config\).

The Inbound Request Configuration table is a metadata table that must be configured to decide how a particular flow is executed, whether synchronous or asynchronous.

The table can be used to perform the following tasks.

-   Enable admins to configure synchronous vs asynchronous processing of requests.
-   Adapt the Sales Customer Relationship Management Request Tracker across all CRM flows.
-   Enable configuration of notification types, whether default, custom, or no notifications.

The **Request Configuration** field on the existing Inbound Request Table \[sn\_tmt\_core\_inbound\_queue\] is a reference to the new Inbound Request Configuration table \(sn\_tmt\_core\_inbound\_queue\_config\).

Any workflow that requires the tracking of a completion status, can use the Inbound Request Configuration table and configure whether a flow is synchronous or asynchronous.

## Fields on the Inbound Request Configuration Table

An admin creates a record in the table and specifies the configuration using the **run\_mode**, **trigger\_notification**, and **configuration\_api** fields.

<table id="table_f3d_3tv_1fc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td>

Config ID

</td><td>

Unique configuration ID for the metadata configuration.

</td><td>

String

</td></tr><tr><td>

Label

</td><td>

Unique label name for the metadata configuration.

</td><td>

Translated text

</td></tr><tr><td>

Active

</td><td>

Specifies whether the Inbound request configuration record is active or not.

</td><td>

True/False Default value is **False**

</td></tr><tr><td>

Run Mode

</td><td>

Specifies whether a request runs synchronously or asynchronously.

</td><td>

String \(choices\): **Sync**, **Async**, **Advanced**.-   Synchronous: Synchronous processing.
-   Asynchronous: Asynchronous processing
-   Advanced: Use custom script to determine if the flow has to be synchronous or asynchronous

</td></tr><tr><td>

Trigger Notification

</td><td>

Specifies how you want to receive notifications.A notification is triggered in one of the following situations.

-   **Trigger notification** field is set to **Default**.
-   State of a request is **Complete** and the status is either **Success** or **Partial success**.

The notifications for the record in the Inbound table are only received by whoever has initiated the flow.

</td><td>

String \(choices\): None, Default, Custom-   None: No notifications
-   Default: Notifications only for asynchronous requests.
-   Custom: Custom notification for asynchronous requests based on requirements.

Configure custom notifications by using the existing event \(sn\_tmt\_core.ibq.custom.notification\) or by handling your own custom event.

Default value for the field is **Default**.


</td></tr><tr><td>

Configuration API

</td><td>

Script required to process the inbound request.To learn more about the configuration API, see [IBQConfigBase API - Scoped](https://www.servicenow.com/docs/access?context=IBQConfigBaseAPIBoth&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td><td>

Reference: sys\_script\_include

</td></tr><tr><td>

Domain

</td><td>

The current domain scope of the record, for example global.

</td><td>

Domain ID

</td></tr></tbody>
</table>## Security roles

The security roles for the Inbound Request Configuration table \(sn\_tmt\_core\_inbound\_queue\_config\) provide different levels of access to the \[sn\_tmt\_core.inbound\_queue\_admin\] role.

|Role|Access|
|----|------|
|sn\_tmt\_core.inbound\_queue\_admin|Create, read, update, delete, report\_view, report\_on|

**Note:** Add a user with the roles sn\_tmt\_core.admin or sn\_tmt\_core.inbound\_queue\_admin, who is responsible for configuring the Inbound Request Configuration table, as a delegated developer for the application where the configuration is being created. Assign the permission “Manage Update Set” \(added under Manage Developers for the respective application\). This ensures that all changes are captured in the correct scope and update sets. For details, see [Exploring Delegated Development](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Related topics**  


[IBQConfigBase API - Scoped](https://www.servicenow.com/docs/access?context=IBQConfigBaseAPIBoth&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

