---
title: Emergency Self Report
description: During a crisis, the ServiceNow Emergency Self Report application gives users a way to notify their organization of their health status. It also provides a workflow for qualified users to safely return to work. Managers and response teams can track user reporting.
locale: en-US
release: zurich
product: Emergency Self Report
classification: emergency-self-report
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Emergency Self Report

During a crisis, the ServiceNow® Emergency Self Report application gives users a way to notify their organization of their health status. It also provides a workflow for qualified users to safely return to work. Managers and response teams can track user reporting.

In contrast to email or phone reporting and manual data consolidation, Emergency Self Report provides a digital workflow that captures and automatically rolls up user reporting data for analysis and action. The application offers benefits for various people within the organization, with different views displayed for various roles.

-   **Use guided setup to implement Safe Workplace suite apps**

    The Safe Workplace guided setup provides a sequence of tasks that help you configure the Safe Workplace and Emergency Response Management applications on your ServiceNow instance. To open the Safe Workplace guided setup, navigate to **Guided Setup** &gt; **Safe Workplace Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


## Users can report their status

A menu-driven interface enables users to report their status to their managers. Users can use the same interface to update their manager and global response team when they are ready to return to work. Managers can notify users when they may return.

![Users can self-report and select their health status](../image/employee-self-report-employee-view.png "User view")

If ServiceNow® [Contact Tracing](../../contact-tracing/concept/contact-tracing.md) is installed, a case is created automatically for a user who self-reports as being in quarantine. If an active case exists for the user at the time of reporting, a note is added to the case for the self-reporting.

## Managers can monitor the status of their teams

Managers can view a summary of their team’s reported status and the details of an individual person. They can reassign an affected user’s work to others on the team if the work is tracked in the ServiceNow instance. If users don't have access to the application, the manager can submit a report on their behalf.

![Managers can see status for all direct reports, and see what tasks they need to reassign](../image/employee-self-report-dashboard-manager-view-fullscreen.png "Manager view")

## Response teams can view the status of all teams

Response teams can view an overview dashboard that summarizes the status for all self-reported users. Data can be viewed and sorted in multiple ways for analysis and action.

![Response team overview dashboard with customization options for at-a-glance status](../image/esr-overview-dashboard.png "Response team view")

## Response team can work with HR tasks

HR tasks are created when a user self-reports. Each HR task is associated with a self-reported crisis task. The response team member can navigate to **Emergency Self Response** &gt; **HR tasks** to view the list.

![HR task list](../image/esr-hr-tasks-list-import-tasks.png "HR tasks")

HR tasks do not have a specific workflow associated with them. They are created in the Open state, and closing the associated crisis task does not affect the HR task. Your organization can determine how to use or manage HR tasks, if at all. Review the HR task form to determine whether it can be of use within your response strategy.

## Use with other Emergency Response Management applications

Emergency Self Report was originally developed to monitor and aid in stopping the community spread of COVID-19 among users. It is part of the suite of ServiceNow® Emergency Response Management applications built on the ServiceNow AI Platform® to assist companies in their emergency response efforts. With the [Emergency Exposure Management](emergency-exposure-management.md) application, you can identify users who might have been exposed. You can then contact affected users through the [Emergency Outreach](emergency-outreach.md) application. Both applications are available in the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

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

-   **[Set up Emergency Self Report](../task/set-up-emergency-self-report.md#)**  
To set up Emergency Self Report, install the application. Then configure user access, a dedicated knowledge base, and system properties.
-   **[Report and track health statuses during an emergency](../task/use-emergency-self-report.md)**  
Emergency Self Report is used by users to self-report their health status, by managers to track the health status of their users, and by response teams to view the status for all users and sort the data for analysis and action.
-   **[View self-reported user HR tasks](../task/view-hr-tasks-response-team.md)**  
Members of the emergency response team can view all user reports and associated HR tasks on the Emergency Self Report overview dashboard.
-   **[Import Crisis Task data](../task/import-crisis-task-data.md)**  
As a crisis task administrator, upload a spreadsheet of self-reported health statuses to create crisis tasks in bulk.
-   **[Domain separation for Emergency Self Report](../reference/emergency-self-report-domain-separation.md)**  
The following table lists the domain separation use cases for service providers \(SPs\) using this application.

**Parent Topic:**[Emergency Response Management](emergency-response-management.md)

