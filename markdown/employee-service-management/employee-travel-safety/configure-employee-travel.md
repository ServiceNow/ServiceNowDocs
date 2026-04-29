---
title: Configure Employee Travel Safety
description: Complete all configuration tasks to ensure that travel notifications and approvals are set up correctly for your company.Set up user groups and roles so that employee travel can be approved by managers or by designated travel approvers.Set up Employee Travel Safety properties to ensure that site safety verification emails, employee contact logs, and employee health verifications are managed according to your company's requirements.Modify the travel approval flow to change the default travel approval settings.Modify the notification emails that are sent to employees, managers and travel approvers, and employee travel contacts to customize the notifications for your company.
locale: en-US
release: australia
product: Employee Travel Safety
classification: employee-travel-safety
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Employee Travel Safety, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Employee Travel Safety

Complete all configuration tasks to ensure that travel notifications and approvals are set up correctly for your company.

**Parent Topic:**[Employee Travel Safety](../concept/employee-travel-safety.md)

## Set up travel approvers

Set up user groups and roles so that employee travel can be approved by managers or by designated travel approvers.

Setting up manager approval or designated approvers is a required configuration step for the Employee Travel Safety application.

-   **Manager approval**

    To set up travel approval by managers, assign the approver\_user role to all managers. With this role, managers can only view and approve travel requests for the employees they directly supervise.

-   **Designated approvers**

    To set up designated travel approvers, add users to the Travel Approvers group. Members of this group can view and approve travel requests for all employees. Don't add managers to the Travel Approvers group unless it's acceptable for them to view and approve travel requests for all employees.


By default, a travel request must be approved by both the employee's manager and a member of the Travel Approvers group. If the employee doesn't have a manager listed in your ServiceNow instance or there are no users in the Travel Approvers group, one approval is enough to approve the travel request. An employee's travel request is automatically rejected if the employee doesn't have a manager listed in your ServiceNow instance and there are no users in the Travel Approvers group. For information about changing the default approval settings, see [Modify the travel approval flow](configure-employee-travel.md#).

## Set up Employee Travel Safety properties

Set up Employee Travel Safety properties to ensure that site safety verification emails, employee contact logs, and employee health verifications are managed according to your company's requirements.

### Before you begin

Role required: sn\_imt\_travel.admin

### About this task

Setting up the Employee Travel Safety properties is a required configuration step for the Employee Travel Safety application.

### Procedure

1.  Navigate to **All** &gt; **Employee Travel Safety** &gt; **Properties**.

2.  Set the following property values.

<table id="table_l44_3fb_5mb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name of the company's travel management system.\[sn\_imt\_travel.travel.management.system.name\]

</td><td>

Name of your company's travel management system. This property is used to provide employees who are approved for travel with a link to the travel management system.

</td></tr><tr><td>

URL of the company's travel management system.\[sn\_imt\_travel.travel.management.system.url\]

</td><td>

URL of your company's travel management system. This property is used to provide employees who are approved for travel with a link to the travel management system.

</td></tr><tr><td>

Email travel contacts to ask them to verify site safety and policy compliance.\[sn\_imt\_travel.email\_site\_verification\]

</td><td>

When enabled, an email is sent to the primary contact that an employee provides on their travel request to verify site safety and policy compliance. The contact must respond to the email before the travel request can be approved by a manager or travel approver.

</td></tr><tr><td>

Comma-separated list of affirmative responses.\[sn\_imt\_travel.affirmative\_email\_responses\]

</td><td>

Defines the responses that are accepted as `Yes` responses for site verification emails.

</td></tr><tr><td>

Enables sending email reminders to travel request approvers for requests pending approval.\[sn\_imt\_travel.enable\_approval\_email\_reminders\]

</td><td>

When enabled, email reminders are sent to travel approvers and managers for travel requests that haven't been approved or rejected.

</td></tr><tr><td>

Length of time \(in hours\) to wait before sending travel request approvers a reminder. Default is 48.\[sn\_imt\_travel.approval\_email\_reminder\_period\]

</td><td>

Sets the frequency of email reminders that are sent to travel approvers and managers. For example, when this property is set to `48`, travel approvers and managers will receive a reminder every 48 hours after a travel request is submitted until it is approved or rejected. This property requires that the **sn\_imt\_travel.enable\_approval\_email\_reminders** property is enabled.

</td></tr><tr><td>

Enables outreach to relevant employees about travel-related health verifications.\[sn\_imt\_travel.daily.health.verification.outreach.flag\]

</td><td>

When enabled, employees who are approved for travel receive notifications to complete a health verification. To set the frequency of the notifications, select a value for the **sn\_imt\_travel.health.verification.run.type** property. For more information about employee health verification, see [Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md).

</td></tr><tr><td>

Choose whether Health Verifications will be sent to requester only once or daily.\[sn\_imt\_travel.health.verification.run.type\]

</td><td>

Sets the frequency of the health verification notifications that are sent to employees who are approved for travel. To send daily notifications before and during travel, select **Send Daily**. To send a notification once after the travel request is approved, select **Send Once**.

 Health verification notifications are only sent if the **sn\_imt\_travel.daily.health.verification.outreach.flag** property is enabled.

 **Note:** Employees who are already enrolled in daily health verifications before their travel request is approved will see no change. They will not receive additional notifications and they will still be enrolled after their trip is complete.

</td></tr><tr><td>

Cancels a travel request if a health verification is not completed after a number of hours.\[sn\_imt\_travel.allow.cancellation\]

</td><td>

When enabled, travel requests are canceled if employees do not complete a health verification by the deadline. Enabling this property requires that the **sn\_imt\_travel.daily.health.verification.outreach.flag** property is also enabled.

</td></tr><tr><td>

For automatic request cancellation, enter the number of hours.\[sn\_imt\_travel.cancellation\_duration\]

</td><td>

Sets the deadline for employees to complete a health verification. This property requires that the **sn\_imt\_travel.allow.cancellation** property is enabled.

</td></tr><tr><td>

Enables outreach to traveling employees about their daily travel contacts.\[sn\_imt\_travel.daily.contact.log.outreach.flag\]

</td><td>

When enabled, employees receive notifications to complete a daily contact log during internal travel. Contact log notifications are not sent for external travel. Employees must be assigned the sn\_imt\_tracing.dailylog\_user role to receive contact log notifications. This property requires the Contact Tracing and Emergency Outreach applications. For more information about contact logs, see [Contact Tracing](../../contact-tracing/concept/contact-tracing.md).**Note:** Employees who are already enrolled in daily contact logs before their trip will see no change. They will not receive additional notifications and they will still be enrolled after their trip is complete.

</td></tr></tbody>
</table>3.  Click **Save**.


## Modify the travel approval flow

Modify the travel approval flow to change the default travel approval settings.

### Before you begin

Role required: flow\_designer

### About this task

Modifying the travel approval flow is an optional configuration step for the Employee Travel Safety application. The travel approval flow is ready to use but can be modified to meet your company's requirements.

If you decide to modify the flow, deactivate the original flow and make a copy. Make any desired changes to the new flow, and then activate it. Modifying the copy makes it easier when you need to upgrade your ServiceNow instance.

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  In the Flows section, click **Travel Approval Flow**.

3.  Click **Deactivate**, then click **OK** to confirm.

4.  In the upper-right corner, click the More actions icon \(![More actions icon](../../../common/image/Form_MoreOptions.png)\), then click **Copy flow**.

5.  Enter a name for the new flow.

6.  In the **Application** field, select **Employee Travel Safety**.

7.  Click **Copy**.

8.  Make any desired changes to the new flow.

    For example, in cases where an employee has a manager listed in your ServiceNow instance and there are also users in the Travel Approvers group, by default, both the manager and a travel approver must approve the request. This setting is defined in action 8.1 of the flow. You can modify this action so that approval is only required from either a manager or a travel approver, not both. To make this change, the AND condition to approve must be replaced with an OR condition.

9.  When you're done modifying the flow, click **Activate**, then click **OK** to confirm.


## Customize notification emails

Modify the notification emails that are sent to employees, managers and travel approvers, and employee travel contacts to customize the notifications for your company.

### Before you begin

Role required: admin

### About this task

Modifying the notification emails is a required configuration step for the Employee Travel Safety application. By default, the notifications use a ServiceNow® banner and the placeholder signature Workplace, Co. Update the notifications to use your company name and logo.

The Employee Travel Safety application uses the following notifications.

<table id="table_wyr_m2t_5mb"><thead><tr><th>

Notification

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Site Verification Request

</td><td>

This email is sent to the primary contact that an employee provides on their travel request to verify site safety and policy compliance. By default, the email asks the contact to confirm the following policies.-   The site screens all employees and visitors for symptoms.
-   All employees and visitors are required to wear personal protective equipment, such as masks.
-   All employees and visitors are required to follow social distancing rules.

 This email is only sent if the **sn\_imt\_travel.email\_site\_verification** property is enabled.

</td></tr><tr><td>

Employee Travel Safety Approver Request

</td><td>

This email is sent to an employee's manager and all members of the Travel Approvers group asking them to approve or reject the travel request.

</td></tr><tr><td>

Employee Travel Safety Request Reminder

</td><td>

This email is sent to managers and travel approvers as a reminder to approve or reject pending travel requests.This email is only sent if the **sn\_imt\_travel.enable\_approval\_email\_reminders** property is enabled.

</td></tr><tr><td>

Travel Request Approval

</td><td>

This email is sent to an employee if their travel request is approved. The email has a link to your company's travel management system.

</td></tr><tr><td>

Travel Request Rejection

</td><td>

This email is sent to an employee if their travel request is rejected.

</td></tr><tr><td>

Travel-related contacts

</td><td>

This email asks an employee to complete a daily contact log. The email is sent to an employee daily for the duration of their trip.This email is only sent if the **sn\_imt\_travel.daily.contact.log.outreach.flag** property is enabled.

</td></tr><tr><td>

Travel-related health verification

</td><td>

This email asks an employee to complete a daily health verification. The email is sent to an employee daily once their travel request is approved though the duration of their trip.This email is only sent if the **sn\_imt\_travel.daily.health.verification.outreach.flag** property is enabled.

</td></tr><tr><td>

Travel request rescinded

</td><td>

This email is sent to an employee if they don't complete a health verification by the deadline.This email is only sent if the **sn\_imt\_travel.allow.cancellation** property is enabled.

</td></tr></tbody>
</table>**Note:** All notifications except the Employee Travel Safety Approver Request are translated to the language selected on the employee's user profile. The Employee Travel Safety Approver Request is translated to the language selected on the manager's or travel approver's user profile. If no language is selected for a user, notifications are translated to the default language for the instance.

### Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Click the notification that you want to update.

3.  To view the default notification, click **Preview Notification**.

4.  Navigate to the **What it will contain** form section.

5.  In the **Message HTML** field, click **Insert/edit image** and select your banner image.

    **Tip:** The image must be added before the mail script so that it appears at the top of the email.

    If you don't already have an email banner image in your ServiceNow instance, you can upload an image to use. For instructions, see [Upload one or more images](https://www.servicenow.com/docs/access?context=upload-multiple-images&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

6.  Click the **Show Notification Scripts** related link.

7.  In the **Script** field, the code `template.print(util.getEmailCompanyLogo());` adds the default ServiceNow® banner to the email.

    Comment out or delete this line of code to remove the ServiceNow® banner.

8.  In the **Script** field, replace all references to `Workplace, Co.` with your company name.

9.  If you would like to make any other changes to the email notification, update the **Script** field as needed.

    If you change any text used in calls to `gs.getMessage` or `gs.getMessageLang`, you must provide translations for your custom text in the Message table \[sys\_ui\_message\]. For more information, see [Message table](https://www.servicenow.com/docs/access?context=r_MessageTable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

10. Click **Update**.

11. Return to the notification record and click **Preview Notification** to confirm your changes.


