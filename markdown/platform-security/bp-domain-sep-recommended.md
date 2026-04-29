---
title: Domain separation recommended practices for service providers
description: You can create, implement, and maintain domain separation for your applications and services.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Domain separation for service providers, Access Management]
---

# Domain separation recommended practices for service providers

You can create, implement, and maintain domain separation for your applications and services.

## Domain basics

With domain separation \(also known as ServiceNow Multitenant Platform Architecture\), you can segregate the application data, user interface, and business logic in a single customer instance that supports hierarchical modeling with cross-tenant intelligence. Business logic describes how the domain separation is configured and what rules are affecting the configuration.

Before you set off on the domain separation journey, here are some good practices to follow. Select topics as you want or follow them in order by clicking the links below the image.

![Global domain](../image/ds-graphic.png)

-   **[Domain separation explained](../concept/bp-what-is-domain-separation.md)**  
With domain separation, you can segregate application data, UI, and business logic, such as rules or workflows, in a single customer instance. Separating these elements into logically defined domains supports specific hierarchies for all customers using your applications.
-   **[Domain separation hierarchies](bp-domain-sep-hierarchies.md)**  
Create a hierarchy when defining a domain architecture to track your processes and workflows.
-   **[Context and domain separation](../concept/bp-domain-sep-context.md)**  
The context of a user's session determines the processes, data, and user interface \(UI\) as the user browses through list views, home pages, reports, and knowledge articles. The context is determined by the processes that you create, the business rules that you set, your workflows, and other factors.
-   **[Segregating and securing data with domain separation](bp-segregate-secure.md)**  
You can segregate and secure data on the ServiceNow platform in multiple ways, depending on your customer's needs. 
-   **[Alternatives to domain separation](bp-domain-separation-alternatives.md)**  
You can use a separate instance as an alternative to domain separation for your customers. A separate instance allows you the flexibility to meet the requirements for data separation within the groups and departments in an organization with little to no impact on others.
-   **[Evaluating the need for domain separation](bp-evaluation-dom-sep.md)**  
You may find that domain separation doesn't always work for your customers' organizations. It's best that you base your decision to go with domain separation by looking at your customers' needs.
-   **[Benefits of domain separation](bp-advantages-dom-sep.md)**  
Domain separation may work better for your customers' organizations than any other method for separating the data between groups and departments.
-   **[How a database query works with domain separation](../concept/bp-db-query-with-ds.md)**  
Using database queries with domain separation in your customers' applications help them protect their data. These queries then speed up the configuration and build processes.
-   **[Domain separation levels of support](bp-domain-levels.md)**  
Choose from three categories for domain separation of an application for your customers' organizations.
-   **[Service provider reference architecture](bp-sp-reference-arch-ds.md)**  
Your customers can access service provider \(SP\) services by using a portal that is designed for them to reach their domain-separated instance.
-   **[Domain separation terms](bp-terms-conditions.md)**  
With a ServiceNow instance, you can improve efficiency, add greater security, and increase performance for your customer organizations. It's helpful to understand some of the most common terms as you create your configurations.
-   **[Domain-separate a custom table](bp-ds-custom-table.md)**  
You may need to create custom tables in separate domains. This topic covers both the procedure and the concept behind domain-separating a custom table.
-   **[Customizing domain properties and themes](../concept/bp-domain-prop-themes.md)**  
You can customize your customers' company properties and themes within the domains that you have configured. Customization makes their instances fit in with their companies' overall look and feel.
-   **[Managing domain separation for specific uses](../concept/bp-emails-catalog-users.md)**  
You can set up separate domains for email notifications and customize the properties of catalog, tables, users, groups, and views. This enables you to provide more specific behavior in each domain, giving your customers more flexibility.
-   **[Configuring domain separation with the domain picker](../concept/bp-domain-picker-config-process.md)**  
Use the domain picker wisely, and remember the 80/15/5 approach so that you do not customize too much and impact the performance of your instance.
-   **[Domain separation performance considerations](../concept/bp-performance-considerations.md)**  
As you configure domain separation in your application and services, make sure that you consider the number and properties of domains you create. Too many property-heavy domains can impact the performance of your instance.
-   **[Setting up domain hierarchies](../concept/bp-domain-hierarchy.md)**  
You can avoid slowdowns and performance impacts in your instance by knowing how domain hierarchies work and by setting them up properly.
-   **[Checking domain logs for errors and warnings](../concept/bp-domain-logs.md)**  
Check the domain logs to find errors or warnings in your domain path processes and hierarchy configurations.
-   **[Importance of the Default domain](../concept/bp-default-domain.md)**  
Organizing your domains is a crucial part of the domain separation process. If you don't set a default domain, new tasks and user records go to the global domain. Anyone can see the records in the global domain, which means that data can be seen when it is not supposed to.
-   **[Contains queries and domain access](../concept/bp-contains-domain-visibility.md)**  
Use a "contains" query only in special cases, such as when users or groups need to see data from a domain that they don't have access to, but you don't want to move those users to a domain. Creating domain "contains" and user or group access for a domain should be an exception, only when absolutely needed.
-   **[Domain paths query method](../concept/bp-domain-query-method.md)**  
You can create effective queries with domain paths.
-   **[Slow queries and SQL debugging](../concept/bp-debug-sql.md)**  
Debugging SQL and slow queries can help you resolve slowness issues in an instance.
-   **[Before Query business rules](../concept/bp-before-query-business-rules.md)**  
You can use a Before Query business rule to help support data segregation on an instance. ServiceNow applications that support domain separation may support the separation of data and data routing only, have advanced business logic separation, or support tenant \(customer\) level administration of the application.
-   **[Avoiding domain path in scripts](../concept/bp-no-domain-path-in-scripts.md)**  
Domain paths can cause the values of your script to change or even break, so don't use them in scripts.
-   **[Domain assignments](bp-domain-assignment.md)**  
How you assign a domain impacts the value of the sys\_domain field. The assignments contain designs and business properties that affect how the application functions in each domain.
-   **[Domain separation and the Customer Service Management \(CSM\) plugin](../concept/bp-ds-and-csm.md)**  
For the best outcome, be aware of how the properties in the CSM plugin work. When the plugin is enabled, you can see the status of your records in your domains.

**Parent Topic:**[Domain separation for service providers](domain-sep-landing-page.md)

