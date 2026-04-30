---
title: Domain separation for Workspace records
description: Workspace supports standard domain separation. In a record, you can safely create another record in the correct domain, change the domain that the record associates with, and temporarily expand the domain scope of a record to a domain outside the record session.Expand the domain scope of a record temporarily to a domain outside the record session. The record expands to include related lists and reference field queries. This enables you to create a main record that applies to issues for more than one domain.Create a new record when the domain of the record is unknown and you have access to multiple domains.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Getting or adding information to a record, Working on records in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Domain separation for Workspace records

Workspace supports standard domain separation. In a record, you can safely create another record in the correct domain, change the domain that the record associates with, and temporarily expand the domain scope of a record to a domain outside the record session.

Workspace uses Cross-Tenant Intelligence to automatically handle the data, metadata, business logic, and processing context for tenants that have access to additional tenant data. Cross-tenant intelligence enables the following behavior when you create a record.

-   Records created from another record inherit the domain of the originating record.

-   Records created with a UI action from a record carry over the domain of the originating record.

-   Records created from a parent record, for example a related list, carry over the domain of the parent record.


For more information on Cross-Tenant Intelligence in Domain Separation, see [What is Domain Separation?](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Toggle domain scope of a record

Expand the domain scope of a record temporarily to a domain outside the record session. The record expands to include related lists and reference field queries. This enables you to create a main record that applies to issues for more than one domain.

### Before you begin

You must first have permission to access the domain that you want to toggle.

Role required: domain\_expand\_scope user role

### Procedure

1.  Navigate to **All** &gt; **Workspace**.

2.  Select a record.

3.  Click the overflow UI action icon \(![Overflow UI action icon.](../image/ellipsis-h-fill.png)\) in the record and select **Toggle Domain Scope**.

    You can now access related lists and reference field queries.

    **Note:** Domain scope doesn't toggle when the record is in the global domain or when your domain and the record domain match.

4.  Click the overflow UI action icon \(![Overflow UI action icon.](../image/ellipsis-h-fill.png)\) in the record and select **Toggle Domain Scope** to return the domain scope to the domain associated with the record.


## Create a record in a domain without a parent

Create a new record when the domain of the record is unknown and you have access to multiple domains.

### Before you begin

Change a domain by modifying the selection of the caller or company on the form of the record.

Role required: user

### Procedure

1.  Navigate to **All** &gt; **Workspace** &gt; **New record menu**.

2.  On the form, fill in the fields.

    The company or caller selected associates the record with the corresponding domain.

    **Note:** Data available for auto-population is limited to the domains you have access to.

3.  Click **Next**.


### Result

The new record includes data and rules specific to the domain.

