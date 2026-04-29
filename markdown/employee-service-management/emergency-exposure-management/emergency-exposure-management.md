---
title: Emergency Exposure Management
description: The ServiceNow Emergency Exposure Management application helps identify users who might have been exposed to infectious diseases by analyzing multiple data sources such as meetings, location, shifts, Wi-Fi access logs, and badge scans of affected users.
locale: en-US
release: australia
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Emergency Response Management, Employee Service Management]
---

# Emergency Exposure Management

The ServiceNow® Emergency Exposure Management application helps identify users who might have been exposed to infectious diseases by analyzing multiple data sources such as meetings, location, shifts, Wi-Fi access logs, and badge scans of affected users.

Emergency Exposure Management provides tracing systems to use the following data sources to generate a list of potentially exposed users:

-   Microsoft Office 365 meeting invite
-   Location of the ServiceNow user profile
-   Workspace reservation
-   Badge scan log
-   Wi-Fi access log
-   Employee daily log
-   Field service task
-   Visitors log
-   Handheld or wearable device proximity sensing data

**Note:** Some of the tracing systems require you to install other Safe Workplace suite and Emergency Response Management applications. For more information, see [Tracing systems in Emergency Exposure Management](tracing-systems-exposure-mgnt.md).

You can also manually add users whom you know might have been potentially exposed to an affected user.

In addition to using the base system tracing systems, you can set up a tracing system that uses your own data source to identify potentially exposed users. For more information, see [Set up a tracing system for an exposure data source](../task/set-up-tracing-system.md).



-   **Use guided setup to implement Safe Workplace suite apps**

    The Safe Workplace guided setup provides a sequence of tasks that help you configure the Safe Workplace and Emergency Response Management applications on your ServiceNow instance. To open the Safe Workplace guided setup, navigate to **Guided Setup** &gt; **Safe Workplace Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).


## Use with other Emergency Response Management applications

Emergency Exposure Management was originally developed to monitor and aid in stopping the community spread of infectious diseases, such as COVID-19 among users. It is part of a suite of ServiceNow® Emergency Response Management applications built on the ServiceNow AI Platform® to assist companies in their emergency response efforts. You can also enable users to self-report their health status through the [Emergency Outreach](emergency-outreach.md) and [Emergency Self Report](emergency-self-report.md) applications, which are both available in the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do).

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

-   **[Install Emergency Exposure Management](../task/install-emergency-exposure-mgt.md)**  
You can install Emergency Exposure Management if you have the admin role.
-   **[Set up Emergency Exposure Management](../task/set-up-emergency-exposure-mgmt.md)**  
 After installing the Emergency Exposure Management application, set up tracing system for your data sources, diagnostic request task configuration, and register Microsoft applications.
-   **[Identify potentially exposed users](../task/use-emergency-exposure-mgnt.md)**  
When a user has indicated a health condition on a self-report, use Emergency Exposure Management to identify other users who might have come in contact with the affected user. You can analyze multiple data sources, such as location, meetings, workspace reservations, badge scans, and Wi-Fi access data of the affected user to identify potentially exposed users.
-   **[Domain separation for Emergency Exposure Management](../reference/emergency-exposure-management-domain-separation.md)**  
The following table lists the domain separation use cases for service providers \(SPs\) using this application.

**Parent Topic:**[Emergency Response Management](emergency-response-management.md)

