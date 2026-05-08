---
title: Emergency Outreach
description: Notify users of important information about anticipated or occurring emergency situations. Send an outreach notification via email, mobile push message, or SMS message to request a user response. You can also configure other preferred communication channels.
locale: en-US
release: australia
product: Emergency Outreach
classification: emergency-outreach
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Emergency Response Management, Employee Service Management]
---

# Emergency Outreach

Notify users of important information about anticipated or occurring emergency situations. Send an outreach notification via email, mobile push message, or SMS message to request a user response. You can also configure other preferred communication channels.

Emergency Outreach was developed with other ServiceNow® Emergency Response Management apps to monitor and aid in stopping the community spread of infectious diseases, such as COVID-19 among users. With the release of additional ServiceNow® Safe Workplace suite apps, companies are able to manage an emergency situation from the outbreak through the reopening of the workplace.

Some of the Safe Workplace suite apps leverage the Emergency Outreach notification feature to communicate with users.

-   [Employee Readiness Surveys](employee-readiness-surveys.md) provides an outreach notification with a link to a survey to assess user readiness to return to the workplace. Customize the notification and the survey to address your company’s concerns.
-   [Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md) uses outreach notifications to request that users submit their health status verification each day before they can return to the workplace.
-   [Contact Tracing](../../contact-tracing/concept/contact-tracing.md) uses the following outreach notifications:
    -   An outreach notification to request that users in the workplace provide a list of users that they were in contact with throughout the day. The daily log notification can be scheduled and sent at a certain time every workday or as needed. Keeping daily logs enables contact tracers to follow up with impacted users when a user is affected.
    -   An outreach notification to request that users review the organization's privacy policy and provide their consent to use their data for contact tracing.

    -   An outreach notification to potentially exposed contacts in an exposure case to notify them that they might have been potentially exposed to an affected user at the workplace.

**Note:** Safe Workplace suite apps require a subscription. Install Emergency Outreach first, then install the Safe Workplace suite app.

-   **Use guided setup to implement Safe Workplace suite apps**

    The Safe Workplace guided setup provides a sequence of tasks that help you configure the Safe Workplace and Emergency Response Management applications on your ServiceNow instance. To open the Safe Workplace guided setup, navigate to **Guided Setup** &gt; **Safe Workplace Guided Setup**. For more information about using the guided setup interface, see Using guided setup.


## Use with other Emergency Response Management applications

The Emergency Response Management applications, built on the ServiceNow AI Platform®, assist organizations in their emergency response efforts. With the [Emergency Exposure Management](emergency-exposure-management.md) application, you can identify users who might have been exposed to affected users. Through the [Emergency Self Report](emergency-self-report.md) application, users can self-report their health status. Managers can track the health status of their direct reports so that work can be reassigned and response teams can monitor the overall data and trends. Both applications are available in the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Emergency Response Management for federal customers

Federal customers using IL4 or FedRAMP environments will see the Emergency Response Management applications ready and available to install on their instances without having to make any special requests. Customers are responsible for configuring the apps to meet U.S. federal regulations and guidelines.

<table id="table_kxr_yz3_blb"><thead><tr><th>

Type

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Commercial on-premise

</td><td>

Visit the ServiceNow® Store to download and install the application.

</td></tr><tr><td>

Federal hosted

</td><td>

See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

Federal on-premise

</td><td>

If you are a federal on-premise customer and you would like to install this application, reach out to your sales representative or open a Now Support or HIWAVE ticket. In the ticket, request to be routed to the SHOT team.

 See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

On-premise

</td><td>

See the [Commercial downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030258\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030258) article in the Store Help Center for more information.

</td></tr></tbody>
</table>## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations’ specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to employees of government agencies in their individual capacities. Use of this application is being offered free of charge for a limited or extended time period and with no expectation of payment from the government agency to ServiceNow for use during that time period, nor does usage create an actual or implied future obligation on behalf of the government. ServiceNow hereby expressly waives any future claims for payment from the agency in connection with usage of the application. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

-   **[Install Emergency Outreach](../task/install-emergency-outreach.md#)**  
You can install Emergency Outreach if you have the admin role.
-   **[Configure Emergency Outreach notifications](../task/configure-emergency-outreach.md)**  
A user with the admin role can add email notifications to use for any of the apps that communicate using Emergency Outreach. Each app provides a default email notification as an example to help with planning a new notification.
-   **[Modify or add Employee Readiness Surveys](../task/modify-emp-readiness-survey.md#)**  
Review the Employee workplace readiness survey that is installed with the Employee Readiness Surveys app. Modify the survey, or create one or more surveys to use based on the readiness concerns that you want to address and any legal obligations under applicable law, including data protection laws.
-   **[Send notifications for an emergency](../task/send-eo-notification-outreach.md)**  
Use Emergency Outreach to notify users to report their health status. Use Emergency Outreach also to quickly notify users of important information if there is an emergency.
-   **[Review Emergency Outreach acknowledgements](../task/eo-review-outreach-acks.md)**  
Review the list of acknowledgements from an outreach notification to see each employee's status. Resend the outreach notification to employees who did not respond.
-   **[Send notifications for daily health verification](../task/send-daily-health-verif-notif-outreach.md)**  
Use Emergency Outreach to notify users to report their daily health status.
-   **[Review daily health verification acknowledgements](../task/daily-health-verif-review-outreach-acks.md)**  
Review the list of acknowledgements from the daily health verification notification to see each user's status. Resend the outreach notification to users who did not respond.
-   **[Send a readiness survey and view responses](../task/send-eo-outreach-survey.md)**  
Use Emergency Outreach to send a workplace readiness survey. Review the survey responses to assist with your plans to reopen your workplace.
-   **[Report your health status](../task/emp-check-in-emergency-outreach.md)**  
If you receive an email, mobile push notification, or SMS notification to report your health status, you can update your status from the message.
-   **[Response scripts](response-scripts.md#)**  
Use response scripts to automatically take actions based on user responses to survey questions. Response scripts can be used to create or update records across any of the Emergency Response Management and Safe Workplace suite apps.
-   **[Domain separation for Emergency Outreach](../reference/emergency-outreach-domain-separation.md)**  
This application fully supports domain separation service provider \(SP\) use cases. The following table lists the domain separation use cases for service providers \(SPs\) using this application.

**Parent Topic:**[Emergency Response Management](emergency-response-management.md)

