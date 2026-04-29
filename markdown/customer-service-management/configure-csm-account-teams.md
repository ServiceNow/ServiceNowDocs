---
title: Creating an account team
description: Create an account team that is made up of both employees and customer contacts who fulfill the jobs or roles for a particular account in the Customer Service Management \(CSM\) application. By defining responsibilities or roles for your team and customer contacts, you confirm that your account team has the functions needed to support customer accounts.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create customer relationships, Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Creating an account team

Create an account team that is made up of both employees and customer contacts who fulfill the jobs or roles for a particular account in the Customer Service Management \(CSM\) application. By defining responsibilities or roles for your team and customer contacts, you confirm that your account team has the functions needed to support customer accounts.

If you have any one of the sn\_crm\_foundation\_admin, sn\_crm\_foundation\_data\_manager, and sn\_crm\_account\_relationship\_data\_manager roles, you can create an account team by using a responsibility definition. By defining the responsibilities that you need for this account team, you create the relationships between the different entities like the accounts, contacts, and more.If you have sn\_crm\_account\_relationship\_viewer or sn\_crm\_foundation\_data\_viewer role, you can view the Account team members table.

You can create two types of responsibility definitions. You can create a definition for an employee and a definition for a contact.

**Note:** If you have the sn\_crm\_customer\_access\_management\_admin or sn\_crm\_foundation\_admin role, you can also delete the definitions that are no longer used. A definition can only be deleted if it has no entries.

After these definitions or roles, are created, the sn\_customerservice\_manager can use these roles to do the following tasks:

-   Build an account team by selecting an account, selecting a role, and then assigning a role to an employee.
-   Add a contact relationship to an account by selecting an account, selecting a role, and then assigning a role to a contact.

The users who have been assigned to this role are displayed in the Account Team Members related list on the Responsibility Definition form. For more information, see the following topics:

-   [Create a responsibility definition](../task/t_CreateAResponsibilityDefinition.md)
-   [Configure access through the responsibility access configuration](../task/declarative-resposibility-framework.md)

