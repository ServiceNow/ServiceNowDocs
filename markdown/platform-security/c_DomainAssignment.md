---
title: Domain assignment
description: By default, domain separation adds a domain field to tables and their extensions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring domain separation, Domain separation for service providers, Access Management]
---

# Domain assignment

By default, domain separation adds a domain field to tables and their extensions.

You can also extend domain separation to any new tables you create by adding a **sys\_domain** field to the table's dictionary definition. By default, the system only domain-separates platform and baseline application tables where appropriate.

**Warning:** ServiceNow does not recommend domain-separating platform tables \(any table with the sys\_ prefix such as the Dictionary Entry \[sys\_dictionary\] and Dictionary Entry Override \[sys\_dictionary\_override\] tables\) because it can produce unexpected results.

Each record is assigned a single domain. That domain is stored in the **sys\_domain** field. Several tables, by default, have the **sys\_domain** column and are already domain separated.

The value of the **sys\_domain** field contains the domain assigned to the record by any of the following:

-   Company to which the user belongs
-   Business rule when creating record
-   Module used when creating record
-   Form template used when creating record
-   Domain of the parent record
-   Domain assigned to User record
-   Domain of the user who creates it

The system prevents the following tables from being domain separated:

-   Access Control `[sys_security_acl]`
-   Script Include `[sys_script_include]`
-   System Property `[sys_properties]`
-   Security Exclusion/Inclusion List Entities `[sys_security_restricted_list]`
-   Dictionary Entry `[sys_dictionary]`
-   Dictionary Entry Override `[sys_dictionary_override]`

## Assigning users to companies

Administrators can quickly assign users to a domain by assigning them to a company. After users are assigned to a domain, records automatically inherit the user's domain.

For example, assigning Bow Ruggeri to the ACME company automatically assigns him to the ACME domain. Assigning Don Goodliffe to the Initech company automatically assigns him to the Initech domain. Any records they create are automatically added to the appropriate domain.

## Using business rules to assign domains

Administrators can use a business rule to automatically set a domain value when creating a record. The business rule must set a value in the **sys\_domain** field. Administrators must ensure there is a **sys\_domain** column available for the record's table. To learn more see [Domain separation recommended practices for service providers](../reference/bp-domain-sep-recommended.md).

## Using modules to assign domains

Administrators can use the **sysparm\_domain** URL parameter to automatically assign new records to a particular domain from a module. Administrators must create a module with an **Argument** value of: `sysparm_domain=sys_ID of domain`.

## Using form templates to assign domains

Administrators can use a form template to automatically assign new records to a particular domain. Administrators must add the **sys\_domain** field to the form and select a domain value. For example, setting the **sys\_domain** field to **TOP/ACME domain** automatically assigns all records from this template to the TOP/ACME domain.

## Domain inheritance on tables

By default, related records inherit the domain of the parent record. For example:

-   A change task record inherits the domain of the parent change request record.
-   A problem record inherits the domain of the parent incident record.

## Automatic domain assignment based on user domains

If no other domain conditions apply, a record automatically inherits the domain of the user who creates it.

**Parent Topic:**[Exploring domain separation](c_DomainSeparation.md)

**Related topics**  


[Configuration that can be delegated to internal or external customers](ds-before-you-begin.md)

[Visibility domains and Contains domains](c_DomainVisibility.md)

[Domain scope](c_DomainScope.md)

[Concepts for service providers](sp-concepts.md)

[Installed with domain separation](../reference/r_InstalledWithDomainSeparation.md)

