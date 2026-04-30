---
title: Domain separation terms
description: With a ServiceNow instance, you can improve efficiency, add greater security, and increase performance for your customer organizations. It's helpful to understand some of the most common terms as you create your configurations.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain separation terms

With a ServiceNow instance, you can improve efficiency, add greater security, and increase performance for your customer organizations. It's helpful to understand some of the most common terms as you create your configurations.

## Managed domain

In a managed domain, the **Managed domain** field allows domain administrators to manually select a domain for the user, group, department, location, or CI record, rather than using the domain that is assigned automatically from the company record.

If you want to change those properties, you can override them to further customize the functions of the applications in each of your domains.

## Process tables

In process tables, if you see a value in the **Overrides \[sys\_overrides\]** field, a process override record exists. That means that delegated administration, which is how administrators can set domain-specific policies, is in effect. Admins in the global domain can use the **Expand/Collapse Domain Scope** related link to see override records.

**Note:** Reports are separated into domains and contain an **Overrides** field. To view all reports from the global domain, use the **Expand Domain Scope** related link.

When you view process tables from a domain, you see only the relevant process records for the selected domain. When you view a process table from the global domain, the **Expand Domain Scope** related link is displayed to let you see all process records, including overrides. To view only the relevant process records for global again, use the **Collapse Domain Scope** related link.

The domain scope feature is used only for process tables and causes the visibility of data on the table to shift in the opposite direction. For example, a record in the parent domain can be seen in the child, but a parent cannot see a child record. This allows the process to flow down to child domains.

## Types of domains

Different types of domains can help you organize your processes and data and how they function in the application or feature.

**Customer Domain**

In the customer's domain is the user interface, as well as the process that controls how the data Is used.

The ACME domain in the following image is a customer domain.

**Process Domain**

You create processes for how the data is used and what it does in the domain. These processes must have these attributes:

-   Specific processes and UI settings for a set of domains
-   No core data of any kind \(such as specific user data\).
-   The TOP domain in the following image is a process domain.

**Data Domain**

The data domain holds data that is relevant to multiple customers. That data can be shared without sharing the actual customer domains. Each customer has its own data domain and can access it.

**Note:**

This kind of domain is not common and can cause performance issues if overused. Consult with an SP architect before use.

Example: The domain may hold tasks that ACME, Cisco, and the SP all need to interact with.

The Default domain in the following image is a data domain.

**User Data**

User record data never belongs in the global domain or any of the process domains. Users are primarily created in customer domains and can on occasion be created in data domains.

Admin accounts are special as they should not be used as everyday users of the instance and should be in the global domain to facilitate administrative functions.

![Domain hierarchy](../image/bp-ds-hierarchy.png "Domain hierarchy")

## Lists, admin, global process

**Lists**

From the global domain, if you right-click any choice field’s label, select **Configure Choices**, and then add a new choice, the choice pushes automatically to all domain-specific lists for that field. If the new option is marked as **Selected**, it is added as active. If the new option is marked as **Available**, it is added as inactive.

**Instance Administration**

The instance owner’s administrators must handle all normal process creation, modification, and maintenance in a domain-separated instance. Individual domain managers can maintain some parts of data-driven processes. The types of domain managers maintain user administration, support group memberships, and locations, or manage applications that are designed with tenant administration in mind.

**Global process/parameters**

You can create and maintain the process that affect the global domain as well as set the parameters. These properties are common for all users of a domain-separated instance.

Examples: System properties, dictionary overrides, `sys_documentation` \(field labels\), the data model \(classes, CI types, and so on\), tables and fields `[sys_dictionary]` \(access can be restricted\), indexing \(text indexes as well as database\), ACLs, installation exits, inbound actions, public pages, and interceptors.

**Parent Topic:**[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](../concept/bp-what-is-domain-separation.md)

[Domain separation hierarchies](bp-domain-sep-hierarchies.md)

[Context and domain separation](../concept/bp-domain-sep-context.md)

[Segregating and securing data with domain separation](bp-segregate-secure.md)

[Alternatives to domain separation](bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](bp-evaluation-dom-sep.md)

[Benefits of domain separation](bp-advantages-dom-sep.md)

[How a database query works with domain separation](../concept/bp-db-query-with-ds.md)

[Domain separation levels of support](bp-domain-levels.md)

[Service provider reference architecture](bp-sp-reference-arch-ds.md)

[Domain-separate a custom table](bp-ds-custom-table.md)

[Customizing domain properties and themes](../concept/bp-domain-prop-themes.md)

[Managing domain separation for specific uses](../concept/bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](../concept/bp-domain-picker-config-process.md)

[Domain separation performance considerations](../concept/bp-performance-considerations.md)

[Setting up domain hierarchies](../concept/bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](../concept/bp-domain-logs.md)

[Importance of the Default domain](../concept/bp-default-domain.md)

[Contains queries and domain access](../concept/bp-contains-domain-visibility.md)

[Domain paths query method](../concept/bp-domain-query-method.md)

[Slow queries and SQL debugging](../concept/bp-debug-sql.md)

[Before Query business rules](../concept/bp-before-query-business-rules.md)

[Avoiding domain path in scripts](../concept/bp-no-domain-path-in-scripts.md)

[Domain assignments](bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](../concept/bp-ds-and-csm.md)

