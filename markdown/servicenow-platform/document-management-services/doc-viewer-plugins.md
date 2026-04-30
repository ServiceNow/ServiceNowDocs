---
title: Document Viewer plugins
description: With Document Viewer, you can view documents directly in the ServiceNow Platform rather than having to download them. Two new plugins enhance the experience and provide more options for document viewing. You can collaborate with other people, copy, delete, restore, and view version history directly in a ServiceNow instance.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Document Viewer, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document Viewer plugins

With Document Viewer, you can view documents directly in the ServiceNow Platform rather than having to download them. Two new plugins enhance the experience and provide more options for document viewing. You can collaborate with other people, copy, delete, restore, and view version history directly in a ServiceNow instance.

## Overview

In previous ServiceNow releases, not all documents could be shared and used for team collaboration. With new plugins for the Platform Document Viewer, now you can:

-   Collaborate \(edit, share\) with Microsoft OneDrive and copy documents to your ServiceNow instance. ​
-   Upload a policy document authored in your ServiceNow instance as a Microsoft 365 document in Microsoft 365 SharePoint.​
-   Attach shared links to a record. Clicking the link opens the document in Microsoft 365 SharePoint​.
-   -   The link can be shared with a co-worker, who can view and edit the document in real time.​
-   The current version is also viewable in the ServiceNow instance.​
-   Use collaboration tools such as Microsoft 365 for review and co-authoring documents.​

## Plugins

To use this feature, install the following plugins:

-   Microsoft OneDrive Spoke​
-   Microsoft OneDrive document service Spoke
-   Microsoft Azure AD Spoke for Integration Hub
-   Multi Provider Document Service Framework

​

See [List of plugins \(Rome\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for a complete list of ServiceNow plugins.

After installation, you can use the base system subflows or customize them.​ Configure the subflows in the Document actions table.​ Once configured, they can be invoked as UI actions from List views or can be invoked through Script Include APIs.​

-   **Microsoft OneDrive integration plugin**

    Collaborate in Microsoft OneDrive and perform copy, delete, restore, and version actions on documents directly in a ServiceNow instance. This integration is bi-directional \(performs in both directions\): Changes are reflected in both Microsoft OneDrive and in the instance.

-   **Microsoft Azure AD __Spoke for IntegrationHub__**

    The [Microsoft Azure AD Spoke](https://www.servicenow.com/docs/access?context=microsoft-azure-ad-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for Integration Hub provides actions that a Process Analyst can use when designing flows. The actions allow them to automate the management of users, security groups, and office groups. User management includes applying licenses that result in user provisioning into Office 365.

-   **Multi Provider Document Service Framework plugin \(glide plugin\)**

    Plugin contains the data model needed to integrate with third-party document service providers.


​

**Note:** To activate a plugin:

1.  Navigate to **System Definition** &gt; **Plugin**.
2.  Enter the plugin name in the Search field.
3.  Select **install**.

## Tables

**mp\_provider\_details**

-   Provider Details Name
-   Provider Name
-   Attributes

**mp\_document\_version**

-   Version​ ​
-   Document
-   Version Modified By​
-   Version Last Modified​

**mp\_document\_activity​**

-   Document Name​
-   Document sys\_id​
-   Document Version sys\_id
-   Document Action​
-   Provider Detail​
-   Notes

**mp\_documents**

-   Document name​
-   Provider Details
-   Attachment
-   URL
-   Description

**mp\_document\_action​**

-   document\_action\_name​
-   provider\_detail​
-   subflow
-   provider\_permission​

**mp\_permission\_configuration​**

-   Entity\_type​
-   Entity\_id
-   Attributes
-   Provider\_group\_id​
-   Provider\_group\_name​
-   permission

**mp\_provider\_permission​**

-   permission
-   provider
-   Attributes
-   description

**mp\_collaborator​**

-   collaborator\_attributes​
-   collaborator\_email​
-   collaborator\_id​
-   collaborator\_name​
-   Provider\_detail​
-   user

**Related topics**  


[Document Viewer](Documentviewer.md)

