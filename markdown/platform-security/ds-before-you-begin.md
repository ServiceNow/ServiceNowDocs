---
title: Configuration that can be delegated to internal or external customers
description: Domain separation is designed to give ServiceNow service providers \(SPs\) the ability to configure the services they offer to their customers. It is not designed to enable their customers to administer those services themselves, except in a few areas that this topic details.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring domain separation, Domain separation for service providers, Access Management]
---

# Configuration that can be delegated to internal or external customers

Domain separation is designed to give ServiceNow® service providers \(SPs\) the ability to configure the services they offer to their customers. It is not designed to enable their customers to administer those services themselves, except in a few areas that this topic details.

## Overview

It is safe for SP customers, on their own, to manage data contained within their domain that does not affect licensing or other customers. For example, it is safe for a customer to create new reports or manage configuration items, but it’s not safe for them to customize fields, choices, business rules, and other processes where they can impact other customers on the same instance.

The ServiceNow base system administrative roles and their access controls on the ServiceNow platform are designed for a single admin team per instance. For example, the domain\_admin role is granted to one of the SP’s resources to manage all domain setting for the instance, and to create new domains. For any domain-specific admin tasks, the SP should create new “customer admin” roles and access controls as needed to grant specific access to their customers.

The following image is an overview of common admin functions in varying categories of what is safe for a customer to do. ![Levels of access allowed for customers of service providers](../image/before-begin-access.png)

![Green icon](../image/icon-green.png) **Can give access**

Examples:

-   CI data management in the CMDB
-   Report creation
-   Updates to existing user data, or new users without roles
-   Updates to existing core data records such as department, group, location,cost center, or new groups without roles, and new departments/ cost centers/ location.

![Yellow icon](../image/icon-yellow.png) **Proceed with caution**

Examples:

-   Catalog Items: To create customer-specific catalog items that can be updated by the customer, two capabilities can be used together: Domain separation for catalog items \([Domain separation and Service Catalog](https://www.servicenow.com/docs/access?context=domain-separation-service-catalog-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)\) enables the instance owner to create items in the customer’s domain. The instance owner can create a role to allow customers to update safe fields such as price, description, and images. The [Catalog Builder](https://www.servicenow.com/docs/access?context=catalog-builder&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) \(new in the Quebec release\), gives the SP admin team the ability to create item templates that are safe to distribute to customers to create new items within their domain from within a prescriptive UI experience.
-   User/Group Management: It’s safe to create a “customer admin” role that can create and modify user records, but adding and removing roles can affect security and licensing. There is no way in the base system to subdivide roles that are safe for a customer to be able to grant them. The same goes for the creation and modification of groups. While the group itself can be modified, the addition or subtraction of roles should be controlled.
-   [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US): ServiceNow Workflow Studio is the building tool used to create process \(workflow\) for tables. The flow\_designer role gives customers script-free access to build flows. They can read and clone every flow in domains above them in the hierarchy. They can create and modify flows in their domain. This cannot happen in a silo, however. Anyone who can affect process must be added to the global admin team for governance so processes do not cancel out each other or cause other conflicts.

![Red icon](../image/icon-red.png) **Do not give access**

Understanding how choice fields work is helpful to understand why only the SP admin team should be managing them.

-   Structure of a choice field: Choice field values are stored in the sys\_choice table and grouped based on: Table, Domain, and Language.

    For example, the **State** field in a Task is available to every table that extends a Task. That means that each table can have its own values, those values can be multiplied by domain, and the domain values can be multiplied by language.

    All of the values for **State** across all tables, domains and languages are considered the values for the **State** field.

-   How changes to choice fields work: When a choice field is updated, a payload is created with all values for that field \(Tables, Domains, Languages\). When you install this payload on an instance, all existing values for the field are deleted and the new values are loaded. This ensures that there are no duplicate entries or leftover values that are no longer valid.

    For this reason, it’s impossible to give a customer in a domain-separated instance the ability to update choice fields directly because that would affect the entire instance. In addition, you can’t update choices directly in a production instance because any imported update sets that affect that field would overwrite the existing choices. In some cases, choice fields can drive processes themselves, which would break if a customer were to change those fields.


To learn more, see:

-   [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)
-   [Create an ACL rule](../../contextual-security/task/t_CreateAnACLRule.md)
-   [Service Provider Learning Path on ServiceNow University](https://snc.do/path)
-   [Domain separation for service providers](https://snc.do/sp)
-   [Service Provider Concepts](https://snc.do/spc)
-   [Application Support for domain separation](https://snc.do/app)
-   [Domain separation release notes](https://snc.do/rn)

**Parent Topic:**[Exploring domain separation](c_DomainSeparation.md)

**Related topics**  


[Domain assignment](c_DomainAssignment.md)

[Visibility domains and Contains domains](c_DomainVisibility.md)

[Domain scope](c_DomainScope.md)

[Concepts for service providers](sp-concepts.md)

[Installed with domain separation](../reference/r_InstalledWithDomainSeparation.md)

