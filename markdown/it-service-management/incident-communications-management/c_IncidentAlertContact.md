---
title: Incident Communications Management and contacts
description: You can define contacts to associate users or groups with an incident communication plan. The users or groups are contacted to complete the tasks included in a communication plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/c\_IncidentAlertContact.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing incident communications, Incident Communications Management, IT Service Management]
---

# Incident Communications Management and contacts

You can define contacts to associate users or groups with an incident communication plan. The users or groups are contacted to complete the tasks included in a communication plan.

If you have the ia\_admin role, you can assign users or groups to an incident communication plan based on the information provided in these records:

-   Contact responsibilities: Provides a name, such as Incident Duty Manager, for a set of tasks related to incident communication plan. The contact responsibility record also indicates whether the tasks are performed by an individual user or a group of users. You can also use contact responsibilities to manually add contacts to an incident communication plan.
-   Contact definitions: Identifies a set of conditions to determine which specific user or group is assigned to handle a particular responsibility for an incident communication plan. For example, all priority 1 \(P1\) incidents must have an incident manager assigned to the US Incident Management group.

Contact responsibilities and contact definitions enable you to define and modify data-driven contact information for automatic notifications. You don't have to specify individual users or groups directly for each incident communication plan.

You can use group contacts when you have on-call scheduling, Notify, and Incident Communications Management. Group contacts include the people who are on call. The group contacts can be included when initiating a conference call that is a result of an incident communication plan. By default, the primary and secondary on-call persons are available. To modify this behavior, set the system property **com.snc.iam.on\_call\_escalation\_level**.

-   **[Contact responsibilities for incident communication plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/r_ResponsibilitiesForIncidentAlerts.md)**  
Contact responsibilities identify the contacts for an incident communication plan and define the role that each contact plays throughout the plan life cycle.
-   **[Define contact responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/t_CreateAContactResponsibility.md)**  
Define the contacts involved in the communication process and their responsibilities, so that it's clear what's expected of each contact throughout the process.
-   **[Create a contact definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/t_CreateAContactDefinition.md)**  
Define the recipients of a particular incident communication plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle.
-   **[Create a default override](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/t_CreateADefaultOverride.md)**  
Create a default override to specify the user or group for a contact definition in an incident communication plan. Use multiple conditions to determine which user or group becomes the contact.
-   **[Add a user as a contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/t_AddAContactManually.md)**  
Add a user as a contact on an incident communication plan when the user isn't already a contact. You can then assign a communication task to the user to help resolve an issue.

**Parent Topic:**[Managing incident communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/working-with-inci-comm-mgmt.md)

