---
title: Domain separation hierarchies
description: Create a hierarchy when defining a domain architecture to track your processes and workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/bp-domain-sep-hierarchies.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Recommended practices for service providers, Domain separation for service providers, Access Management]
---

# Domain separation hierarchies

Create a hierarchy when defining a domain architecture to track your processes and workflows.

## Sample domain separation hierarchies

The following diagram is a good starting point for defining domain architecture. It demonstrates the relationship between the TOP and lower domains and how the process, data, and business rules impact parent and child domains.

-   In the following example, TOP is a process domain. It should never contain users. Rather, TOP should contain the new processes that instance owners develop and the overrides to these processes from the global domain.
-   Only the service provider \(SP\) has access to the default domain. This domain never contains active users. It contains only the "lost" data that you need to reassign to the correct domain.

    **Note:** When data is not assigned to a specific domain, it moves to the default domain. It is temporarily "lost" and needs to be assigned to its correct domain.

-   Tasks and users without a domain are placed in the default domain automatically when you create or update domains. You can override that action by either clearing the **Default** option on this record or selecting the **Default** option on another domain record. If you have not set a default domain yet, tasks and users with no domain move to the global domain.
    -   Don't move data between domains while you are using the instance.
    -   If any data ends up in the default domain, that means you have a configuration or procedural problem to address.

You don't see the word "Global" in this diagram because there is no global domain. Remember that "global" is the absence of a domain on a record.

For example, a table that has no domain field means that the table contains all global records. A table that has a domain field means that any record without a domain is a global domain.

The word "global" is in the domain field. It is placed there automatically when the record has no domain.

Global records are available to all users of the instance unless they are restricted by security configurations.

-   Use the default domain to make sure that records do not end up in the global domain on tables that should never have global records.
-   Instance owners must then triage the records in the default domain and move them to the correct domain.

\[Omitted image "bp-ds-hierarchy.png"\] Alt text: Sample domain separation hierarchies

## Domain hierarchies

-   Parent/child: Process and data affected
    -   Design that is based on a process flow.
    -   Remember that the parent domains can access all data in the child domains.
-   "Contains" domain: Only data is affected. For example, making SP in the diagram contain TOP does not make processes in SP run in the TOP domain and downward.
    -   Grants data access rights to individuals in groups that require dedicated access to certain domains.
    -   Contains causes or conditions to be added to database queries that can cause performance issues with large domain and data sets.
-   Visibility: Hierarchy that is always visible to users once you provide access. Only the data is affected, not the processes.
    -   Grants data access of a domain to another domain that did not have that access when the parent-and-child hierarchy was built.
    -   Enables users to see all the data in the domains that they have visibility access for, all the time, regardless of the record they are working on.

        **Note:** Use sparingly, as Visibility can allow complete access that you may not intend.


## Basic principles of defining a domain hierarchy

Unrestricted and restricted use cases for domain separation.

Many SPs have customers who implicitly state that access to their domains must be tightly regulated, which constrains the use of the “contains” function at the TOP domain. The following diagram explains how to mitigate that regulation by dividing domains into Restricted and Unrestricted domains.

1.  Customers exist in a specific "vertical" of the domain separation hierarchy. This means they only consume processes defined in their domain and all parent domains above theirs in the hierarchy. Any processes defined in domains that are not in their linear parent-child hierarchy do not apply.

    **Note:** Customers or "tenants" are entities that are segregated from each other completely, not like departments or business units that share resources with each other.

2.  Super verticals \(restricted, manager services, and so on\) are allowed as long as the customers only ever belong to one of them.
3.  Services, products, or offerings that need to be horizontally available to all customers are not defined within separate domain hierarchies.

\[Omitted image "bp-domain-hierarchy-1.png"\] Alt text: Domain hierarchy flow

\[Omitted image "bp-domain-hierarchy-2.png"\] Alt text: Domain hierarchy with verticals

Here are some sample use cases:

-   Under TOP, you might create two domains, Unrestricted and Restricted.
    -   Place customers and their domains that don't have SP visibility restraints under Unrestricted.
    -   Place customers and their domains that do have that requirement under Restricted.
-   System admins can then use “contains” and “visibility” functions in an efficient, targeted manner.
    -   Apply "contains" to Unrestricted, so a single “contains” can grant visibility to most customers.
    -   Apply domain visibility using ”domain visibility groups” to specific domains as needed.

The following diagram delineates how to choose which hierarchy model is right for you. You can choose separate hierarchies, hybrid, or shared hierarchies depending on which processes and functionality you want in your domain structures.

\[Omitted image "bp-customer-decision-a-tree.png"\] Alt text: Customer decision tree

\[Omitted image "bp-dedicated-vs-shared.png"\] Alt text: Dedicated vs shared hierarchy of data separation

To learn more about hierarchy architecture, see [Service provider reference architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-sp-reference-arch-ds.md).

**Parent Topic:**[Domain separation recommended practices for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-sep-recommended.md)

**Related topics**  


[Domain separation explained]()

[Context and domain separation]()

[Segregating and securing data with domain separation]()

[Alternatives to domain separation]()

[Evaluating the need for domain separation]()

[Benefits of domain separation]()

[How a database query works with domain separation]()

[Domain separation levels of support]()

[Service provider reference architecture]()

[Domain separation terms]()

[Domain-separate a custom table]()

[Customizing domain properties and themes]()

[Managing domain separation for specific uses]()

[Configuring domain separation with the domain picker]()

[Domain separation performance considerations]()

[Setting up domain hierarchies]()

[Checking domain logs for errors and warnings]()

[Importance of the Default domain]()

[Contains queries and domain access]()

[Domain paths query method]()

[Slow queries and SQL debugging]()

[Before Query business rules]()

[Avoiding domain path in scripts]()

[Domain assignments]()

[Domain separation and the Customer Service Management \(CSM\) plugin]()

