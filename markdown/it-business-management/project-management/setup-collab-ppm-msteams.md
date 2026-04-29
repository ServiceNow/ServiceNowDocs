---
title: Setting up PPM collaboration for Microsoft Teams
description: Integrate your ServiceNow instance with your organization's Microsoft Teams to enable collaboration of your projects in Microsoft Teams.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaborate with your project teams using PPM Collaboration application, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Setting up PPM collaboration for Microsoft Teams

Integrate your ServiceNow instance with your organization's Microsoft Teams to enable collaboration of your projects in Microsoft Teams.

PPM Collaboration uses the Microsoft Teams Graph and Microsoft Azure AD spoke actions such as creating a team for your project, adding or removing your project team members, archiving the team when the project is closed, posting a message when a record is updated, and so on. To enable these spoke actions, you must integrate your ServiceNow instance with Microsoft Teams Graph and Microsoft Azure AD to authenticate ServiceNow requests. For more information, see the [Set up Microsoft Teams Graph spoke](https://www.servicenow.com/docs/access?context=set-up-msteams&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [Set up Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=set-up-azure&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) topics.

**Important:** When you activate the Microsoft Teams Graph and Microsoft Azure AD spokes, a [Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US) for Microsoft Teams Graph and Microsoft Azure AD is created by default with the IDs **sn\_msteams\_ahv2.Microsoft\_Teams\_Spoke** and **sn\_azure\_ad\_spoke.AzureAD** respectively. The connection that is active \(the Active field is set to **true**\) in Connections related list of this alias uses this default ID to connect your ServiceNow instance to Microsoft Teams Graph and Microsoft Azure AD. Therefore, you can have multiple connections associated with this alias but ensure that only one connection is active at any given time.

**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

