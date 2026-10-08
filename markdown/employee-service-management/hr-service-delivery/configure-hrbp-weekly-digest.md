---
title: Configure the HRBP weekly digest
description: Review and adjust the scheduled job that sends HR business partners a weekly email summarizing the open HR cases assigned to them. You can change when the weekly digest is sent, how many cases it lists, or stop sending it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/configure-hrbp-weekly-digest.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 4
keywords: [weekly digest, HRBP digest, scheduled job, notification, email]
breadcrumb: [Configure, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Configure the HRBP weekly digest

Review and adjust the scheduled job that sends HR business partners a weekly email summarizing the open HR cases assigned to them. You can change when the weekly digest is sent, how many cases it lists, or stop sending it.

## Before you begin

-   Data access records, rules, and assignments are set up so that HR cases are assigned to HR business partners. For more information, see [Define HRBP data access and data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).
-   The link for the **Ask HRBP Specialized Assistant** button is set. For more information, see [Configure the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-pa.md).
-   Email sending is enabled on your instance.

Role required: HRBP administrator \[sn\_hrbp\_hub.admin\]

## About this task

The weekly digest relies on two components that are installed with the HRBP Productivity app:

-   **HRBP Weekly Email Scheduled Job**

    A scheduled job that finds each active user with the sn\_hrbp\_hub.user role, collects the open HR cases assigned to that user, and builds the email content.

-   **HRBP Weekly Email Notification**

    An email notification that sends the email that the scheduled job builds.


Both components are active when the HRBP Productivity app is installed, so the digest is sent each week without further configuration. Because the scheduled job builds the email content, changes to the notification don't affect what the digest shows.

When the scheduled job collects cases for an HR business partner, it uses the access permissions of that HR business partner. As a result, each digest includes only the cases that the recipient has access to. HR business partners who have no open cases don't receive a digest.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select **Name** from the drop-down list associated with the **Search** field.

3.  In the **Search** field enter `*HRBP Weekly`.

4.  Select the **HRBP Weekly Email Scheduled Job** record.

    The record contains the following fields and default values:

<table id="table_digest_job"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

Weekly.

</td></tr><tr><td>

Day

</td><td>

Monday.

</td></tr><tr><td>

Time

</td><td>

08:00:00.The job runs at this time and sends every digest during that run.

</td></tr><tr><td>

Time zone

</td><td>

Floating.The job runs at the set time in the system time zone of your instance.

</td></tr><tr><td>

Run as

</td><td>

HRBP Weekly Digest Runner. A user installed with the application to run the scheduled job. If your change this user, the scheduled job doesn't send the digest.

</td></tr><tr><td>

Active

</td><td>

Selected. Clear this check box to stop sending the digest.

</td></tr></tbody>
</table>5.  Change the **Day** or **Time** fields to change when the digest is sent.

6.  Clear the **Active** check box to stop sending the digest.

7.  Select **Update**.

8.  Change the number of cases that the weekly digest lists.

    1.  Navigate to the **All** menu, and enter `sys_properties.list` in the navigation filter.

        The System Properties \[sys\_properties\] table appears.

    2.  Select **Name** from the drop-down list associated with the **Search** field.

    3.  In the **Search** field enter `*sn_hrbp_hub`.

        A list of system properties associated with the HRBP Productivity app appears.

    4.  Select the **sn\_hrbp\_hub.weekly\_digest.max\_items\_per\_category** property.

    5.  Use the **Value** field to specify the maximum number of cases that you want each digest to list.

        The default value in this field is **10**. Valid values are **1** through **10**.

    6.  Select **Update**.

9.  Run the scheduled job to verify that the weekly digest is sent and lists the cases that you expect.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Select **Name** from the drop-down list associated with the **Search** field.

    3.  In the **Search** field enter `*HRBP Weekly`.

    4.  Select the **HRBP Weekly Email Scheduled Job** record.

    5.  Select **Execute Now**.

        **Important:** Running the job sends the digest to every HR business partner with open cases.

    6.  Navigate to the **All** menu, and enter `sys_email.list` in the navigation filter.

        The Emails \[sys\_email\] table appears and lists an email record with the subject **HRBP Weekly Digest** for each HR business partner who has open cases.


## Result

Each HR business partner with open HR cases receives a weekly digest. The weekly digest shows the number of open cases that the HR business partner has and the number that are high priority. It also lists those cases, up to the number set in the **sn\_hrbp\_hub.weekly\_digest.max\_items\_per\_category** property. The digest includes an **Ask HRBP Specialized Assistant** button that the HR business partner can select to access the HRBP productivity assistant.

