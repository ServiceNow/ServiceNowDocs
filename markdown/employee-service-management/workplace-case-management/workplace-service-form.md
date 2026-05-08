---
title: Workplace Service form
description: Use the Workplace Service form to specify details such as the case table, default template, and record producers.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Workplace Service form

Use the Workplace Service form to specify details such as the case table, default template, and record producers.

<table id="table_ews_1x4_smb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service name

</td><td>

Enter a name for the Workplace service.

</td></tr><tr><td>

Case table

</td><td>

Table that is used for the workplace service.

</td></tr><tr><td>

Fulfillment type

</td><td>

Fulfillment type for the workplace service. You can select one of the following values:-   **Manual**: Select this option for manual fulfillment. This option enables you to fulfill the request with a human response.
-   **Service activity**: Select this option to trigger activities to fulfill the workplace service. Save the form to create or update workplace service activities. For more information, see [Create a Workplace service activity](../task/create-workplace-service-activity.md)
-   **Flow**: Select this option to use an existing subflow from the application for fulfillment. For more information about Flows, see Create a subflow.

**Note:** If you are creating a custom subflow, ensure that the input fields are set to following:

    -   Label: Workplace Case
    -   Name: workplace\_case
    -   Type: Reference.Workplace Case

</td></tr><tr><td>

Automatically close case

</td><td>

Option to close the case automatically if the service activities are closed.This field appears if you select the **Fulfillment type** as **Service Activity**.

</td></tr><tr><td>

Flow

</td><td>

Flow that is used for the workplace service.This field appears if you select the **Fulfillment type** as **Flow**.

</td></tr><tr><td>

Default template

</td><td>

Case template for the workplace service. For more information on templates, refer to [Case and Task Templates](../concept/wsd-templates.md).

</td></tr><tr><td>

Reinitiate activities on updates

</td><td>

Option to close all child tasks and create them again when a user modifies the workplace service items of a case.If this option is not selected, the requested item record is updated and only the child tasks that have changes are cancelled and created again. Child tasks that are already closed are not created again.

If a user modifies the location, date, time, or any other request data, all the child tasks are re-initiated, even if this field is not selected.

Selecting this field is helpful if you have service activities like approvals, which must be completed before other activities.

</td></tr><tr><td>

Application

</td><td>

Application that the workplace service is created for.

</td></tr><tr><td>

Active

</td><td>

Option to activate the workplace service.

</td></tr><tr><td>

Available for

</td><td>

Option to specify where the workplace service is available.-   **Case**: Select this option to make the workplace service available only to Workplace Case Management users.
-   **Reservation**: Select this option to make the workplace service available for employees while making a reservation.
-   **Case and Reservation**: Select this option to make the workplace service available to both Workplace Case Management users and to employees making a reservation.

**Note:** The **Reservation** and **Case and Reservation** options appear only if the Workplace Reservation Management application is installed.

</td></tr><tr><td>

Allow request modifications for

</td><td>

Option to specify where users can modify the workplace service requests.You can select the **Case**, **Reservation**, or both options based on your requirement.

This field is only available for the sn\_wsd\_case.admin role.

</td></tr><tr><td>

Allow request modifications

</td><td>

Option to enable modifications of the workplace service requests.This field is available from Workplace Case Management 1.23.1.

</td></tr><tr><td>

Record producers

</td><td>

Record producer through which users can request the workplace service. You can select one or more record producers for a workplace service. The record producer must be created in the Workplace Case Management application.

</td></tr><tr><td>

Record producer for reservation

</td><td>

Record producer to be used while adding extra services to a reservation.

 This field appears only if the value of the **Available for** field contains reservation.

 If this field is empty, a generic interface is used while adding or editing extra services for a reservation.

 If services are added using a record producer, the same record producer is used while editing the service till all the items are fulfilled. If the record producer is changed or removed before the items are fulfilled, the earlier record producer is still used while editing the services.

 If the selected record producer is deleted or made inactive, users will see an error while editing the service items. Users must then contact the administrator or case manager to update the services.

</td></tr><tr><td>

Short description mapping

</td><td>

Record producer field that is used for the short description of the workplace service.This field appears after a record producer is selected for the workplace service.

</td></tr><tr><td>

Allow only single service item selection

</td><td>

Option to restrict users to select only one option within a category from a list of choices.**Note:** This field appears only if Workplace Reservation Management application is installed.

</td></tr><tr><td>

Description

</td><td>

Description about the workplace service that explains the purpose of the workplace service. You can add HTML text or regular text as the description.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Case Management references](../concept/workpalce-case-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Case Management](components-installed-with-workplace-case-mgmt.md)

[Properties installed with Workplace Case Management](properties-installed-with-workplace-case-mgmt.md)

[Workplace Location Assignment service](location-assignment-service.md)

