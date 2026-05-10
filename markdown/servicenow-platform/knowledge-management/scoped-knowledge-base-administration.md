---
title: Scoped knowledge bases
description: To protect knowledge bases containing sensitive articles, use a scoped knowledge base. Even system administrators and knowledge administrators can't administer scoped knowledge bases unless explicitly authorized through user criteria.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Scoped knowledge bases

To protect knowledge bases containing sensitive articles, use a scoped knowledge base. Even system administrators and knowledge administrators can't administer scoped knowledge bases unless explicitly authorized through user criteria.

For example, say you have a knowledge article with sensitive payroll information that should be seen only by the Payroll department and not by a system administrator or knowledge administrator. You could create a knowledge article with the sensitive information in a scoped knowledge base within the Human Resources: Core application.

Only users with the admin role of an application and the knowledge\_admin role can administer a scoped knowledge base. You control access to knowledge bases of an application with application administration enabled, such as HR, through the Access Control Lists \(ACLs\) of the knowledge tables in the application instead of global ACLs. To define access to a scoped knowledge base, specify appropriate user criteria for users, including system administrators and knowledge administrators.

**Note:** For Scope Master tables to derive scope and execute scoped ACLS, you must set the **glide.enforce\_security\_scope.&lt;scope\_name&gt;** system property to true.

You can't modify the scope of existing knowledge bases. They remain in the global scope. However, you can create a scoped knowledge base to protect sensitive knowledge articles.

To create a scoped knowledge base for an application, in addition to the knowledge\_admin or admin role, you must have access to view and select that application in the application picker \(see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md)\). For example, before you create a knowledge base in the Human Resources: Core application, you must select the Human Resources: Core application in the application picker, and then create the knowledge base. Then, when you create a knowledge base, on the Knowledge base form, the application scope of the knowledge base is set in the **Application** field.

**Related topics**  


[Create a knowledge base](../task/create-a-knowledgebase.md)

[Select an application from the application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_SelectAnAppFromTheAppPicker.md)

[Application administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-administration.md)

[Control access at the knowledge base level through user criteria](../task/t_SelectUserCriteria.md)

