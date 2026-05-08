---
title: Configure Health and Safety Testing
description: Complete all configuration tasks to ensure that Health and Safety Testing is set up correctly for your company.Set up Health and Safety Testing properties to define the data retention period for health testing data and enable or disable emails to potentially exposed individuals.Configure the data retention settings for Health and Safety Testing so that the data-retention policy is country-specific.Create a list of COVID-19 diagnostic test providers that your company uses to schedule testing for employees.Modify the notification email that is sent to potentially exposed individuals to customize the notification for your company.Set up privacy consents for users who are providing health and safety testing data to your company.
locale: en-US
release: australia
product: Health and Safety Testing
classification: health-and-safety-testing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Health and Safety Testing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Health and Safety Testing

Complete all configuration tasks to ensure that Health and Safety Testing is set up correctly for your company.

**Parent Topic:**[Health and Safety Testing](../concept/health-safety-testing.md)

## Set up Health and Safety Testing properties

Set up Health and Safety Testing properties to define the data retention period for health testing data and enable or disable emails to potentially exposed individuals.

### Before you begin

Role required: sn\_imt\_health\_test.admin

### Procedure

1.  Navigate to **All** &gt; **Health and Safety Testing** &gt; **Properties**.

2.  Set the following property values.

<table id="table_vhc_j5n_cnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Testing data retention period \(in days\).\[sn\_imt\_health\_test.data\_retention\_period\]

</td><td>

Sets the number of days that data for COVID-19 diagnostic test requests and results is available in the system before it is deleted automatically. The **Data Retention Job for Health and Safety Testing** scheduled job runs daily to delete records that have an updated date past the specified retention period.**Note:** When an employee's test results are deleted, their health and safety requirement status is reset to the default status for **Testing Requirement Satisfied**. If the employee is a potentially exposed individual in a contact tracing case, their health and safety requirement status is reset to **Not Cleared** until they submit a negative test result. For more information about health and safety requirements, see [Employee Health and Safety Status](../../employee-readiness-core/concept/employee-health-safety-status.md).

</td></tr><tr><td>

Send email to potentially exposed individuals asking them to submit a test request.\[sn\_imt\_health\_test.notify\_potentially\_exposed\]

</td><td>

When enabled, an email notification is sent to employees who are potentially exposed individuals in a contact tracing case and have a health status of **Under investigation**. The notification informs the employee of the potential exposure and provides them with a link to request testing.

</td></tr><tr><td>

Use country-specific data retention policy for Health and Safety Testing.\[sn\_imt\_health\_test.use\_country\_specific\_data\_retention\_policy\]

</td><td>

Enable this property to use country-specific data retention policies for Health and Safety Testing. When enabled, records are compared to the data retention policy of the user's location to determine how long records are retained.

 For example, one country may have a 90 day retention period while another has a 120 day policy.

 When there is no country-specific policy, the policy defaults to the value in the **Health and Safety Testing data retention period \(in days\)** property. This property is inactive by default.

</td></tr><tr><td>

Message auto-created in work notes when test result is positive.\[sn\_imt\_health\_test.positive\_result\_message\]

</td><td>

Create the message automatically generated in the work notes for users to read when a test result is positive, such as advice to self-quarantine or notify members of their household that they tested positive.

</td></tr><tr><td>

Prevent admin from accessing attachments\[sn\_imt\_health\_test.prevent\_admin\_access\_to\_attachments\]

</td><td>

Enable this property to ensure that only scoped administrators can view attachments submitted by users for reported vaccinations. This prevents system administrators from viewing these attachments. The property is inactive by default.

</td></tr><tr><td>

Allow managers the ability to update health test results\[sn\_imt\_health\_test.allow\_managers\_ability\_to\_update\_test\_result\_records\]

</td><td>

Enable this property to provide all managers with the ability to review and update the reported health tests of their direct reports in the Approval Portal. All managers receive the Approval Portal manager \[sn\_imt\_core.approval\_portal\_manager\] role. This property is inactive by default. **Note:** If this property is not enabled, managers can access employee records in the Test Result table.

</td></tr></tbody>
</table>3.  Click **Save**.


## Configure country-specific data retention settings for Health and Safety Testing

Configure the data retention settings for Health and Safety Testing so that the data-retention policy is country-specific.

### Before you begin

Role required: sn\_imt\_core.admin, sn\_imt\_health\_test.admin, or sn\_imt\_vaccine.admin

### About this task

Employers remain solely responsible for complying with their legal obligations under applicable law, including data protection laws on collection, use, disclosure, and retention of personal data, and should enable, choose not to enable, or customize any functionality available within the application to meet the Employers’ specific requirements.

The **Health and Safety Testing data retention period \(in days\)** property sets the number of days that COVID-19 diagnostic test requests and results are available before they are deleted automatically. The**Data Retention Job for Health and Safety Testing** scheduled job runs daily to delete records that have an updated date past the specified retention period.

Enable the **Use country-specific data retention policy for Health and Safety Testing** property and use the Data Retention module in Employee Health and Safety Status to define policies at the country-level.

### Procedure

1.  Navigate to **All** &gt; **Health and Safety Testing** &gt; **Properties**.

2.  Set the **Use country-specific data retention policy for Health and Safety Testing** to **true**.

3.  Click **Save**.

4.  Generate location policies for Health and Safety Testing.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Data Retention**.

    2.  Click **Generate Location Policies**.

        The default number of days is based off the value in the **Health and Safety Testing data retention period \(in days\)** property.

5.  Open the location policy that you want to modify.

6.  In the **Retention period \(in days\)** field, enter the number of days that you want to retain data for.

7.  Click **Update**.


### Result

When the **Data Retention Job for Health and Safety Testing daily** scheduled job completes or is manually executed, the data for users in those locations have their COVID-19 diagnostic test requests and results retained or deleted based on their country's data retention policy.

## Add COVID-19 test providers

Create a list of COVID-19 diagnostic test providers that your company uses to schedule testing for employees.

### Before you begin

Role required: sn\_imt\_health\_test.testing\_admin

### Procedure

1.  Navigate to **All** &gt; **Health and Safety Testing** &gt; **Providers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Company|The company providing COVID-19 diagnostic tests.|
    |Supported test types|The types of testing offered by the provider. The options are **At a facility** and **Self-administered**. You can create additional test types if necessary.|

4.  Click **Submit**.


### What to do next

When an employee submits a request for testing, use the list of providers to schedule the test according to the employee's preferred test type and location.

## Customize the notification for potentially exposed individuals

Modify the notification email that is sent to potentially exposed individuals to customize the notification for your company.

### Before you begin

Role required: admin and sn\_imt\_health\_test.admin

### About this task

The **Potentially exposed health test request** notification is sent to employees who are potentially exposed individuals in a contact tracing case and have a health status of **Under investigation**. The notification informs the employee of the potential exposure and provides them with a link to request testing. The notification is only used when the **sn\_imt\_health\_test.notify\_potentially\_exposed** property is enabled.

By default, the notification uses a ServiceNow® banner and a placeholder signature. Update the notification to use your company logo and signature.

### Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Click the **Potentially exposed health test request** notification.

3.  To view the default notification, click **Preview Notification**.

4.  Navigate to the **What it will contain** form section.

5.  In the **Message HTML** field, click **Insert/edit image** and select your banner image.

    **Tip:** The image must be added before the mail script so that it appears at the top of the email.

    If you don't already have an email banner image in your ServiceNow instance, you can upload an image to use. For instructions, see Upload one or more images.

6.  Click the **Show Notification Scripts** related link.

7.  In the **Script** field, the code `template.print(util.getEmailCompanyLogo());` adds the default ServiceNow® banner to the email.

    Comment out or delete this line of code to remove the ServiceNow® banner.

8.  In the **Script** field, replace `You can expect [these next outreach steps]` with the next steps that you want to communicate to employees.

9.  In the **Script** field, replace `The Site Safety Team` signature with your preferred signature.

10. If you would like to make any other changes to the email notification, update the **Script** field as needed.

11. Click **Update**.

12. Return to the notification record and click **Preview Notification** to confirm your changes.


## Set up privacy consents for Health and Safety Testing

Set up privacy consents for users who are providing health and safety testing data to your company.

### Before you begin

Role required: sn\_imt\_core.admin

### About this task

Users must agree to a privacy policy in order to be able to request or report diagnostic data. They also must have the sn\_imt\_core.privacy\_consent\_user role.

### Procedure

1.  Customize the privacy consent template.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Privacy Consent Templates** and click **Testing Consent Template**.

    2.  Fill in the placeholder text with the name of your company and contact information.

    3.  Click **Update**.

2.  Assign the sn\_imt\_core.privacy\_consent\_user role to all users who will be requesting and reporting diagnostic test results.

    This role allows users to complete the privacy consent.

3.  Generate the [location-based privacy configurations](../../employee-readiness-core/task/generate-location-common-privacy-configuration.md) for the locations in your instance.

4.  Configure an outreach to send the privacy consent to users.

    1.  Navigate to **Emergency Outreach** &gt; **View Outreaches** and click the **Health and Safety Testing Diagnostic Test Placeholder** outreach.

        This outreach is preconfigured to use the Health and Safety Testing Diagnostic Test Placeholder Audience Record and the Testing Consent Template.

    2.  Make any modifications to the outreach if needed, such as scheduling a time to send.

        For more information, see [Send notifications for an emergency](../../business-continuity/task/send-eo-notification-outreach.md).

    3.  Enable the outreach to provide location-specific privacy consents by selecting the **Use Country** option on the **Content configuration** tab.

        When enabled, the privacy statement text in Location Privacy Configuration takes precedence over text in the privacy consent templates. This text is used for the outreach, system notification email, and push notification. If you need to update the text that users receive, you must change the location's privacy statement.

    4.  Click **Update**.


### Result

Users can request and report diagnostic test results. Users that attempt to request a test are automatically added to the Health and Safety Testing Diagnostic Test Placeholder Audience Record about every 10 minutes. These users will also receive the notification around that time.

