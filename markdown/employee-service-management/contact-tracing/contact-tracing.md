---
title: Contact Tracing
description: The ServiceNow Contact Tracing application helps organizations reduce workplace transmission of infectious diseases, such as COVID-19, by identifying any on-site users who might have been in contact with an affected user. The user receives updates about the number of reported cases or symptoms in the location. A list of potentially exposed users is created from various data inputs, such as badge scans, Wi-Fi access logs, and daily contact logs.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Safe Workplace, Health and Safety, Employee Service Management]
---

# Contact Tracing

The ServiceNow® Contact Tracing application helps organizations reduce workplace transmission of infectious diseases, such as COVID-19, by identifying any on-site users who might have been in contact with an affected user. The user receives updates about the number of reported cases or symptoms in the location. A list of potentially exposed users is created from various data inputs, such as badge scans, Wi-Fi access logs, and daily contact logs.

## Features

In Contact Tracing version 1.29.4. and above, the navigation path is not available in the Application search context menu \(**All** &gt; **Contact Tracing**\) for Zebra and Devvio. The navigation path is available if you are using Contact Tracing 1.29.2 and later versions.

-   Identify on-site users who may have been in contact with a potentially infected user.
-   Aggregate contact tracing information across workplace locations, work shifts and reservations, badge scans, Wi-Fi access logs, and self-reporting logs to enhance search criteria.
-   Identify potential user interactions with a user using the Wi-Fi access data by correlating who connected to the same Wi-Fi network using laptops, mobile devices, or Bluetooth LE devices. You can get the Wi-Fi access data by manual import or through integration with Mist Systems or Cisco DNA Spaces.

-   Get the contact tracing data of users who use handheld or wearable devices at the workplace. You can import the contact tracing report from Zebra MotionWorks Portal.
-   Monitor risk scores of users who use wearable devices at the workplace. You can import risk score reports with Devvio integration.
-   Create outreach cases and tasks for follow-up interviews with potentially impacted users.
-   Assess the status of potentially exposed contacts and their next two levels of potential exposures from within a case using visualization.
-   Maintain the data privacy of users, in the context of contact tracing by obtaining their consent.
-   Use data retention settings to determine when the data collected for contact tracing is automatically deleted from the system.

![Identify potential exposures from affected users to minimize transmission of infectious diseases at the workplace](../image/contact-tracing-overview.png)

-   **Use guided setup to implement Safe Workplace suite apps**

    The Safe Workplace guided setup provides a sequence of tasks that help you configure the Safe Workplace and Emergency Response Management applications on your ServiceNow instance. To open the Safe Workplace guided setup, navigate to **Guided Setup** &gt; **Safe Workplace Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).


## Use with other ServiceNow® Safe Workplace suiteand applications

The Contact Tracing application provides enhanced capabilities and additional features with other Safe Workplace suite applications.

-   Emergency Outreach: Configure and send email and mobile notifications to users requesting them to submit [daily contact logs](employee-daily-log.md) and to get [responses for privacy consents](contact-tracing-user-privacy-options.md).
-   Emergency Exposure Management: Run a diagnostic report on affected users to identify potentially exposed users who might have interacted with the affected user. You can use multiple data sources to broaden the coverage of finding potential exposure. Review [tracing systems](../../business-continuity/concept/tracing-systems-exposure-mgnt.md) for data sources provided by Contact Tracing to see whether these tracing systems meet your business needs. You can modify these tracing systems or set up a new tracing system for your data source. For more information, see [Set up a tracing system for an exposure data source](../../business-continuity/task/set-up-tracing-system.md).
-   Safe Workplace Dashboard: View the trend of active cases and potentially exposed contacts over a given time period for a campus or location. You can also get alerts to determine when the number of active cases is higher than the threshold in a particular campus or location.
-   Emergency Self Report: A case is created automatically for a user who is reported to be in quarantine if no active case exists for the user at the time of reporting.
-   Employee Readiness Core:
    -   Automatically adds or updates a user's health and safety requirement status when a user is identified as a potentially exposed contact in a case. This up-to-date information helps you evaluate the readiness of your potentially exposed users to return to the workplace.
    -   Automatically adds or updates a user's privacy consent requirement status when a user responds to the privacy consent request. This up-to-date information helps you ensure that your users acknowledge the privacy consent before entering the workplace to facilitate contact tracing as desired.
-   Vaccination Status: Review a potentially exposed contact's vaccination status in the contact tracing visualization.

## Domain separation for the Contact Tracing application

The Contact Tracing application supports domain separation at the Standard\* level. For more information, see [Domain separation and Contact Tracing](contact-tracing-domain-separation.md). For a deeper understanding of the support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to employees of government agencies in their individual capacities. Use of this application is being offered free of charge for a limited or extended time period and with no expectation of payment from the government agency to ServiceNow for use during that time period, nor does usage create an actual or implied future obligation on behalf of the government. ServiceNow hereby expressly waives any future claims for payment from the agency in connection with usage of the application. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

-   **[Install Contact Tracing](../task/install-contact-tracing.md#)**  
You can install Contact Tracing if you have the admin role.
-   **[Setting up Contact Tracing](set-up-contact-tracing.md)**  
Configure system properties, scheduled jobs, script includes, Wi-Fi access log integration, and outreach notifications to aggregate contact tracing information for various data sources.
-   **[Maintaining user data privacy in Contact Tracing](contact-tracing-user-privacy-options.md)**  
The Contact Tracing application enables your organization to maintain the data privacy of all users given the high sensitivity of the data collected throughout the contact tracing process.
-   **[Collecting user badge data](badge-management.md)**  
In the Contact Tracing application, manage data for user badges and badge readers. Identify potentially exposed users who may have come in contact with affected users by importing their badge swipe data into the application.
-   **[Collecting risk scores in Contact Tracing](contact-tracing-collect-risk-scores.md)**  
Identify at-risk and potentially exposed users by importing and monitoring risk scores from their wearable devices and external systems.
-   **[Retrieving Wi-Fi access log data](wifi-access-management.md)**  

-   **[Tracking employee contacts using daily logs](employee-daily-log.md)**  
After employees start returning to the workplace, use daily contact logs to help promote the health and safety of all your employees. Let employees submit a list of other people with whom they come in contact during the day. Send mobile and email push notifications to employees to submit their contact log for the day.
-   **[Managing cases to follow up with potentially exposed contacts](exposure-case-management.md)**  
When an employee who returns to the workplace is classified as positive for a condition, such as COVID-19, the case manager creates a case to identify and follow up with potentially exposed contacts.

**Parent Topic:**[Safe Workplace](../../human-resources/concept/safe-workplace.md)

