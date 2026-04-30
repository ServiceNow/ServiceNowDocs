---
title: Configure Employee Health Screening
description: Set properties to specify the global maximum temperature thresholds in Fahrenheit and Celsius. Temperatures taken during a health screening are compared to the global temperature threshold, established by the company, to allow or deny entry.Decide whether you store temperatures recorded during screening events. Also set the maximum temperature threshold to use to determine whether it is safe for employees or visitors to enter the workplace.Define overrides of the maximum temperature threshold specified in properties for particular locations. For example, a workplace in Mexico may have a higher setting because the climate is warmer. Also override the property for whether QR codes are generated.The Employee Health Screening application provides an employee health verification that is ready to use. However, you can modify the verification if you want to change the criteria that employees must agree to.The Employee Health Screening application provides visitor notifications that are ready to use. However, you can modify the notifications if you want to customize them for your company.
locale: en-US
release: yokohama
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Employee Health Screening, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Employee Health Screening

Set properties to specify the global maximum temperature thresholds in Fahrenheit and Celsius. Temperatures taken during a health screening are compared to the global temperature threshold, established by the company, to allow or deny entry.

Another property lets you decide whether to generate QR codes when a health verification is submitted. You can also determine whether to store temperature readings within the application, and establish overrides by location.

Add an email notification and configure an outreach notification for the daily health verification. Send the outreach notification on demand or as scheduled to employees before they return to the workplace. For more information, see [Send notifications for daily health verification](../../business-continuity/task/send-daily-health-verif-notif-outreach.md).

**Parent Topic:**[Employee Health Screening](../concept/employee-health-screening.md)

## Set up Employee Health Screening properties

Decide whether you store temperatures recorded during screening events. Also set the maximum temperature threshold to use to determine whether it is safe for employees or visitors to enter the workplace.

### Before you begin

Role required: sn\_imt\_monitoring.monitoring\_admin or admin

### About this task

Employers remain solely responsible for complying with their legal obligations under applicable law, including data protection laws on collection, use, disclosure, and retention of personal data, and should enable, choose not to enable, or customize any functionality available within the application to meet the Employers’ specific requirements.

### Procedure

1.  Navigate to **All** &gt; **Employee Health Screening** &gt; **Properties**.

2.  Set the following property values.

<table id="table_n1r_jl4_rlb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clear health verification dailysn\_imt\_monitoring.clear\_health\_verification\_daily

</td><td>

If the **Yes/No** check box is selected, the **Response** field on health verification records is reset to **No** every day at the specified time. If the Employee Health Verification Requirement is active, the employee's requirement status is reset to **Not Cleared**.This property is not enabled by default.

</td></tr><tr><td>

Time to reset health verificationssn\_imt\_monitoring.time\_to\_reset\_health\_verifications

</td><td>

Sets the time when health verification responses are reset to **No** each day. The reset uses the local time for each user. For example, if you enter `17:00:00`, a user in Seattle has their verification reset at 5:00pm Pacific time and a user in Boston has their verification reset at 5:00pm Eastern time. The default time is midnight.

</td></tr><tr><td>

Limit health verification submissions to once per day.\[sn\_imt\_monitoring.limit\_health\_verification\_submission\]

</td><td>

If the **Yes/No** check box is selected, each employee can only submit the health verification once per day. If the **Yes/No** check box is cleared, there is no limit on the number of times per day that an employee can submit the health verification.

</td></tr><tr><td>

Enforce cleared status as condition for Health Screening.\[sn\_imt\_monitoring.enforce\_cleared\_status\_on\_screen\]

</td><td>

If the **Yes/No** box is selected, each employee must have a **Cleared** status to gain entry to a location. If the **Yes/No** box is cleared, a user's health and safety status does not automatically deny entry.

</td></tr><tr><td>

Setting this value to true will track employee temperature.\[sn\_imt\_monitoring.track\_temperature\]

</td><td>

If the **Yes/No** check box is cleared, the temperature thresholds entered are used only to determine whether the employee can enter. This information is not stored. By default, recording and storing temperatures is turned off.

</td></tr><tr><td>

Disable temperature check for vaccinated employees.\[sn\_imt\_monitoring.disable\_temperature\_check\_for\_vaccinated\_employees\]

</td><td>

If the **Yes/No** box is selected, vaccinated employees do not require a temperature check during health screening.**Note:** The **Temperature** field is hidden during health screening for vaccinated employees.

</td></tr><tr><td>

Setting this value to true will track employee PPE data.\[sn\_imt\_monitoring.track\_ppe\]

</td><td>

If the **Yes/No** check box is cleared, the PPE values entered are used only to determine whether the employee can enter. This information is not stored.

</td></tr><tr><td>

Global property for employee temperature fever cutoff in Fahrenheit. Values at or above this temperature are considered a fever.\[sn\_imt\_monitoring.temperature\_threshold\_fahrenheit\]

</td><td>

Set this threshold based on what you consider a safe temperature in Fahrenheit to allow returning employees into the workplace.

</td></tr><tr><td>

Global variable for employee temperature fever cutoff in Celsius. Values at or above this temperature are considered a fever.\[sn\_imt\_monitoring.temperature\_threshold\_celsius\]

</td><td>

Set this threshold for Celsius as described in the previous entry.

</td></tr><tr><td>

Setting this value to true will track visitor temperature data.\[sn\_imt\_monitoring.track\_visitor\_temperature\]

</td><td>

If the **Yes/No** check box is cleared, the temperature thresholds entered are used only to determine whether the visitor can enter. This information is not stored. By default, recording and storing temperatures is turned off.

</td></tr><tr><td>

Setting this value to true will track visitor PPE data.\[sn\_imt\_monitoring.track\_visitor\_ppe\]

</td><td>

If the **Yes/No** check box is cleared, the PPE values entered are used only to determine whether the visitor can enter. This information is not stored.

</td></tr><tr><td>

Global property for visitor temperature fever cutoff in Fahrenheit. Values at or above this temperature are considered a fever.\[sn\_imt\_monitoring.visitor\_temperature\_threshold\_fahrenheit\]

</td><td>

Set this threshold based on what you consider a safe temperature in Fahrenheit to allow visitors into the workplace.

</td></tr><tr><td>

Global variable for visitor temperature fever cutoff in Celsius. Values at or above this temperature are considered a fever.\[sn\_imt\_monitoring.visitor\_temperature\_threshold\_celsius\]

</td><td>

Set this threshold for Celsius as described in the previous entry.

</td></tr><tr><td>

Setting this property to true will show QR code for entry.\[sn\_imt\_monitoring.show\_qr\_code\]

</td><td>

If the **Yes/No** check box is selected, a QR code is displayed when an employee agrees to the health verification form. A health monitor at an entry point scans the code to review the employee's health requirements status. **Note:** Requirements are created in the Employee Readiness Core application. For more information, see [Employee Health and Safety Status](../../employee-readiness-core/concept/employee-health-safety-status.md).

 The QR code can be printed or displayed on a mobile device with the Now Mobile app.

</td></tr><tr><td>

Create entry request record when screener views Health Status record.sn\_imt\_monitoring.auto\_create\_request

</td><td>

If the **Yes/No** check box is selected, a record is created in the Request for Entry table \[sn\_imt\_monitoring\_request\_for\_entry\] every time that a user with the sn\_imt\_monitoring.monitoring\_user role views an employee's [health and safety status](../../employee-readiness-core/concept/employee-health-safety-status.md) by scanning the QR code or manually looking up the employee. If the employee's health and safety status is **Cleared**, the **Access Granted** field is set to **true** otherwise it is set to **false**.

 This property is not enabled by default.

</td></tr></tbody>
</table>3.  Click **Save**.


## Override maximum temperature by location

Define overrides of the maximum temperature threshold specified in properties for particular locations. For example, a workplace in Mexico may have a higher setting because the climate is warmer. Also override the property for whether QR codes are generated.

### Before you begin

Role required: sn\_imt\_monitoring.monitoring\_admin or admin

### Procedure

1.  To define overrides for employees, navigate to **Employee Health Screening** &gt; **Location Overrides**. To define overrides for visitors, navigate to **Employee Health Screening** &gt; **Visitor Location Overrides**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_nbd_qp4_rlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

The location to set a different maximum temperature threshold.

</td></tr><tr><td>

Track temperature

</td><td>

Option that indicates whether temperature data is stored when screened at this location.

</td></tr><tr><td>

Track PPE

</td><td>

Option that indicates whether PPE compliance is stored when screened at this location.

</td></tr><tr><td>

Show QR Code**Note:** This field is not used for visitors.

</td><td>

Option that indicates whether to generate a QR code when an employee health verification is submitted.

</td></tr><tr><td>

Unit

</td><td>

Temperature measuring unit.

</td></tr><tr><td>

Temperature

</td><td>

Employees or visitors must be at or below this temperature to be considered okay to enter the workplace.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Modify the employee health verification page

The Employee Health Screening application provides an employee health verification that is ready to use. However, you can modify the verification if you want to change the criteria that employees must agree to.

### Before you begin

Role required: catalog\_admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  Click the Health verification catalog item.

3.  In the **Description** field, update the criteria that employees must agree to.

4.  Click **Update**.


## Modify visitor notification emails

The Employee Health Screening application provides visitor notifications that are ready to use. However, you can modify the notifications if you want to customize them for your company.

### Before you begin

Role required: admin

### About this task

The Employee Health Screening application uses the following visitor notifications.

<table id="table_tdk_13r_2mb"><thead><tr><th>

Notification

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notify about scheduled visit

</td><td>

When the **sn\_imt\_core.send\_email\_to\_visitor** property is enabled, this email is sent to the visitor when an employee invites them to the workplace. The email is sent immediately after the employee submits the invitation. The email contains a brief confirmation of the scheduled visit, including information about the date of the visit and the name of the employee who invited them.This notification is installed with the Employee Readiness Core application.

</td></tr><tr><td>

Ask for health related data from visitor

</td><td>

This email is sent to the visitor before their scheduled visit. The **sn\_imt\_core.days\_to\_ask\_for\_health\_data** property sets when the email is sent. The email contains information about safety requirements and policies that the visitor must agree to follow. The visitor must respond `Yes` to the email to complete the Visitor Invitation Requirement from [Employee Health and Safety Status](../../employee-readiness-core/concept/employee-health-safety-status.md).

**Note:** To ensure that a visitor’s requirement status is updated when the visitor responds to this email, set the **glide.user.trusted\_domain** property to the default value \(\*\). For more information, see

 **Note:** [Inbound mail configuration](https://www.servicenow.com/docs/access?context=r_InboundMailConfiguration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). If you need to perform filtering on inbound emails, see [Email filters](https://www.servicenow.com/docs/access?context=c_EmailFilters&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

 This notification is installed with the Employee Readiness Core application.

</td></tr><tr><td>

Visitor Invitation Criteria Met

</td><td>

This email is sent to the visitor, the employee who invited them, and anyone on the watch list on the invitation. It is sent after the visitor responds `Yes` to the health data email. This email confirms the upcoming visit.

</td></tr><tr><td>

Visitor Invitation Criteria Not Met

</td><td>

This email is sent to the visitor, the employee who invited them, and anyone on the watch list on the invitation. It is sent after the visitor responds `No` to the health data email. This email asks the visitor to reschedule their visit.

</td></tr></tbody>
</table>For more information about the properties used to configure the email notifications, see [Set up Employee Health and Safety Status properties](../../employee-readiness-core/task/config-emp-core-properties.md).

### Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Click the visitor notification that you want to update.

3.  In the What it will contain form section, edit the **Message HTML** field to customize the notification email.

4.  To verify your changes, click **Preview Notification**.

5.  Click **Update**.


