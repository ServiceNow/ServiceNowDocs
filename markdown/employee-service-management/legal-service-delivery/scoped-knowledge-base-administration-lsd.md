---
title: Scoped knowledge bases
description: To protect knowledge bases containing sensitive articles, use a scoped knowledge base. Even system administrators and knowledge administrators can't administer scoped knowledge bases unless explicitly authorized through user criteria.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security in Legal Service Delivery, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Scoped knowledge bases

To protect knowledge bases containing sensitive articles, use a scoped knowledge base. Even system administrators and knowledge administrators can't administer scoped knowledge bases unless explicitly authorized through user criteria.

For example, say you have a knowledge article with sensitive payroll information that should be seen only by the Payroll department and not by a system administrator or knowledge administrator. You could create a knowledge article with the sensitive information in a scoped knowledge base within the Human Resources: Core application.

Users with the admin role of an application and the knowledge\_admin role can administer a scoped knowledge base. You control access to knowledge bases of an application with application administration enabled, such as HR, through the ACLs of the knowledge tables in the application instead of global ACLs. To define access to a scoped knowledge base, specify appropriate user criteria for users, including system administrators and knowledge administrators.

**Note:** For Scope Master tables to derive scope and execute scoped ACLS, you must set the **glide.enforce\_security\_scope.&lt;scope\_name&gt;** system property to true.

You can't modify the scope of existing knowledge bases. They remain in the global scope. However, you can create a scoped knowledge base to protect sensitive knowledge articles.

To create a scoped knowledge base for an application, in addition to the knowledge\_admin or admin role, you must have access to view and select that application in the application picker \(see Application picker\). For example, before you create a knowledge base in the Human Resources: Core application, you must select the Human Resources: Core application in the application picker, and then create the knowledge base. Then, when you create a knowledge base, on the Knowledge base form, the application scope of the knowledge base is set in the **Application** field.

**Related topics**  


[bundle-platcap.create-a-knowledgebase]

[bundle-cadev.application-administration]

[bundle-platcap.t_SelectUserCriteria]

