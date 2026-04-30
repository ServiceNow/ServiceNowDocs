---
title: Configure an email notification for a privacy consent request
description: Configure an email notification to use in the Emergency Outreach app to request that employees review the organization's privacy policy and provide their consent to use their data for contact tracing.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up data privacy consent settings for Contact Tracing, Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure an email notification for a privacy consent request

Configure an email notification to use in the Emergency Outreach app to request that employees review the organization's privacy policy and provide their consent to use their data for contact tracing.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notifications** &gt; **Email** &gt; **Notifications**.

2.  Review the existing **User Privacy Consent** email notification to familiarize yourself with the script and other settings.

    ![The When to send tab in the User Privacy Consent notification.](../image/email-notif-privacy.png "User Privacy Consent base system notification")

3.  Click **New**.

4.  In the **Table** field, select the User Privacy Notice and Consents \[sn\_imt\_tracing\_user\_privacy\_consent\] table.

5.  On the **When to send** tab, set the conditions.

    1.  In the **Conditions** field, set the criteria as shown in the image of the base system notification.

    2.  Copy the following example script in the **Advanced condition** field.

        ```
        var employeeCheckInAcmeSysId = '<replace with this notification sys_id';
        answer = current.employee_check_in.notification == employeeCheckInAcmeSysId
        
        ```

    3.  Make the following modifications to the example script:

        -   Give the variable a different name, for example, *employeeCheckInAcmeSysId*.
        -   Enter the new notification sys\_id as the value.
        -   Enter the variable name that you declared at the end of the second line.
6.  On the **Who will receive** tab, open **Users/Groups in fields** and select **Assigned to**.

7.  Complete the remaining information on the **What it will contain** tab.

    While entering the email content in the **Message HTML** field, make sure that you include the link to the Privacy Consent form.

8.  Click **Submit**.

9.  In the Notifications list, open the notification that you added and click **Preview Notification**.

10. Review the notification and make any changes required.

11. Click **Update**.


**Parent Topic:**[Setting up data privacy consent settings for Contact Tracing](../concept/set-up-privacy-consent-settings.md)

