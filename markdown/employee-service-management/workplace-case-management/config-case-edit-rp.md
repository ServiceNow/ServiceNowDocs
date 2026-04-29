---
title: Configuring a record producer for request edit
description: Configure a record producer for editable workplace service requests.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configuring a record producer for request edit

Configure a record producer for editable workplace service requests.

The request edit feature in Workplace Service Delivery lets users modify the details of their submitted requests. Cases that are created with record producers on the Workplace Case or Workplace Case Extension tables can be edited, keeping records current and accurate.

To configure the edit functionality of a record producer, follow the steps in the following sections.

## Creating a record producer

You must first create a record producer on the Workplace Case or Workplace Case Extension tables, then map it to the **Record Producer** field of a Workplace Service. For more information about creating a record producer, see [Configure a Record producer](../task/wsd-create-record-producer.md).

If you want to integrate the record producer with Workplace Reservation Management, see [Configuring a record producer for reservation](config-reservation-rp.md).

## Enabling the edit functionality

You can enable the button by selecting `Case` or `Case and Reservation` in the **Available for** field, then selecting the **Allow request modifications** field of the workplace service.

When the **Allow request modifications** option is enabled on a workplace service, users see the **Edit request** action in the request summary page for all the record producers associated with that service.

For more information about the fields of a workplace service, see [Workplace Service form](../reference/workplace-service-form.md).

## Redirecting to the Case Editor page

When users select the edit request option for their request, they’re redirected to the WSD Case Editor page, which looks like the record producer to provide a familiar interface for users.

After making their changes, users can save the updated case, which makes the following changes:

-   The Workplace Case record is updated with the new values provided by the user.
-   New service item requests are created based on the updated case information, if necessary.

## Configuring the record producer for editing

-   **Handling variables with default values on load**

    Condition

    Variables that have default values on load can cause data inconsistency on the edit page. The edit page must fill variables based on the submitted request.

    For example, the system tries to populate the logged-in user in the Requested for field instead of picking the data from the submitted request.

    Remedy

    While setting the default value for any variable, ensure that it only applies to the new request submission. You can use the `id` parameter from the page URL in the client scripts to determine whether it’s a request submission page or an edit page.

    For more information, refer to any record producers installed with Workplace Case Management, like `Catering`.

-   **Triggering an event on submission**

    For the edit page, you must trigger the `wsd.serviceEditor.onSubmit.success` event in the `onSubmit` catalog client script \(last executable script\) of the record producer with the parameter `success: true`. Ensure that the last executable client script has the **UI type** field set to `All`.

    Triggering the event makes sure that all the onSubmit client scripts are validated and that the updated variable data can be used to update the case record.

    For more information, refer to any record producers installed with Workplace Case Management, like `Catering`.

-   **Using custom widgets in the record producer**

    Condition

    To use custom widgets in the record producer, ensure that the widget can pre-fill data based on the submitted request. The reference for the widget can be taken from the Workplace Service widget.

    Remedy

    Ensure that if you are on the edit page, you can use the `sys_id` parameter from the URL to get the sys\_id of the submitted request. Use the sys\_id to retrieve the case data and populate the existing data on the widget during the first load.

    Alternatively, you can use the following variable sets that are installed with Workplace Case Management:

    -   For both item and space selection in the request, use the `Workplace Service widget Variable set`.
    -   For only space selection, use the `Multilevel space picker widget variable set`.

**Parent Topic:**[Configuring Workplace Case Management](workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](../task/install-workplace-case-mgmt.md)

[Create a Workplace case template](../task/wsd-case-template.md)

[Create a Workplace task template](../task/wsd-task-template.md)

[Smart Assessment for Workplace Case and Task](../task/smart-assessment-for-workplace-case-and-task.md)

[Automating seat assignment for new hires](auto-assign-new-hires.md)

[Configure Approval options](../task/config-approval-optns.md)

[Configure a Record producer](../task/wsd-create-record-producer.md)

[Configuring a record producer for reservation](config-reservation-rp.md)

[Create an SLA Definition](../task/create-sla-defn-case-mgmt.md)

[Create a Workplace service](../task/create-workplace-service.md)

[Add a workplace service item to a workplace service](../task/add-workplace-service-items.md)

[Create a workplace template configuration](../task/create-workplace-template-confguration.md)

[Create a workplace field mapping](../task/create-workplace-field-mapping.md)

[Configure an escalation rule](../task/configure-escalation-rule.md)

[Add Fulfillment instructions](../task/add-fulfillment-instructions.md)

[Group similar workplace cases under a parent case](../task/group-similar-workplace-cases.md)

