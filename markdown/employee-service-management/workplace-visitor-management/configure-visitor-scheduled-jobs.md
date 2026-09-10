---
title: Configure the frequency of email notifications
description: ServiceNow provides two scheduled jobs in the Workplace Visitor Management application that automate email notifications for visitor registration and policy confirmation. This topic explains how to locate these jobs and adjust their execution frequency to meet your organization's notification requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-visitor-management/configure-visitor-scheduled-jobs.html
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 3
breadcrumb: [Configure, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Configure the frequency of email notifications

ServiceNow provides two scheduled jobs in the Workplace Visitor Management application that automate email notifications for visitor registration and policy confirmation. This topic explains how to locate these jobs and adjust their execution frequency to meet your organization's notification requirements.

## Before you begin

Role required: admin

## About this task

The Workplace Visitor Management application includes the following scheduled jobs to handle automated visitor email communications:

-   Send visitor policy confirmation reminders: Runs daily to send reminder emails to visitors who have not yet confirmed the visitor policy.
-   Send visitor registration emails: Runs every hour to notify visitors about their upcoming or pending registrations.

As an admin, you can change the frequency of the jobs to control how often your visitors receive automated email reminders.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select the job that you want to configure.

    -   Send visitor policy confirmation reminders
    -   Send visitor registration emails
    The scheduled jobs are of the type **Scheduled script execution**.

3.  Configure the frequency of the job based on your requirement.

    For more information about scheduled script execution jobs, see [Automatically run a script of your choosing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ScheduleAScriptExecution.md).

    1.  In the **Run** field, select an option based on your requirement.

        For Send visitor policy confirmation reminders, the default value is **Daily**. For Send visitor registration emails, the default value is **Periodically**.

    2.  Based on the value of the **Run** field, edit one of the following fields.

        -   If you selected **Daily**, set the **Time** field to the time of day the job should run. For example, set it to `15:00:01` to run it at 3:00pm every day.
        -   If you selected **Periodically**, set the **Repeat Interval** field to the desired interval. For example, set it to `1 hour` to run the job every hour.
        -   If you selected **Weekly** or **Monthly**, configure the **Day** and **Time** fields to specify when the job should run.
    3.  In the **Time zone** field, set a time zone for the job execution.

        If you don't select a time zone, the job runs in your time zone. If you select **Use System Time Zone**, the job runs in the time zone of the instance.

4.  Select **Update** to save your changes.

    The scheduled job is saved with the new frequency settings. The job runs automatically at the next scheduled interval and visitors will receive automated emails based on the updated schedule.


## Result

The selected visitor notification scheduled job is now configured to run at the specified frequency. Visitors will receive automated emails according to the updated schedule.

**Parent Topic:**[Configuring Workplace Visitor Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-visitor-management/configure-visitor-mgmt.md)

**Related topics**  


[Install Workplace Visitor Management]()

[Create a visitor policy]()

[Create a record producer for visitor management]()

[Configure a visitor type]()

[Configure visit requirements]()

[Create a visitor badge template]()

[Configuring Workplace Visitor Management for Workplace Services Kiosk]()

[Quick start test for Workplace Visitor Management]()

