---
title: Employee Readiness Surveys
description: The ServiceNow Employee Readiness Surveys application lets you evaluate the readiness of your workforce to return to the workplace by asking users to complete a survey.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Safe Workplace, Health and Safety, Employee Service Management]
---

# Employee Readiness Surveys

The ServiceNow® Employee Readiness Surveys application lets you evaluate the readiness of your workforce to return to the workplace by asking users to complete a survey.

Employee Readiness Surveys is an application that you install to use with Emergency Outreach. For information about Emergency Outreach and how surveys are sent via outreach notifications, see [Emergency Outreach](emergency-outreach.md).

After you install the application, the check-in administrator for Emergency Outreach can view and edit the survey questions to suit your needs. New surveys can be added, for example, to evaluate users in different regions or address other concerns.

The check-in administrator sends the surveys to targeted audiences using the Emergency Outreach notification methods.

-   **Use guided setup to implement Safe Workplace suite apps**

    The Safe Workplace guided setup provides a sequence of tasks that help you configure the Safe Workplace and Emergency Response Management applications on your ServiceNow instance. To open the Safe Workplace guided setup, navigate to **Guided Setup** &gt; **Safe Workplace Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).


## Use with other Safe Workplace suite applications

Employee Readiness Surveys is part of a suite of ServiceNow® Safe Workplace suite applications. Use it with these other applications to help your organization prepare its workforce and workplaces to resume operations after emergencies and pandemics like COVID-19.

-   Before users re-enter workspaces, use the [Employee Health Screening](../../employee-health-screening/concept/employee-health-screening.md) application to screen users and ensure compliance with your entry requirements, such as a temperature check and PPE.
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
</table>## Domain separation for the Employee Readiness Surveys application

Surveys are configured and managed through the Survey Management application on your ServiceNow instance. For information about how domain separation is supported, see [Domain separation for Survey Management](https://www.servicenow.com/docs/access?context=domain-separation-surveys&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to employees of government agencies in their individual capacities. Use of this application is being offered free of charge for a limited or extended time period and with no expectation of payment from the government agency to ServiceNow for use during that time period, nor does usage create an actual or implied future obligation on behalf of the government. ServiceNow hereby expressly waives any future claims for payment from the agency in connection with usage of the application. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

-   **[Install Employee Readiness Surveys](../task/emp-readiness-survey-install.md)**  
You can install Employee Readiness Surveys if you have the admin role. Installing Employee Readiness Surveys adds notification options and a default health readiness survey to the Emergency Outreach app.
-   **[Configure Employee Readiness Surveys notifications](../task/config-employee-readiness-survey.md#)**  
The administrator can add or modify Employee Readiness Surveys notifications. Users with the sn\_imt\_checkin.checkin\_admin or survey\_admin role can view the base system survey and copy it to make changes, or add a new survey.
-   **[Configure Employee Readiness Surveys](../task/config-emp-readiness-survey.md#)**  
Review the default Employee workplace readiness survey installed with the Employee Readiness Surveys app. Modify the survey, or create one or more surveys to use based on the readiness concerns that you want to address and any legal obligations under applicable law, including data protection laws.

**Parent Topic:**[Safe Workplace](../../human-resources/concept/safe-workplace.md)

