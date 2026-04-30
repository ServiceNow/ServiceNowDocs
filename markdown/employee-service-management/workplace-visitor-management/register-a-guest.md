---
title: Make a visitor registration
description: Pre-plan your visitor or off-site colleagues visit. Specify their visit details like date, time, location, and more.
locale: en-US
release: yokohama
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Registering a visitor, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Make a visitor registration

Pre-plan your visitor or off-site colleagues visit. Specify their visit details like date, time, location, and more.

## Before you begin

**Important:** Starting with Workplace Core \(sn\_wsd\_core\) version 2.1, all updates, and new features are available only on the Workplace Service Portal. The workplace services provided by ServiceNow® are removed from the Service Portal on Workplace Core \(sn\_wsd\_core\) beginning with version 2.1. To configure the Workplace service catalog in the Service Portal, see [Configure a catalog in Service Portal](https://www.servicenow.com/docs/access?context=associate-portal-catalog&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

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

    **Important:** The date and time fields are in the time zone of the selected location.

<table id="table_y4z_yqy_cnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visit description

</td><td>

Description with details about the purpose of the visit.

</td></tr><tr><td>

Location

</td><td>

The location of the visit.

</td></tr><tr><td>

Host

</td><td>

The name of the host of the visitor. By default, the field is set to **System Administrator**.

</td></tr><tr><td>

Arrival date and time

</td><td>

Date and arrival time of the visit, shown as the arrival date and time icon \(![Arrival date and time icon.](../image/date-time-icon.png)\).

</td></tr><tr><td>

Departure date and time

</td><td>

This field is automatically set to one hour after the arrival date and time. You can change this field by selecting your own time using the departure date and time icon \(![Departure date and time icon.](../image/date-time-icon.png)\).

</td></tr><tr><td>

All-day invitation

</td><td>

Option for visits that last for an entire day.

</td></tr><tr><td>

Recurring invitation

</td><td>

Option to make a recurring invitation for the visitor.For recurring invitations, you can configure the following fields:

-   Repeat: Frequency of the recurring invitation. It can be **Daily**, **Weekly**, or **Monthly**.
-   Lasts: How long the recurring invitation lasts. You can the following values.
    -   For: Specifies how long the invitation lasts based on the **Number of days** field.
    -   Until: Specifies when the invitation expires based on the **Ends on this date** field.


</td></tr><tr><td>

Private note to receptionist

</td><td>

Additional requirements or a private note to the receptionist.

</td></tr><tr><td>

Co-hosts

</td><td>

Co-hosts for the visitor. The co-hosts and the main host are notified about the registration.

</td></tr></tbody>
</table>5.  Select **Add an external visitor**, to add a visitor.

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

7.  Bulk upload a list of visitors by using an Excel or CSV file.

    1.  Select **Add visitors using a file**.

    2.  Download the CSV or Excel template based on your preference.

    3.  In the downloaded file, fill in the visitor information.

        The columns in the file correspond to the fields in the **Add an external visitor** form. The visitor email column is required. If the visitor email is empty for any row, it’s skipped.

        **Note:** You can only add 50 internal visitors and 50 external visitors in one file. If you want to increase the number of rows that can be imported, configure the global property glide.sc.multirow\_set.rows.size and set it to the desired value which will apply to all portals. For more information, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0818277](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0818277).

    4.  Upload the file from your system by selecting **Upload**.

        The system displays invalid information in the **Invalid values** column. Ensure that you fix the issues before submitting the request.

        You can edit or remove a row from the form table using the add-remove row icon \(![Add-remove row icon.](../image/add-remove-sp-icon.png)\).

8.  In the **Notification preferences** section, select the channel to be notified on when the visitor checks into the building.

    You can link the Virtual Agent with other channels like Microsoft Teams or Slack. For more information, see [Integrating Virtual Agent with other channels](https://www.servicenow.com/docs/access?context=integrate-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

9.  Select **Submit**.


## Result

Your visitor registration is submitted and you can view your requests. The details about the visit are sent to the visitor's email address. The visitors also receive a reminder email with the invite code on the day before the registered date. For recurring invitations, only one email is sent for the visit details, but reminder emails are sent a day before every visit.

If any visitor policies are applicable for the visit, the email sent to the visitor contains options to accept or decline the policies. If the visitor declines the policies in the email, they can still accept them while checking in through the Workplace Services Kiosk. For more information about the kiosk check-in process, see [Check in using an invite](../../workplace-services-kiosk/task/visitor-check-in.md).

## What to do next

You can check the details of your request. You can also edit or cancel the request.

-   You can view your requests by following one of the following steps.
    -   On the Employee Center, go to the Requests tab to view your requests and reservations.
    -   On the Now Mobile app navigation bar, select **For Me** and scroll down to the My Request section to view your requests.
    -   In the virtual agent chat, enter your question or select **Show Me Everything** to select from a list of available options to view your visitor details.
-   On the request details screen, you can cancel a request by selecting **Cancel Request**.
-   You can search for registered visitors in the **Visitors list** using the search option.

**Parent Topic:**[Registering a visitor](../concept/registerring-a-visitor.md)

**Related topics**  


[Review visitor policies](review-visitor-policies.md)

