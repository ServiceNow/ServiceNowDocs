---
title: Before Query business rules
description: You can use a Before Query business rule to help support data segregation on an instance. ServiceNow applications that support domain separation may support the separation of data and data routing only, have advanced business logic separation, or support tenant \(customer\) level administration of the application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Domain separation recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Before Query business rules

You can use a Before Query business rule to help support data segregation on an instance. ServiceNow applications that support domain separation may support the separation of data and data routing only, have advanced business logic separation, or support tenant \(customer\) level administration of the application.

A Before Query business rule is supplementary code that you use to support data segregation within domain-separated environments.

**Warning:** Do not use the Before Query business rule in place of the Domain Separation plugin. This business rule does not prevent data leakage as securely as the plugin.

## Using the Before Query business rule for data segregation

You can use the Before Query business rule with data segregation in these situations:

-   When domain separation is not supported by a ServiceNow application and you must grant or restrict table or row access to one or more non-internal customers outside of the service provider organization.

    **Note:** Before you begin developing, contact ServiceNow Customer Support about the application roadmap for that product; domain support improvements may be planned for upcoming releases.

-   When a table is domain-separated but access to its rows must be granted or restricted based on certain conditions that apply only to a set of domains in the system.

    **Note:** For example, a customer in the X domain has multiple vendors supporting that domain and those vendors are granted access to see only the records that are assigned to them.


## Points to consider before creating Before Query business rules

You can script Before Query business rules to prevent parent and child table access based on a combination of user information, group memberships, companies, roles, or record-specific field conditions. Before Query business rules are put into separate domains and created to apply globally, to a specific branch of a domain hierarchy.

-   Where you can, create Before Query business rules at the lowest possible part of the domain hierarchy so that the rule runs only for users that it applies to.
-   Know that there are scenarios in the system where business rules may not run or where a user-triggered interaction may not trigger a business rule to run. For example, a business rule won't run when you have transform maps with Run business rules turned off, or you have scripts with the workflow disabled.
-   Always populate the condition field to specify when the rule runs. For example, you can specify if the business rule applies only to certain vendors in a domain.

    **Warning:** When designing and coding business rules \(especially Query business rules\), limit OR clauses and searches in non-indexed fields. Too many OR clauses and searches in non-indexed fields can slow queries or affect how your instance performs.

-   Use Before Query business rules only when necessary. Too many Before Query rules can affect how your instance performs.


Before Query business rules run before access control lists \(ACLs\) and perform better in general. This is true especially when you limit the returned results to those users in service provider \(SP\) environments who have access to several domains in the system.

**Note:** Filtering the data is transparent \(unlike with ACLs\) to users who do not see the message `Data Security restricts….` when interacting with data.

## When not to use Before Query business rules and ACLs

Be careful when you use Before Query business rules and ACLs to segregate customer data. By using both business rules and ACLs, you create customizations that you then must maintain. Customizations can potentially cause performance issues. Your development teams should create processes to make sure that they don’t break the system.

Domain separation provides both scalability and governance with the current domain path query method \(v3\), which is a widely supported framework. The ServiceNow Platform and App teams are responsible for maintaining the framework, taking the burden off the customer.

For companies with many customers in many instances, excessive use of Before queries and ACLs may cause the database queries not to perform well.

## How domain separation is enabled

You can enable domain separation with a ServiceNow plugin. A product manager, supported by a development team, manages the functionality. Enhancements and fixes for domain separation functionality are included with ServiceNow releases. Instance owners can consult Customer Service and Support resources, such as the Service Portal, at [https://support.servicenow.com](https://support.servicenow.com) for assistance with domain separation.

**Parent Topic:**[Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained](bp-what-is-domain-separation.md)

[Domain separation hierarchies](../reference/bp-domain-sep-hierarchies.md)

[Context and domain separation](bp-domain-sep-context.md)

[Segregating and securing data with domain separation](../reference/bp-segregate-secure.md)

[Alternatives to domain separation](../reference/bp-domain-separation-alternatives.md)

[Evaluating the need for domain separation](../reference/bp-evaluation-dom-sep.md)

[Benefits of domain separation](../reference/bp-advantages-dom-sep.md)

[How a database query works with domain separation](bp-db-query-with-ds.md)

[Domain separation levels of support](../reference/bp-domain-levels.md)

[Service provider reference architecture](../reference/bp-sp-reference-arch-ds.md)

[Domain separation terms](../reference/bp-terms-conditions.md)

[Domain-separate a custom table](../reference/bp-ds-custom-table.md)

[Customizing domain properties and themes](bp-domain-prop-themes.md)

[Managing domain separation for specific uses](bp-emails-catalog-users.md)

[Configuring domain separation with the domain picker](bp-domain-picker-config-process.md)

[Domain separation performance considerations](bp-performance-considerations.md)

[Setting up domain hierarchies](bp-domain-hierarchy.md)

[Checking domain logs for errors and warnings](bp-domain-logs.md)

[Importance of the Default domain](bp-default-domain.md)

[Contains queries and domain access](bp-contains-domain-visibility.md)

[Domain paths query method](bp-domain-query-method.md)

[Slow queries and SQL debugging](bp-debug-sql.md)

[Avoiding domain path in scripts](bp-no-domain-path-in-scripts.md)

[Domain assignments](../reference/bp-domain-assignment.md)

[Domain separation and the Customer Service Management \(CSM\) plugin](bp-ds-and-csm.md)

