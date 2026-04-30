---
title: Incident Communications Management and Contacts
description: You can define contacts to associate users or groups to an incident communication plan. The users or groups are contacted to complete the tasks included in a communication plan.
locale: en-US
release: yokohama
product: Incident Communications Management
classification: incident-communications-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage, Incident Communications Management, IT Service Management]
---

# Incident Communications Management and Contacts

You can define contacts to associate users or groups to an incident communication plan. The users or groups are contacted to complete the tasks included in a communication plan.

If you have the ia\_admin role, you can assign users or groups to an incident communication plan based on the information provided in these records:

-   Contact responsibilities: Provides a name, such as Incident Duty Manager, for a set of tasks related to incident communication plan. The contact responsibility record also indicates whether the tasks are performed by an individual user or a group of users. Contact responsibilities can also be used to manually add contacts to an incident communication plan.
-   Contact definitions: Identifies a set of conditions to determine which specific user or group is assigned to handle a particular responsibility for an incident communication plan. For example, All P1 Incidents must have an Incident manager, assigned to US Incident Management group.

Contact responsibilities and contact definitions allow you to define and modify data-driven contact information for automatic notifications. You do not have to specify individual users or groups directly for each incident communication plan.

You can use group contacts. You can use the Group contacts functionality when you have on-call scheduling, Notify, and Incident Communications Management. Group contacts include the people that are on-call. The group contacts can be included when initiating a conference call that is a result of an incident communication plan. By default, the primary and secondary on-call persons are available. To modify this behavior, set the system property **com.snc.iam.on\_call\_escalation\_level**.

-   **[Responsibilities for Incident Communication Plan](../reference/r_ResponsibilitiesForIncidentAlerts.md)**  
Contact responsibilities helps you to identify contacts by their responsibilities and to understand what you can expect from the user throughout the life cycle of the communication plan.
-   **[Define contact responsibilities](../task/t_CreateAContactResponsibility.md)**  
Define the different contacts or target audience involved in the communication process and their responsibility to understand the expectations from those contacts throughout the process.
-   **[Create a contact definition](../task/t_CreateAContactDefinition.md)**  
Define the recipients of a particular incident communication plan to determine the target audience involved in each communication task and the responsibilities the recipients are expected to handle.
-   **[Create a default override](../task/t_CreateADefaultOverride.md)**  
Create a default override to specify user or group for a contact definition of an incident communication plan. It helps you to set multiple conditions based on which a user or a group is considered as a contact.
-   **[Add a user as a contact](../task/t_AddAContactManually.md)**  
Add a user to a communication plan if you have not added the user earlier in the contact. You can assign a communication task to the user to resolve an issue.

**Parent Topic:**[Managing Incident Communications](working-with-inci-comm-mgmt.md)

