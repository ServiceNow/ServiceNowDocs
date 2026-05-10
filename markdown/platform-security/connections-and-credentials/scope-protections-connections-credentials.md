---
title: Scope protections for Credentials and Connections
description: You can classify certain types of Connection &amp; Credential records as belonging to a scope, and extend scope protections to them. These scope policies protect records you create in a table, and prevent interactions with records that are private to another scope.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore credentials, connections, and aliases, Connections and Credentials, Access Management]
---

# Scope protections for Credentials and Connections

You can classify certain types of Connection &amp; Credential records as belonging to a scope, and extend scope protections to them. These scope policies protect records you create in a table, and prevent interactions with records that are private to another scope.

An **Application** field is available in the Connection \[sys\_connection\] and Discovery Credentials \[discovery\_credentials\] tables for associating these types of records to specific scopes. It is not visible on UI forms in Australia, but you can easily add it to them. To learn more about these record types, and adding the field to their UI forms, see:

-   [Get started with connections](../reference/connection-information.md)
-   [Get started with credentials](../reference/credentials-getting-started.md)
-   [Credential aliases for Discovery](discovery-credential-alias.md#)
-   [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md)

Restricting the use of a Connection &amp; Credentials record to a specific scope is important for managing applications that require enforced security. These applications include HR Service Delivery or Security Operations Connection &amp; Credentials records created in scoped administered applications are not visible to admin users. Associating a Connection &amp; Credentials record to a specific application scope affords the following protections:

-   Applies Access Control List rules \(ACLs\) to restricted scopes. To learn more about scoped ACLs, see [Access control list rules](../../../administer/contextual-security/concept/access-control-rules.md).

    **Note:** Some applications using scope administration and enforced security may require additional setup. To learn more, see [Manage HR roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/c_ManageRoles.md)

-   Protects records when queried using a script. If you do a query from the Global scope, and the Connection &amp; Credential record is in a protected scope, it doesn't appear in the query, unless given access to it.

You can customize and grant access to query-restricted records by using Restricted Caller Access. To learn more, see [Restricted caller access privilege settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/restricted-caller-access-privilege.md). Scoping restrictions also apply to all children tables of the Connection \[sys\_connection\] and Discovery Credentials \[discovery\_credentials\] tables. Empty fields and other scopes are not restricted.

**Note:** Scope protections are only enabled for specific secured scopes to avoid confusion when setting up new records. If someone makes a connection in their scoped application scope, it doesn't have automatic scope restriction.

**Parent Topic:**[Explore credentials, connections, and aliases](credentials-connections-alias.md)

