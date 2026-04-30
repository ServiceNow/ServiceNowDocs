---
title: Configure Contact Tracing data retention settings
description: Configure the data retention settings for the data collected for contact tracing such as badge swipe data, employee daily contact logs, and cases.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Contact Tracing data retention settings

Configure the data retention settings for the data collected for contact tracing such as badge swipe data, employee daily contact logs, and cases.

## Before you begin

Role required: admin

## About this task

Employers remain solely responsible for complying with their legal obligations under applicable law, including data protection laws on collection, use, disclosure, and retention of personal data, and should enable, choose not to enable, or customize any functionality available within the application to meet the Employers’ specific requirements.

A system property and scheduled jobs control the data retention policy for contact tracing data.

-   The **sn\_imt\_tracing.data\_retention\_period** system property determines the number of days the contact tracing data will be available in the system before it is deleted automatically.
-   The **Data Retention Job For Contact Tracing** scheduled job checks for records that have an updated date that is past the defined retention period, and deletes them.

    The data retention policy applies to the following contact tracing data:

    -   **Badge swipe data**

        Table impacted: Badge Access Register \[sn\_imt\_tracing\_badge\_access\_register\]

    -   **Closed and canceled cases and associated records**

        Tables impacted: Case \[sn\_imt\_tracing\_case\], Case Task \[sn\_imt\_tracing\_case\_task\], Exposed Contacts \[sn\_imt\_tracing\_exposed\_contact\], Diagnostic Request \[sn\_imt\_diagnosis\_diagnostic\_request\], Diagnostics Events \[sn\_imt\_diagnosis\_diagnostics\_event\], and Potential Workplace Exposure \[sn\_imt\_diagnosis\_potential\_workplace\_exposure\]

        The Diagnostic Request and Diagnostics Events tables are installed with the [Emergency Exposure Management](../../business-continuity/concept/emergency-exposure-management.md) application.

        **Note:** A survey associated with cases that are eligible for deletion after the retention period is not deleted because surveys have their own retention period. For more information, see [Clean up assessment data](https://www.servicenow.com/docs/access?context=t_CleanUpAssessmentData&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   **Employee daily contact logs**

        Tables impacted: Daily Contact Logs \[sn\_imt\_tracing\_daily\_contact\_log\], Daily Log Acknowledgements \[sn\_imt\_tracing\_daily\_log\_acknowledgement\], and Daily Log Notes \[sn\_imt\_tracing\_daily\_log\_note\]

    -   **Wi-Fi access data**

        Tables impacted: WiFi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\]and Wi-Fi Access Register Job \[sn\_imt\_tracing\_wifi\_access\_register\_job\]

-   The **Purge Contact Tracing Deleted Records \(Data Retention\)** scheduled job purges all deleted records of contact tracing from the Audit Deleted Record \[sys\_audit\_delete\] table. All deleted records with an updated date past the defined retention period are purged.

## Procedure

1.  Set the period for which you want to keep the contact tracing data.

    1.  Navigate to **Contact Tracing** &gt; **Administration** &gt; **Properties**.

    2.  Enter a value in the **Contact Tracing data retention period \(in days\)** property.

        The default value is 90 days.

    3.  Click **Save**.

2.  Configure the scheduled job to determine when the job runs to check for and delete the contact tracing data.

    1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    2.  Open the **Data Retention Job For Contact Tracing** scheduled job.

    3.  Configure the job settings and click **Save**.

        For more information, see [Configure a scheduled job](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

3.  Download, import, and configure the **Purge Contact Tracing Deleted Records \(Data Retention\)** schedule job in the Global scope to purge deleted records.

    1.  Download the `Purge Contact Tracing Deleted Records (Data Retention)` XML file from the Contact Tracing application page on the ServiceNow® Store.

    2.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    3.  Import the downloaded XML file into the Scheduled Job \[sysauto\] table.

        For more information on importing, see [Import a record from the template](https://www.servicenow.com/docs/access?context=t_ImportARecordFromTheTemplate&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

    4.  Search and open the **Purge Contact Tracing Deleted Records \(Data Retention\)** record.

    5.  Select **Active** to activate the job.

    6.  In the **Run** field, set the schedule for the job to run.

    7.  Click **Update**.


**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

