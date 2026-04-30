---
title: Make a visitor registration
description: Pre-plan your visitor or off-site colleagues visit. Specify their visit details like date, time, location, and more.
locale: en-US
release: xanadu
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Registering a visitor, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Make a visitor registration

Pre-plan your visitor or off-site colleagues visit. Specify their visit details like date, time, location, and more.

## Before you begin

**Important:** Starting with Workplace Core \(sn\_wsd\_core\) version 2.1, all updates, and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal on Workplace Core \(sn\_wsd\_core\) beginning with version 2.1. To configure the Workplace service catalog in the Service Portal, see [Configure a catalog in Service Portal](https://www.servicenow.com/docs/access?context=associate-portal-catalog&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Role required: sn\_wsd\_core.workplace\_user

## About this task

Submit this request to register a guest. Specify if there are any additional requirements for the visit as a private note to the reception staff.

Workplace Visitor Management admin and reception staff can also register visitors directly from the application. Navigate to **Workplace Visitor Management** &gt; **Reception Staff** &gt; **Register Visitors**.

You can also register a visitor using the Virtual agent chat support. Navigate to **Workplace Core** &gt; **Workplace service portal** &gt; **Workplace Service Portal Home** and select the chat icon \(![Chat icon.](../../wsd-reservation-management/image/chat-icon.png)\). Enter your question or select **Show Me Everything** to select from a list of available options to register a visitor.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Workplace service portal**.

    **Note:** You can also raise a request from the Employee Center. On the home page, navigate to **Workplace** &gt; **Browse all Workplace** and select the workplace service.

2.  Open the **Visitor Management** category.

    1.  Select **Catalog**.

    2.  Select **Browse by Categories**.

    3.  In the Workplace Services Catalog, select **Visitor Management**.

        **Note:** If there are multiple catalogs configured on the portal, go to the Catalogs list and select **Workplace Services Catalog** &gt; **Visitor Management**.

3.  Select **Register a guest**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Visit description|Description with details about the purpose of the visit.|
    |Location|The location of the visit.|
    |Host|The name of the host of the visitor. By default, the field is set to **System Administrator**.|
    |Arrival date and time|The date and arrival time of the visit, shown as the arrival date and time icon \(![Arrival date and time icon.](../image/date-time-icon.png)\).|
    |Departure date and time|This field is automatically set to 1 hour after the specified arrival date and time. You can change this field by selecting your own time using the departure date and time icon \(![Departure date and time icon.](../image/date-time-icon.png)\).|
    |All day|Option for visits that last for an entire day.|
    |Private note to receptionist|Additional requirements or a private note to the receptionist.|
    |Co-hosts|Co-hosts for the visitor. The co-hosts and the main host are notified about the registration.|

5.  Select **Add an external visitor**, to add a visitor.

    1.  Select **Add**.

    2.  On the form, fill in the fields.

        | | |
        |---|---|
        |Select a known visitor|Option for selecting from a list of known visitors if the visitor has visited before. This selection automatically sets the name, email, and other relevant information of the visitor.|
        |Visitor type|The type of visitor.|
        |First name|The visitor's first name.|
        |Last name|The visitor's last name.|
        |Title|A title for the visitor if necessary.|
        |Visitor's email|The visitor's email address.|
        |Visitor's phone number|The visitor's contact number.|
        |Organization|The organization of the visitor.|
        |Wifi|Option for giving WiFi access to the visitor.|
        |VIP|Option for marking the visitor as an important person \(VIP\). This option helps the receptionist to prioritize the visitor.|
        |Parking preferences|The visitor's parking preference.|
        |License plate|The visitor's license plate details.|

    3.  Select **Add**.

    You can edit or remove a row from the form table using the add-remove row icon \(![Add-remove row icon.](../image/add-remove-sp-icon.png)\).

6.  Select **Add a company employee**, to add a colleague.

    1.  Select **Add**.

    2.  On the form, fill in the fields.

<table id="table_wlt_d5y_cnb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Select a colleague

</td><td>

The name of your colleague. The **First name**, **Last name**, and **Email** fields are automatically set. To edit any details, select the preview record icon \(![Preview record icon.](../../workplace-case-mgmt/image/preview-icon.png)\) and **Save** the changes.

</td></tr><tr><td>

Email

</td><td>

This field automatically sets t with the email address of the selected colleague. You can edit it.

</td></tr><tr><td>

Parking Type

</td><td>

The colleague's parking preference.

</td></tr><tr><td>

License plate

</td><td>

The colleague's license plate details.

</td></tr></tbody>
</table>    3.  Select **Add**.

    You can edit or remove a row from the form table using the Add-remove row icon \(![Add-remove row icon.](../image/add-remove-sp-icon.png)\).

7.  In the **Notification preferences** section, select the channel to be notified on when the visitor checks into the building.

    You can link the Virtual Agent with other channels like Microsoft Teams or Slack. For more information, see [Integrating Virtual Agent with other channels](https://www.servicenow.com/docs/access?context=integrate-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

8.  Select **Submit**.


## Result

Your visitor registration is submitted and you can view your requests. The details about the visit are sent to the visitor's email address.

If any visitor policies are applicable for the visit, the email sent to the visitor contains options to accept or decline the policies. If the visitor declines the policies in the email, they can still accept them while checking in through the Workplace Services Kiosk. For more information about the kiosk check-in process, see [Check in using an invite](../../workplace-services-kiosk/task/visitor-check-in.md).

## What to do next

You can check the details of your request. You can also edit or cancel the request.

-   You can view your requests by following one of the following steps.
    -   On the Workplace Service Portal, go to the Requests tab to view your requests and reservations.
    -   On the Now Mobile app navigation bar, select **For Me** and scroll down to the My Request section to view your requests.
    -   In the virtual agent chat, enter your question or select **Show Me Everything** to select from a list of available options to view your visitor details.
-   On the request details screen, you can cancel a request by selecting **Cancel Request**.
-   You can search for registered visitors in the **Visitors list** using the search option.

**Parent Topic:**[Registering a visitor](../concept/registerring-a-visitor.md)

**Related topics**  


[Review visitor policies](review-visitor-policies.md)

