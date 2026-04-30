---
title: Setting up Contact Tracing
description: Configure system properties, scheduled jobs, script includes, Wi-Fi access log integration, and outreach notifications to aggregate contact tracing information for various data sources.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Setting up Contact Tracing

Configure system properties, scheduled jobs, script includes, Wi-Fi access log integration, and outreach notifications to aggregate contact tracing information for various data sources.

In Contact Tracing version 1.29.4. and above, the navigation path is not available in the application context menu search \(**All** &gt; **Contact Tracing**\) for Zebra MotionWorks and Devvio. The following application modules are not available in the application search context menu Contact Tracing version 1.29.4:

-   Handheld/Wearable Access Management \(separator\)
-   Wearable Access Register
-   Devvio \(Separator\)
-   Devvio Users Risk Report
-   Devvio Users Risk Report Import Set

The navigation path is available if you are using Contact Tracing 1.29.2 and later versions.

Get contact tracing information from various data sources such as workplace locations, work shifts and reservations, badge scans, Wi-Fi access logs, and self-reporting logs. Use these data sources to identify potentially exposed users by running the diagnostic request in the Emergency Exposure Management application.

## Identifying potentially exposed users using tracing systems

A tracing system is configured for each contact tracing data source. Review the tracing systems for data sources to see whether these tracing systems meet your business needs. You can modify these tracing systems or set up a new tracing system for your data source.

For more information, see [Set up a tracing system for an exposure data source](../../business-continuity/task/set-up-tracing-system.md).

-   **[Set up Contact Tracing properties](../task/configure-contact-tracing-properties.md)**  
Configure system properties to adjust how contact tracing data is used.
-   **[Domain separation and Contact Tracing](contact-tracing-domain-separation.md)**  
Domain separation is supported for the ServiceNow® Contact Tracing application. The application helps organizations reduce workplace transmission of infectious diseases, such as COVID-19, by identifying anyone on site who might have been in contact with an affected person.
-   **[Modify the scheduled data import job](../task/configure-badge-sched-import-job.md)**  
As an administrator, review and modify the scheduled data import jobs used for importing badge access and Wi-Fi access data from an Excel file into the Contact Tracing application.
-   **[Configure the time zone setting for badge and daily log data](../task/add-script-include-contact-tracing.md)**  
 Add a script include in the Global scope to consider the affected user's time zone when you run a diagnostic request using the badge reader or user daily log data source.
-   **[Configure an email notification for the daily contact log](../task/add-daily-log-notification.md)**  
Configure a custom email notification to use with Emergency Outreach notifications so you can request that users submit a list of other users they came in contact with throughout the workday.
-   **[Configure an Emergency Outreach notification for the daily contact log](../task/configure-outreach-notif-daily-log.md)**  
As an administrator, create or configure the Emergency Outreach notification to send email and mobile push notifications to employees to ask them to submit a list of co-workers whom they have interacted with on a given day.
-   **[Configure Contact Tracing data retention settings](../task/configure-contact-tracing-data-retention.md)**  
Configure the data retention settings for the data collected for contact tracing such as badge swipe data, employee daily contact logs, and cases.
-   **[Create a requirement for potentially exposed contacts to return to work](../task/create-exposed-contacts-requirement.md)**  
Create a requirement for potentially exposed employees to meet to verify that they are eligible to return to work.
-   **[Create a requirement for employees to acknowledge the privacy consent request](../task/create-privacy-consent-requirement.md)**  
Create a requirement for your employees to respond to the privacy consent request before entering the workplace to facilitate the use of their data for contact tracing.
-   **[Configure an email notification for an exposure notice](../task/configure-notify-exp-contact-email.md)**  
Configure an email notification to use in the Emergency Outreach to send to potentially exposed contacts in an exposure case to notify them of potential exposure from an affected employee.
-   **[Configure an Emergency Outreach notification for the exposure notice](../task/configure-outreach-notify-exp-contact.md)**  
Configure an Emergency Outreach notification to send email and mobile push notifications to potentially exposed employees in an exposure case to notify them of a potential exposure from an affected employee.
-   **[Configure contact tracing visualization to show vaccination status](../task/add-vaccination-status-to-case-visualization.md)**  
Configure Contact Tracing so case managers can view the vaccination status of potentially exposed contacts in the contact tracing visualization.
-   **[Setting up data privacy consent settings for Contact Tracing](set-up-privacy-consent-settings.md)**  
As an admin, you can configure privacy consent templates, location-based privacy configurations, email notifications, and outreach notifications for sending privacy consent alerts in Contact Tracing.
-   **[Map handheld computing devices assigned to employees](../task/add-user-handheld-devices.md)**  
Map handheld computing devices that are assigned to employees and running the Zebra MotionWorks software to record proximity logs for contact tracing using those devices.
-   **[Configure KINEXON integration](../task/configure-kinexon-integration.md)**  
Configure Contact Tracing and enable the KINEXON SafeZone tracing system to use data from KINEXON wearable devices in diagnostic requests. This data enables the identification of potentially exposed contacts based on the interactions and proximity of users with KINEXON wearable devices.
-   **[Virtual Agent conversations for Contact Tracing](contact-tracing-va-sms.md#)**  
Contact Tracing provides a Virtual Agent conversation to assess the health of potentially exposed contacts via SMS.

**Parent Topic:**[Contact Tracing](contact-tracing.md)

