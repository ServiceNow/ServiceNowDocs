---
title: Configuring a record producer for reservation
description: Configure a record producer to integrate it with Workplace Reservation Management.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configuring a record producer for reservation

Configure a record producer to integrate it with Workplace Reservation Management.

Integrating a record producer with Workplace Reservation Management provides administrators with flexible choices to handle service requests. If a record producer is mapped to the **Record producer for reservation** field in a workplace service, it’s displayed to users during the reservation process. If no record producer is mapped, the system displays a custom widget for service item requests.

The dual approach with a record producer and a custom widget provides a streamlined and unified experience:

-   Using a record producer automatically populates and hides fields with known data from the reservation context like requested for, date and time, space details. It makes sure that users only provide the necessary information, simplifying the process and improving data accuracy.
-   Using the custom widget maintains backward compatibility for workplace services that don't have a record producer.

## Enabling a record producer for editing

You must first create a record producer on the Workplace Case or Workplace Case Extension tables and configure it for editing. For more information, see [Configuring a record producer for request edit](config-case-edit-rp.md).

For more information about creating a record producer, see [Configure a Record producer](../task/wsd-create-record-producer.md).

While creating the record producer, make sure that you follow these steps.

**Important:** If you don't follow these steps, the record producer doesn't load correctly on the reservation portal.

-   You must use the `Workplace Service widget Variable set` in your record producer to ensure that space selection and service item selection widgets are included and function correctly.

    The variable set includes the following widgets:

    -   WSD Multilevel Space Picker: The widget used to select building, floor, and space information.
    -   WSD Workplace Service: The widget used to select specific service items.
-   You must adhere to specific names for the variables so the system can automatically pass data from the reservation to your record producer. These variables are populated with known data from the reservation and are typically hidden on the form.

    Make sure that you use the specified names for the following variables:

    -   **Requested for**: requested\_for
    -   **Date and time requested by**: delivery\_time
    -   **Urgency**: urgency
    -   **Impact**: impact
    **Note:** Ensure that you include a record producer variable with the field name `reservation`. Otherwise, the reservation case isn't linked to the child case generated.

-   Sections like request details and space selection are hidden on the request form as they’re derived from the reservation data. For more information, refer to any record producers installed with Workplace Case Management, like `Catering`.


## Mapping the record producer to the reservation page

To map the record producer to the reservation page, you must first add it to the **Record producer** field of the workplace service. You must then add it to the **Record producer for reservation** field of the same workplace service.

For more information about the fields of a workplace service, see [Workplace Service form](../reference/workplace-service-form.md).

**Parent Topic:**[Configuring Workplace Case Management](workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](../task/install-workplace-case-mgmt.md)

[Create a Workplace case template](../task/wsd-case-template.md)

[Create a Workplace task template](../task/wsd-task-template.md)

[Smart Assessment for Workplace Case and Task](../task/smart-assessment-for-workplace-case-and-task.md)

[Automating seat assignment for new hires](auto-assign-new-hires.md)

[Configure Approval options](../task/config-approval-optns.md)

[Configure a Record producer](../task/wsd-create-record-producer.md)

[Configuring a record producer for request edit](config-case-edit-rp.md)

[Create an SLA Definition](../task/create-sla-defn-case-mgmt.md)

[Create a Workplace service](../task/create-workplace-service.md)

[Add a workplace service item to a workplace service](../task/add-workplace-service-items.md)

[Create a workplace template configuration](../task/create-workplace-template-confguration.md)

[Create a workplace field mapping](../task/create-workplace-field-mapping.md)

[Configure an escalation rule](../task/configure-escalation-rule.md)

[Add Fulfillment instructions](../task/add-fulfillment-instructions.md)

[Group similar workplace cases under a parent case](../task/group-similar-workplace-cases.md)

