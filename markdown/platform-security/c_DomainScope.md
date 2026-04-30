---
title: Domain scope
description: Domain scope defines what users can and cannot access.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring domain separation, Domain separation for service providers, Access Management]
---

# Domain scope

Domain scope defines what users can and cannot access.

Every user has two domain scopes when establishing a session in a domain-separated instance.

-   Session scope is set upon session establishment to the domain listed in the user's user record. Users can manually change their session domain scope from the domain picker.
-   Record scope uses the domain of the record and is active when viewing the form of any record.

By default, the record scope takes precedence over the session scope so that users in higher level domains adhere to each record's data and process constraints. However, these users can choose to expand or collapse the domain scope to show or hide data from other domains. For example, a user in the Service Provider \(SP\) domain also has visibility into child domains such as the ACME domain. When looking at an incident record from the ACME domain, the user can choose to expand the domain scope to show values from the SP domain or collapse the domain scope to show only record values that match the record's ACME domain.

**Note:** Users always have access to data from domains that have been explicitly granted to them by domain visibility.

Users with the domain\_expand\_scope user role can select the domain scope from the **Toggle Domain Scope** UI action on the form. When record scope is in effect, click the UI action to expand to session scope and display all data available based to the user's domain and child domains. When session scope is in effect, click the UI action to collapse to record scope and display only data that matches the current record's domain.

**Note:** A record does not display the UI action to toggle the domain scope if the record is in the global domain or if the user's domain matches the record's domain.

## Record value selection from other domains

Users who can see multiple domains have the option to select record values from a domain that is different than the record's domain.

For example, service desk agents working for a service provider might want to assign certain incidents to themselves to resolve issues on behalf of their customers. When they do this, the incident **Assigned to** field might contain a user from the SP domain, even though the incident record itself is associated with a child domain such as ACME.

Selecting a record value from another domain does not change the record's domain. The record retains its original domain. When a user views a record with values from multiple domains, the user's domain visibility determines what they see.

<table id="table_lnm_z3h_1r"><thead><tr><th>

When these conditions are met

</th><th>

The user has access to these UI elements

</th></tr></thead><tbody><tr><td>

The user has access to the domain of the current record referenced in a field.

</td><td>

The user can:-   See reference field display value. For example, sees the user name in the **Assigned to** field.
-   See the related record from reference icon. For example, sees the user record for the user in the **Assigned to** field.
-   Select values from any visible domain. For example, can select users from either the SP and ACME domains.

</td></tr><tr><td>

The user does not have access to the domain of the current record referenced in a field.

</td><td>

The user can:-   Not see reference field display values. \(This is the case if domain separation was activated in Madrid or later releases and the user doesn't have access to the domain of that record.\)
-   Only select values from the record's domain. For example, can only select users from the ACME domain.

</td></tr></tbody>
</table>## Domains and associated companies

With domain separation you can cascade changes you make to a company record to the domain and other records associated to the company.

By default, the system automatically assigns users to the same domain as their company. For example, all users of the ACME company automatically become members of the TOP/ACME domain.

**Note:** Users with the admin role can change their own user records and therefore change domains. Service Providers may want to either disable delegated administration or set up an approval process to verify that the user needs the admin role.

When you change a company's domain, the instance automatically changes the domain of the following associated records to match the company's new domain.

-   Locations
-   Departments
-   Groups
-   Users

**Note:** The instance does not automatically change the domain of any record where you have selected the **Managed domain** checkbox.

## Domain deactivation and associated companies

When you deactivate a domain, the instance also automatically completes the following actions.

-   Deactivates all companies in the domain.
-   Prevents all users assigned to the inactive company from logging in.

**Note:** When a user from an inactive company attempts to log in, the user sees an error message similar to `Company inactive - your access to this instance is not authorized`.

For example, if you deactivate the ACME domain from the sample data, the instance also deactivates the ACME company, and the three sample users are locked out.

**Parent Topic:**[Exploring domain separation](c_DomainSeparation.md)

**Related topics**  


[Configuration that can be delegated to internal or external customers](ds-before-you-begin.md)

[Domain assignment](c_DomainAssignment.md)

[Visibility domains and Contains domains](c_DomainVisibility.md)

[Concepts for service providers](sp-concepts.md)

[Installed with domain separation](../reference/r_InstalledWithDomainSeparation.md)

