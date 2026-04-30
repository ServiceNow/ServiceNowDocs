---
title: Employee Health Screening
description: Screen users before entering the workplace to ensure compliance with the organization's entry requirements, such as a temperature check and PPE. Require that users agree to comply with health and safety policies before they return to the workplace.
locale: en-US
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Safe Workplace, Health and Safety, Employee Service Management]
---

# Employee Health Screening

Screen users before entering the workplace to ensure compliance with the organization's entry requirements, such as a temperature check and PPE. Require that users agree to comply with health and safety policies before they return to the workplace.

The ServiceNow® Employee Health Screening application enables organizations to screen users before entering the workplace to ensure compliance with the organization's entry requirements, such as a temperature check and personal protective equipment \(PPE\). Based on their own criteria, organizations can determine whether it’s safe for the user to enter the workplace. Organizations can use a reporting dashboard  to view trends by sites and record the return of users into  their  facilities.

![Screen employees for fever and PPE before allowing them to enter the workplace](../image/health-screen-overview.png)

-   **Use guided setup to implement Safe Workplace suite apps**

    The Safe Workplace guided setup provides a sequence of tasks that help you configure the Safe Workplace and Emergency Response Management applications on your ServiceNow instance. To open the Safe Workplace guided setup, navigate to **Guided Setup** &gt; **Safe Workplace Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


## Integrate with Customer Service Management

Use ServiceNow® Customer Service Management and Employee Health Screening together to provide consumers and contacts with access to a health verification form on your Consumer or Customer Service Portals. Conduct health screenings for consumers and contacts before they can be granted entry to a location. For more information about using Customer Service Management with Employee Health Screening, see [Integrate Customer Service Management with Safe Workplace applications](https://www.servicenow.com/docs/access?context=csm-integration-safe-workplace&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Use with other Safe Workplace suite applications

Employee Health Screening is part of a suite of ServiceNow® Safe Workplace suite applications. Use it with these other applications to help your organization prepare its workforce and workplaces to resume operations after emergencies and pandemics like COVID-19.

-   With the [Employee Readiness Surveys](../../business-continuity/concept/employee-readiness-surveys.md) application, evaluate the readiness of your users to return to the workplace by asking them to fill in a survey.
-   With the [Emergency Outreach](../../business-continuity/concept/emergency-outreach.md) application, notify employees of important information about anticipated or occurring emergency situations. Send an outreach notification via email, mobile push message, or SMS message to request an employee response. You can also configure other preferred communication channels.
-   With the [Explore Workplace Core](../../workplace-service-delivery/concept/workplace-service-delivery-overview.md) application, prepare for the return of users by configuring and maintaining clean and socially distanced workspaces for them to use.
-   You can manage the inventory of safety equipment for your workforce with the [Workplace Personal Protective Equipment Inventory Management](../../ppe-inventory-management/concept/ppe-inventory-management.md) application.

All Safe Workplace suite applications are available in the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Safe Workplace suite for federal customers

Federal customers using IL4 or FedRAMP environments will see the Safe Workplace suite applications ready and available to install on their nonproduction instances without having to make any special requests. Licenses are required to use Safe Workplace suite applications on production instances. Customers are responsible for configuring the apps to meet U.S. federal regulations and guidelines.

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

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to employees of government agencies in their individual capacities. Use of this application is being offered free of charge for a limited or extended time period and with no expectation of payment from the government agency to ServiceNow for use during that time period, nor does usage create an actual or implied future obligation on behalf of the government. ServiceNow hereby expressly waives any future claims for payment from the agency in connection with usage of the application. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

-   **[Install Employee Health Screening](../task/install-emp-health-screening.md#)**  
You can install the Employee Health Screening application if you have the admin role. This application includes demo data and installs the related store applications and plugins if they are not already installed.
-   **[Configure Employee Health Screening](../task/configure-health-screening.md#)**  
Set properties to specify the global maximum temperature thresholds in Fahrenheit and Celsius. Temperatures taken during a health screening are compared to the global temperature threshold, established by the company, to allow or deny entry.
-   **[Add message for users during health screening](../task/add-screening-information-message.md)**  
Add an optional custom message for people to read during their health screenings with additional information or guidelines.
-   **[Add an email notification for daily health verification](../../business-continuity/task/add-daily-health-verification-notif.md)**  
Add an Employee Readiness Surveys email notification to use for sending the survey link.
-   **[Verify your health status and compliance](../task/agree-compliance-return.md)**  
Verify that you understand and will comply with your organization's safety requirements and policies before you can be allowed entry to the location.
-   **[Conduct a health screen for entry](../task/screen-returning-employee.md)**  
Use a health screen to verify a person's return requirement status to determine whether the person is able to enter the location.
-   **[Screen a visitor for entry to the workplace](../task/screen-visitor.md)**  
Verify the visitor's entry requirement status on your smartphone, tablet, or computer. Then complete and submit the health screening form to determine whether the visitor is able to enter the workplace.
-   **[Monitor progress with the Employee Health Screen Overview dashboard](../task/view-health-screen-dashboard.md)**  
View the dashboard to monitor the entry requests and assess how the return to the workplace is progressing. Evaluate the number of entry requests, how many requests were denied entry, and for what reason.
-   **[View entry requests](../task/view-entry-requests.md)**  
Filter the list of entry requests that were completed to evaluate different areas of your return to work progress. Entry requests are the records submitted by the health screener for each employee who is screened before entry.

**Parent Topic:**[Safe Workplace](../../human-resources/concept/safe-workplace.md)

