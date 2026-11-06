---
title: Setting up PPM collaboration for Microsoft Teams
description: Integrate your ServiceNow instance with your organization's Microsoft Teams to enable collaboration of your projects in Microsoft Teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/project-management/setup-collab-ppm-msteams.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Collaborate with your project teams using PPM Collaboration application, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Setting up PPM collaboration for Microsoft Teams

Integrate your ServiceNow instance with your organization's Microsoft Teams to enable collaboration of your projects in Microsoft Teams.

PPM Collaboration uses Microsoft Teams Graph and Microsoft Entra ID spoke actions. These actions include creating a team, adding or removing team members, archiving the team when the project closes, and posting a message when a record is updated. To enable these spoke actions, integrate your ServiceNow instance with Microsoft Teams Graph and Microsoft Azure AD to authenticate requests. For more information, see [Set up Microsoft Teams Graph spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-msteams.md) and [Set up Microsoft Azure AD spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-azure.md).

**Important:** When you activate the Microsoft Teams Graph and Microsoft Azure AD spokes, a [Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connection-alias.md) for Microsoft Teams Graph and Microsoft Azure AD is created by default with the IDs **sn\_msteams\_ahv2.Microsoft\_Teams\_Spoke** and **sn\_azure\_ad\_spoke.AzureAD** respectively. The connection that is active \(the Active field is set to **true**\) in Connections related list of this alias uses this default ID to connect your ServiceNow instance to Microsoft Teams Graph and Microsoft Azure AD. Therefore, you can have multiple connections associated with this alias but ensure that only one connection is active at any given time.

**Parent Topic:**[Using Project Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/project-management/using-project-management.md)

