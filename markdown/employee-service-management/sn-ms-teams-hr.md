---
title: HR Service Delivery integration with Microsoft Teams and Microsoft 365
description: HR Service Delivery integration with Microsoft Teams extends the Now Virtual Agent integration with Microsoft Teams to enable employees to more effectively request and receive service from within Microsoft Teams.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration for Employee Experience, Explore, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# HR Service Delivery integration with Microsoft Teams and Microsoft 365

HR Service Delivery integration with Microsoft Teams extends the Now Virtual Agent integration with Microsoft Teams to enable employees to more effectively request and receive service from within Microsoft Teams.

The HR Service Delivery integration with Microsoft Teams application extends the [Now Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) integration and includes the following additional capabilities:

-   Actionable notifications – for approval and comments on tickets. Users can take action on the notifications from within Microsoft Teams.

    Ticket comments: Employees are able to respond to notifications on the tickets from within Microsoft Teams.

    This `respond_to_comment_notification_inclusion_list_for_hr` property specifies the HR tables for which the **Respond to Comments** notification triggers. &lt;HR services&gt;

    -   sn\_hr\_core\_case\_total\_rewards
    -   sn\_hr\_core\_case\_global\_mobility
    -   sn\_hr\_core\_case\_operations
    -   sn\_hr\_core\_case\_performance
    -   sn\_hr\_core\_case\_benefits
    -   sn\_hr\_core\_case\_workforce\_admin
    -   sn\_hr\_core\_case\_talent\_management
    -   sn\_hr\_core\_case\_corporate\_communication
    -   sn\_hr\_core\_case\_payroll,
    -   sn\_hr\_core\_case\_compensation.
-   Provides agents the ability to initiate a Microsoft Teams chat with an employee from an HR case and then to copy the chat transcript back to the ticket as a comment.
    -   sn\_now\_teams\_hr.chat\_sn\_hr\_core\_case\_fields

        This system property contains the list of HR Case table fields that will be shown as recommended participants for "Start Chat" feature. By default, the recommended participants contain the participants comprising of "opened\_for", "subject\_person", "collaborators" fields.

    -   sn\_now\_teams\_hr.chat\_sn\_hr\_core\_task\_fields

        This system property contains the list of HR Task table fields that will be shown as recommended participants for "Start Chat" feature. By default, the recommended participants contain the participant defined in "assigned\_to" field.

    -   sn\_now\_teams\_hr.hr\_case\_allow\_list\_for\_teams\_chat\_actions

        This system property contains the list of HR Case tables for which "Start Chat" and "Import Messages" UI Action. By default, this list does not include highly sensitive HR Cases such as "Employee Relations", "Investigation", and "Ethics" cases.

    -   sn\_now\_teams\_hr.respond\_to\_comment\_notification\_inclusion\_list\_for\_hr

        This system property contains the list of HR Case tables for which "Respond to Comment" actionable notifications will be sent. By default, this list does not include highly sensitive HR Cases such as "Employee Relations", "Investigation", and "Ethics" cases.


**Note:** Approvals for HR cases and Approvals with e-Signature are not yet supported for HR Service Delivery with Microsoft Teams.

|Feature|License Requirements|
|-------|--------------------|
|Actionable Notifications|HR Pro or above|
|Chat - Agent to Employee/Agent to Agent|HR Pro or above|
|Employee Center|HR Standard or above|

You must perform the following activities to integrate HR Service Delivery with Microsoft Teams in ServiceNow instance:

1.  [Install HR Service Delivery integration with Microsoft Teams application](../task/install-hr-ms-teams-plugin.md)
2.  [Setting up the ServiceNow instance for Microsoft Teams integration](setup-tenants.md)

To configure HR Service Delivery integration with Microsoft Teams in ServiceNow instance, see [Configure HR Service Delivery integration with Microsoft Teams](sn-ms-teams-config-hr.md).

To manage HR Service Delivery integration with Microsoft Teams in ServiceNow instance, see [Customize HR Service Delivery integration with Microsoft Teams](customize-sn-ms-teams-hr.md).

To use HR Service Delivery integration with Microsoft Teams in ServiceNow instance, see [Use ITSM and HRSD integrations with Microsoft Teams](user-sn-ms-teams.md).

**Parent Topic:**[Explore Microsoft Teams and Microsoft 365 integration for Employee Experience](c_employee_experience.md)

**Related topics**  


[IT Service Management integration with Microsoft Teams and Microsoft 365](sn-ms-teams.md)

[Universal Request integration with Microsoft Teams](sn-ms-teams-ur.md)

