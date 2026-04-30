---
title: Add email notifications for use with Emergency Outreach
description: Add an email notification to customize the send conditions and notification for your employees and use it in place of the default notification for an Emergency Outreach notification.
locale: en-US
release: zurich
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Emergency Outreach notifications, Emergency Outreach, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Add email notifications for use with Emergency Outreach

Add an email notification to customize the send conditions and notification for your employees and use it in place of the default notification for an Emergency Outreach notification.

## Before you begin

Review the default email notification to familiarize yourself with the way that the notification is laid out and scripted. Use the default notification details to prepare the information to use for the notification that you're adding.

<table id="table_hjq_v5n_dmb"><thead><tr><th>

Application

</th><th>

Notification name

</th></tr></thead><tbody><tr><td>

Emergency Outreach

</td><td>

Employee Check-ins

</td></tr><tr><td>

Employee Readiness Surveys

</td><td>

Outreach Surveys

</td></tr><tr><td>

Employee Health Screening

</td><td>

Daily Health Verification

</td></tr><tr><td>

Contact Tracing

</td><td>

-   Employee Daily Log Alert
-   User Privacy Consent
-   Notify Exposed Contact

</td></tr></tbody>
</table>Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_xgf_n1f_5mb"><thead><tr><th>

Outreach notification

</th><th>

Required fields for configuring the email notification

</th></tr></thead><tbody><tr><td>

Voluntary health check-in

</td><td>

**Table** field: Outreach Acknowledgements \[sn\_imt\_checkin\_check\_in\_acknowledgement\]**When to send** tab:

 -   **Send when**: Select **Record inserted or update**
-   **Conditions**:

**\[User.Active\]\[is\]\[true\]**

**\[Notification count\]\[changes\]** and

**\[Sys id\] \[starts with\]**

</td></tr><tr><td>

Outreach Surveys

</td><td>

**Table** field: Assessment Instance \[asmt\_assessment\_instance\]**When to send** tab:

 -   **Send when** field: Select **Event is fired**
-   **Event name** field: Select **sn\_imt\_checkin.survey\_instance\_notify**
-   **Conditions**:

**\[Assigned to.Active\]\[is\]\[true\]**

</td></tr><tr><td>

Daily Contact Log

</td><td>

**Table** field: Daily Log Acknowledgements \[sn\_imt\_tracing\_daily\_log\_acknowledgement\]**When to send** tab:

 -   **Send when**: Select **Record inserted or update**
-   **Conditions**:

**\[User.Active\]\[is\]\[true\]** and

**\[Acknowledgment Status\]\[is not\]\[Acknowledged\]**

</td></tr><tr><td>

User Privacy Consent

</td><td>

**Table** field: User Privacy Notice and Consents \[sn\_imt\_tracing\_user\_privacy\_consent\]**When to send** tab:

 -   **Send when**: Select **Record inserted or update**
-   **Conditions**:

**\[Parent consent\]\[is empty\]** and

**\[Consent status\]\[is\]\[Not Acknowledged\]** and

**\[Notification count\]\[changes\]** and

**\[Notification count\]\[greater than or is\]\[1\]** and

**\[User.Active\]\[is\]\[true\]** and

**\[Emergency Outreach.Email notification\]\[is\]\[true\]**

</td></tr><tr><td>

Notify Exposed Contact

</td><td>

**Table** field: Exposure Notice \[sn\_imt\_tracing\_exposure\_notice\]**When to send** tab:

 -   **Send when**: Select **Record inserted or update**
-   **Conditions**:

**\[User.Active\]\[is\]\[true\]** and

**\[Notification count\]\[changes\]**

</td></tr><tr><td>

Daily Health Verification Outreach

</td><td>

**Table** field: Health Verification Acknowledgements \[sn\_imt\_checkin\_health\_verification\_acknowledgement\]**When to send** tab:

 -   **Send when**: Select **Record inserted or update**
-   **Conditions**:

**\[User.Active\]\[is\]\[true\]** and

**\[Acknowledgment Status\]\[is not\]\[Acknowledged\]**

</td></tr></tbody>
</table>4.  In the **Advanced condition** field, enter the code to associate the email notification with the corresponding outreach notification.

    -   For the Outreach Surveys notification:

        ```
        var checkInSysId = event.getValue('parm1');
        var checkInGr = new GlideRecord('sn_imt_checkin_employee_check_in');
        checkInGr.get(checkInSysId);
        var thisNotificationSysId = '<your-sys_id>';
        answer = checkInGr.getValue('notification') === thisNotificationSysId && checkInGr.email_notification;
        
        ```

    -   For other outreach notifications:

        ```
        var thisNotificationSysId = '<your-sys_id>'
        answer = current.employee_check_in.notification = thisNotificationSysId;
        
        ```

    Replace the &lt;your-sys\_id&gt; variable with the sys\_id of the notification that you're adding. To do so, right-click in the header, select the **Copy sys\_id** option, and paste the sys\_id into the code line.

5.  In the **Who will receive** tab, select the audience to whom the notification will be sent.

    You can also select the target audience while configuring or sending the associated outreach notification. For more information, see [Send notifications for an emergency](send-eo-notification-outreach.md).

6.  In the **What it will contain** tab, enter the subject and text of the email message.

    Clear the email template if it does not apply to your outreach notification or you have defined the email content in the corresponding outreach notification.

7.  Click **Submit**.

8.  In the Notifications list, open the notification that you added and click **Preview Notification**.

9.  Review the notification and modify as necessary.

10. Click **Update**.


