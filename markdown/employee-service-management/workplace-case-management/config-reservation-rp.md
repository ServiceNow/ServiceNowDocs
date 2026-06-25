---
title: Configuring a record producer for reservation
description: Configure a record producer to integrate it with Workplace Reservation Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/config-reservation-rp.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configuring a record producer for reservation

Configure a record producer to integrate it with Workplace Reservation Management.

Integrating a record producer with Workplace Reservation Management provides administrators with flexible choices to handle service requests. If a record producer is mapped to the **Record producer for reservation** field in a workplace service, it’s displayed to users during the reservation process. If no record producer is mapped, the system displays a custom widget for service item requests.

**Note:**

Some fields or minor functionality can differ between cases submitted for additional services of a reservation and standalone cases. While the fulfillment experience for both cases is similar, it is not completely the same because they serve different purposes.

For example, while reserving a room with a projector from 10:00 to 11:00, the preparation and cleanup time is applicable to set up and remove the projector. If the preparation and cleanup duration is 30 minutes each, the room is reserved from 9:30 to 11:30. For standalone cases, users can raise a request at any time. The request doesn't need a start time and end time, therefore, preparation and cleanup time aren't applicable.

The dual approach with a record producer and a custom widget provides a streamlined and unified experience:

-   Using a record producer automatically populates and hides fields with known data from the reservation context like requested for, date and time, space details. It makes sure that users only provide the necessary information, simplifying the process and improving data accuracy.
-   Using the custom widget maintains backward compatibility for workplace services that don't have a record producer.

## Enabling a record producer for editing

You must first create a record producer on the Workplace Case or Workplace Case Extension tables and configure it for editing. For more information, see [Configuring a record producer for request edit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/config-case-edit-rp.md).

For more information about creating a record producer, see [Configure a Record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/wsd-create-record-producer.md).

While creating the record producer, make sure that you follow these steps.

**Important:** If you don't follow these steps, the record producer doesn't load correctly on the reservation portal.

-   You must use the `Workplace Service widget Variable set` in your record producer to ensure that space selection and service item selection widgets are included and function correctly.

    The variable set includes the following widgets:

    -   WSD Multilevel Space Picker: The widget used to select building, floor, and space information.
    -   WSD Workplace Service: The widget used to select specific service items.
-   You must adhere to specific names for the variables so the system can automatically pass data from the reservation to your record producer. These variables are populated with known data from the reservation and are typically hidden on the form.

    Make sure that you use the specified names for the following variables.

    -   **Requested for**: requested\_for
    -   **Date and time requested by**: delivery\_time
    -   **Urgency**: urgency
    -   **Impact**: impact
    **Note:** Ensure that you include a record producer variable with the field name `reservation`. Otherwise, the reservation case isn't linked to the child case generated.

-   Sections like request details and space selection are hidden on the request form as they’re derived from the reservation data. For more information, refer to any record producers installed with Workplace Case Management, like `Catering`.


## Mapping the record producer to the reservation page

To map the record producer to the reservation page, you must first add it to the **Record producer** field of the workplace service. You must then add it to the **Record producer for reservation** field of the same workplace service.

For more information about the fields of a workplace service, see [Workplace Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-service-form.md).

**Parent Topic:**[Configuring Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Create a Workplace task template]()

[Smart Assessment for Workplace Case and Task]()

[Automating seat assignment for new hires]()

[Configure Approval options]()

[Configure a Record producer]()

[Configuring a record producer for request edit]()

[Create an SLA Definition]()

[Create a Workplace service]()

[Add a workplace service item to a workplace service]()

[Create a workplace template configuration]()

[Create a workplace field mapping]()

[Configure an escalation rule]()

[Add Fulfillment instructions]()

[Group similar workplace cases under a parent case]()

