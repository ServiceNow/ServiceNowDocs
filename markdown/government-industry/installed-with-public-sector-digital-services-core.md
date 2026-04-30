---
title: Components installed with Public Sector Digital Services Core
description: Several types of components such as tables, user roles, and flows are installed when you activate the Public Sector Digital Services Core plugin.The Public Sector Digital Services Core application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between users.Roles and personas help you to understand the different roles involved in Public Sector Digital Services.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 17
breadcrumb: [Set up your environment, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Components installed with Public Sector Digital Services Core

Several types of components such as tables, user roles, and flows are installed when you activate the Public Sector Digital Services Core plugin.

The following plugins are activated when you enable the Public Sector Digital Services Core plugin \(sn\_gsm\):

-   UI Components for Customer Portals \(com.sn\_ciwf\_ui\_cmpnt\)
-   Agency Support Model \(com.sn\_agency\_support\_model\)
-   Customer Service Case Types \(com.snc.csm\_case\_types\)
-   Customer Service Portal \(com.glide.service-portal.customer-portal\)
-   Customer Service Install Base Management \(com.snc.install\_base\)

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** For information about the roles installed when you activate the Public Sector Digital Services Core plugin, see [Roles installed with Public Sector Digital Services Core](installed-with-public-sector-digital-services-core.md#).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Government Service Case\[sn\_gsm\_government\_service\_case\]

</td><td>

Government service case table**Note:** This table is an extension of the Case \[sn\_customerservice\_case\] table.

</td></tr><tr><td>

Constituent Profile\[sn\_gsm\_constituent\_profile\]

</td><td>

Constituent profile table

</td></tr><tr><td>

Service Definition\[sn\_case\_type\_selection\_list\]

</td><td>

Service-definition table **Note:** This table is an extension of the Product Model \[cmdb\_model\] table.

</td></tr><tr><td>

Business Registration Request \[sn\_gsm\_business\_registration\]

</td><td>

Table for a new business registration request

</td></tr></tbody>
</table>## Flows installed

<table id="table_f55_gbp_rsb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create blocked by record if Case Task is associated with government case\[create\_blocked\_by\_record\_if\_case\_task\_is\_associated\_with\_government\_case\]

</td><td>

Creates a blocked by record if the Case Task is associated with a government case.

</td></tr><tr><td>

Create blocked by record if Government case needs customer information\[create\_blocked\_by\_record\_if\_case\_needs\_customer\_information\]

</td><td>

Creates a blocked by record if the Government case needs more customer information.

</td></tr><tr><td>

Resolve blocked by record if Case Task is closed and associated with Government Case\[resolve\_blocked\_by\_record\_if\_case\_task\_is\_closed\_and\_associated\_with\_government\_case\]

</td><td>

Removes the blocked by record for the associated Government case if the Government case is resolved.

</td></tr><tr><td>

Resolve blocked by record if user information is provided for Government case\[resolve\_blocked\_by\_record\_if\_user\_information\_is\_provided\_for\_govt\_case\]

</td><td>

Removes the blocked by record if the case task is closed.

</td></tr></tbody>
</table>**Parent Topic:**[Set up your environment in Public Sector Digital Services](../concept/psds-config-set-up-your-environment.md)

## Roles installed with Public Sector Digital Services Core

The Public Sector Digital Services Core application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between users.

### Core Roles

<table id="table_qw1_zs3_g5b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

constituent\[sn\_gsm.constituent\]

</td><td>

Enables constituents to request services and manage their information, government service cases, and services received.

</td><td>

-   sn\_install\_base.sold\_product\_authorized\_consumer
-   sn\_gsm.service\_received\_read\_granular
-   sn\_customerservice.consumer
-   sn\_gsm.case\_write\_granular

</td></tr><tr><td>

constituent\_agent\[sn\_gsm.constituent\_agent\]

</td><td>

Enables agents to perform the following actions:-   Read, write, and update government service cases for all constituents.
-   Read, write, and update constituent records.

</td><td>

-   sn\_gsm.report\_viewer
-   sn\_gsm.case\_writer
-   sn\_gsm.service\_offered\_writer
-   sn\_customerservice.consumer\_agent
-   sn\_gsm.constituent\_writer
-   interaction\_agent

</td></tr><tr><td>

constituent\_contributor\[sn\_gsm.constituent\_contributor\]

</td><td>

Enables users to request services and raise government service cases on behalf of any constituent.

</td><td>

-   sn\_customerservice.consumer\_contributor
-   sn\_gsm.contributor\_creator
-   sn\_customerservice.case\_authorized\_contributor

</td></tr><tr><td>

constituent\_admin\[sn\_gsm.constituent\_admin\]

</td><td>

Provides agents with admin access and enables them to create, read, update, and delete constituent records.

</td><td>

sn\_gsm.constituent\_writer

</td></tr><tr><td>

constituent\_writer\[sn\_gsm.constituent\_writer\]

</td><td>

Provides agents with access to create, read, and update constituent records.

</td><td>

sn\_gsm.constituent\_viewer

</td></tr><tr><td>

License &amp; Permits Install base writer\[sn\_gsm\_lic\_prmt.ib\_writer\]

</td><td>

Provides create, read, and write access to Install base items.

</td><td>

sn\_gsm\_lic\_prmt.ib\_writer

</td></tr><tr><td>

constituent\_viewer\[sn\_gsm.constituent\_viewer\]

</td><td>

Provides agents with read-only access to constituent records.

</td><td>

sn\_customerservice.customer\_data\_viewer

</td></tr><tr><td>

License &amp; Permits Install base Item viewer\[sn\_gsm\_lic\_prmt.ib\_viewer\]

</td><td>

This role provides read access to Install base items

</td><td>

-   sn\_gsm\_lic\_prmt.business\_agent
-   sn\_gsm\_lic\_prmt.ib\_writer
-   sn\_gsm\_lic\_prmt.constituent\_agent

</td></tr></tbody>
</table><table id="table_ekd_mt3_g5b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

business\_contact\[sn\_gsm.business\_contact\]

</td><td>

Enables business stakeholders to request services and manage information, government service cases, and services received.

</td><td>

-   sn\_customerservice.customer
-   sn\_install\_base.sold\_product\_authorized\_consumer
-   sn\_gsm.service\_received\_read\_granular
-   sn\_gsm.case\_write\_granular

</td></tr><tr><td>

business\_contact\_admin\[sn\_gsm.business\_contact\_admin\]

</td><td>

Provides a business stakeholder with admin access to a business account. This role has access to all the data within the business account.

</td><td>

-   sn\_customerservice.customer\_admin
-   sn\_gsm.business\_contact

</td></tr><tr><td>

business\_case\_manager\[sn\_gsm.business\_case\_manager\]

</td><td>

Enables a business stakeholder to manage government service cases for a business account and associated child accounts. This role can perform the following actions:-   Create a case on behalf of another business contact.
-   View a list of cases belonging to the business.
-   Edit cases belonging to the business.

</td><td>

-   sn\_customerservice.customer\_case\_manager
-   sn\_gsm.business\_contact

</td></tr><tr><td>

business\_contributor\[sn\_gsm.business\_contributor\]

</td><td>

Enables business stakeholders to request services and raise government service cases on behalf of any business.

</td><td>

-   sn\_customerservice.relationship\_contributor
-   sn\_gsm.contributor\_creator
-   sn\_customerservice.case\_authorized\_contributor

</td></tr><tr><td>

business\_partner\[sn\_gsm.business\_partner\]

</td><td>

Enables business partners to create, view, and edit government service cases from their own account or from a business account that they are associated with.

</td><td>

-   sn\_customerservice.partner
-   sn\_gsm.business\_contact

</td></tr><tr><td>

business\_partner\_admin\[sn\_gsm.business\_partner\_admin\]

</td><td>

Provides a business stakeholder with admin access to a partner account. This user can access all the data within the partner account and the government service cases created by the partners.

</td><td>

-   sn\_customerservice.partner\_admin
-   sn\_gsm.business\_partner
-   sn\_gsm.business\_contact
-   sn\_gsm.business\_contact\_admin

</td></tr><tr><td>

business\_agent\[sn\_gsm.business\_agent\]

</td><td>

Enables agents to perform the following actions:-   Read, write, and update government service cases for all business accounts.
-   Read, write, and update business records.

</td><td>

-   sn\_gsm.report\_viewer
-   sn\_gsm.case\_writer
-   sn\_gsm.service\_offered\_writer
-   sn\_customerservice.consumer\_agent
-   sn\_gsm.business\_writer
-   interaction\_agent

</td></tr><tr><td>

Social Benefits Business Contributor\[sn\_gsm\_soc\_bnfts.business\_contributor\]

</td><td>

Enables users to request service and raise Social Benefits cases on behalf of any business. This allows business stakeholders to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.business\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td></tr></tbody>
</table><table id="table_wqx_nt3_g5b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

agency\_agent \[sn\_gsm.agency\_agent\]

</td><td>

Enables agency agents to create and fulfill government service cases for the businesses and business contacts associated with the agency.

</td><td>

sn\_customerservice.svc\_location\_agent

</td></tr><tr><td>

agency\_constituent\_agent \[sn\_gsm.agency\_constituent\_agent\]

</td><td>

Enables agency agents to create and fulfill government service cases for constituents and households associated with the agency.

</td><td>

sn\_customerservice.svc\_location\_consumer\_agent

</td></tr><tr><td>

external\_reviewer\[sn\_gsm\_grnt\_mgmt.external\_reviewer\]

</td><td>

Enables users to review and score grant proposals.

</td><td>

-   sn\_svc\_appl\_pgm\_mg.resource\_role\_viewer
-   sn\_svc\_appl\_pgm\_mg.milestone\_viewer
-   sn\_svc\_appl\_pgm\_mg.resource\_mapping\_viewer
-   sn\_svc\_appl\_pgm\_mg.scoring\_framework\_attribute\_writer
-   sn\_svc\_appl\_pgm\_mg.business\_calendar\_entry\_viewer
-   sn\_svc\_appl\_pgm\_mg.resource\_assignment\_viewer
-   sn\_svc\_appl\_pgm\_mg.scoring\_framework\_viewer
-   sn\_svc\_appl\_pgm\_mg.planning\_item\_viewer

</td></tr><tr><td>

License &amp; Permit Constituent Agent\[sn\_gsm\_lic\_prmt.constituent\_agent\]

</td><td>

Enables users to work on License &amp; Permit cases for all constituents. It includes the ability to read/write/update all License &amp; Permit cases and constituent records

</td><td>

-   sn\_gsm.constituent\_agent
-   sn\_gsm\_lic\_prmt.case\_writer
-   sn\_gsm\_lic\_prmt.report\_viewer
-   sn\_gsm\_lic\_prmt.ib\_viewer

-   sn\_gsm\_lic\_prmt.manager


</td></tr><tr><td>

agency\_contributor\[sn\_gsm.agency\_contributor\]

</td><td>

Enables agency agents to request services and raise government service cases on behalf of the agency.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_gsm.contributor\_creator
-   sn\_customerservice.case\_authorized\_contributor

</td></tr><tr><td>

License &amp; Permit Agency Contributor\[sn\_gsm\_lic\_prmt.agency\_contributor\]

</td><td>

Enables users to request service and raise License &amp; Permit cases for their service organization \(business location\). This role is agnostic to internal and external.

</td><td>

-   sn\_gsm.agency\_contributor
-   sn\_gsm\_lic\_prmt.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor


</td></tr><tr><td>

agency\_manager\[sn\_gsm.agency\_manager\]

</td><td>

Enables an agency manager to perform the following actions:-   Create and update government service cases for constituents, households, business, and business contacts.
-   Manage data for constituents and households associated with the agencies within the agency hierarchy.
-   Manage data for businesses and business contacts associated with the agencies within the agency hierarchy.

</td><td>

-   sn\_customerservice.svc\_location\_manager
-   sn\_gsm.agency\_agent
-   sn\_gsm.agency\_constituent\_agent

</td></tr><tr><td>

License &amp; Permit Agency Manager\[sn\_gsm\_lic\_prmt.agency\_manager\]

</td><td>

Enables users to manage data for agencies in the manager's agency hierarchy.

</td><td>

-   sn\_gsm.agency\_manager
-   sn\_gsm\_lic\_prmt.agency\_constituent\_agent
-   sn\_gsm\_lic\_prmt.agency\_agent

</td></tr><tr><td>

License &amp; Permit Agency Constituent Agent\[sn\_gsm\_lic\_prmt.agency\_constituent\_agent\]

</td><td>

Enables users to manage data for agencies in the constituent agent's agency hierarchy.

</td><td>

-   sn\_gsm.agency\_constituent\_agent

-   contract\_manager
-   decision\_table\_reader
-   sn\_gsm\_lic\_prmt.agency\_manager


</td></tr><tr><td>

agency\_manager\_contributor\[sn\_gsm.agency\_manager\_contributor\]

</td><td>

Enables users to create, update, view, and approve cases. Allows them to register and remove staff across all agencies they manage. 

</td><td>

-   "sn\_gsm.business\_contributor
-   sn\_gsm.government\_agency\_contributor
-   sn\_gsm.constituent\_contributor
-   sn\_gsm.government\_agency\_contributor
-   sn\_gsm.agency\_manager\_core
-   sn\_customerservice.svc\_location\_manager\_contributor"

</td></tr><tr><td>

License &amp; Permit Agency Manager Contributor\[sn\_gsm\_lic\_prmt.agency\_manager\_contributor\]

</td><td>

Enables users to create, update, view, and approve cases. They can also register and remove staff across all agencies they manage. 

</td><td>

-   sn\_gsm\_lic\_prmt.business\_contributor
-   sn\_gsm\_lic\_prmt.agency\_relationship\_manager

-   sn\_gsm\_lic\_prmt.constituent\_contributor
-   sn\_gsm\_lic\_prmt.agency\_contributor
-   sn\_gsm\_lic\_prmt.agency\_manager\_core
-   sn\_gsm.agency\_manager\_contributor

</td></tr><tr><td>

relationship\_manager\[sn\_gsm.agency\_relationship\_manager\]

</td><td>

Enables users to view cases across all the external agencies where they have location\_relationship\_manager responsibility.

</td><td>

-   sn\_bus\_loc.location\_relationship\_manager
-   sn\_gsm.agency\_manager\_contributor

</td></tr><tr><td>

License &amp; Permits Agency Manager Core\[sn\_gsm\_lic\_prmt.agency\_manager\_core\]

</td><td>

Granular role to manage agency staff registrations and staff relationships with businesses, constituents, and households for all the agencies within the hierarchy.

</td><td>

-   sn\_gsm.agency\_manager\_core
-   contract\_manager

</td></tr><tr><td>

License &amp; Permit Agency Relationship Manager\[sn\_gsm\_lic\_prmt.agency\_relationship\_manager\]

</td><td>

Enables users to view cases across all the external agencies where they have location\_relationship\_manager responsibility.

</td><td>

-   sn\_gsm.agency\_relationship\_manager
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor

</td></tr><tr><td>

service\_manager\[sn\_gsm.service\_manager\]

</td><td>

Enables a service manager to perform the following actions:-   Manage all work performed by agents working on government service cases.
-   Read, write, update, and delete all government service cases.
-   Read, write, update, and delete all constituent, business, and agency records.

</td><td>

-   sn\_gsm.service\_offered\_admin
-   sn\_gsm.service\_offered\_writer
-   sn\_gsm.constituent\_agent
-   sn\_gsm.constituent\_admin
-   sn\_gsm.business\_agent

</td></tr><tr><td>

License &amp; Permit Case Task Agent\[sn\_gsm\_lic\_prmt.case\_task\_agent\]

</td><td>

Provides users the ability to create and fulfill License &amp; Permit cases for the constituents and households in the agent's agency.

</td><td>

-   sn\_gsm\_lic\_prmt.contributor\_editor
-   sn\_gsm\_lic\_prmt.case\_viewer
-   sn\_gsm.case\_task\_agent

</td></tr><tr><td>

License &amp; Permit Case Viewer\[sn\_gsm\_lic\_prmt.case\_viewer\]

</td><td>

This role provides users read only access to License &amp; Permit case records.

</td><td>

-   sn\_gsm.case\_viewer
-   decision\_table\_reader
-   sn\_gsm\_lic\_prmt.case\_writer

-   sn\_gsm\_lic\_prmt.case\_task\_agent

</td></tr><tr><td>

License &amp; Permit Agency Business Agent\[sn\_gsm\_lic\_prmt.agency\_agent\]

</td><td>

Enables users to create and fulfill License &amp; Permit cases for the accounts and contacts in the agent's agency.

</td><td>

-   sn\_gsm.agency\_agent
-   contract\_manager
-   decision\_table\_reader
-   sn\_gsm\_lic\_prmt.agency\_manager


</td></tr><tr><td>

License &amp; Permit Business Agent\[sn\_gsm\_lic\_prmt.business\_agent\]

</td><td>

Provides users the ability to work on license and permit cases for business. It includes the ability to read, write, or update all license and permit cases and business records.

</td><td>

-   sn\_gsm\_lic\_prmt.report\_viewer

-   sn\_gsm\_lic\_prmt.case\_writer
-   sn\_gsm.business\_agent
-   sn\_gsm\_lic\_prmt.ib\_viewer

-   sn\_gsm\_lic\_prmt.manager


</td></tr><tr><td>

social\_benefits\_agency\_agent\[sn\_gsm\_soc\_bnfts.agency\_agent\]

</td><td>

Provides users the ability to create and fulfill cases for the accounts and contacts in the agent's agency.

</td><td>

-   sn\_gsm.agency\_agent
-   decision\_table\_reader
-   contract\_manager

</td></tr><tr><td>

social\_benefits\_agency\_constituent\_agent\[sn\_gsm\_soc\_bnfts.agency\_constituent\_agent\]

</td><td>

Provides users the ability to create and fulfill cases for the constituents and households in the agent's agency.

</td><td>

-   decision\_table\_reader
-   sn\_gsm.agency\_constituent\_agent
-   contract\_manager

</td></tr><tr><td>

social\_benefits\_agency\_contributor\[sn\_gsm\_soc\_bnfts.agency\_contributor\]

</td><td>

Enables users to request service and raise Social Benefits cases for their agency\(business location\). This role is agnostic to internal and external.

</td><td>

-   sn\_gsm.government\_agency\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td></tr><tr><td>

social\_benefits\_agency\_manager\[sn\_gsm\_soc\_bnfts.agency\_manager\]

</td><td>

Provides users the ability to manage data for agencies in the manager's agency hierarchy.

</td><td>

-   sn\_gsm\_soc\_bnfts.agency\_agent
-   sn\_gsm\_soc\_bnfts.agency\_manager\_core
-   sn\_gsm.agency\_manager
-   sn\_gsm\_soc\_bnfts.agency\_constituent\_agent

</td></tr><tr><td>

social\_benefits\_agency\_manager\_contributor\[sn\_gsm\_soc\_bnfts.agency\_manager\_contributor\]

</td><td>

Manage agencies and create a case for a business, household, or constituent at the agency or any child agency.

</td><td>

-   sn\_gsm\_soc\_bnfts.agency\_contributor
-   sn\_gsm\_soc\_bnfts.business\_contributor
-   sn\_gsm\_soc\_bnfts.agency\_manager\_core
-   sn\_gsm\_soc\_bnfts.constituent\_contributor
-   sn\_gsm.agency\_manager\_contributor

</td></tr><tr><td>

social\_benefits\_agency\_manager\_core\[sn\_gsm\_soc\_bnfts.agency\_manager\_core\]

</td><td>

Granular role to manage agency staff registrations and staff relationships with businesses, constituents, and households for all the agencies within the hierarchy.

</td><td>

-   sn\_gsm.agency\_manager\_core
-   contract\_manager

</td></tr><tr><td>

social\_benefits\_agency\_relationship\_manager\[sn\_gsm\_soc\_bnfts.agency\_relationship\_manager\]

</td><td>

Manages and monitors all the activities performed by the agencies. It also acts as an internal point of contact for the agencies.

</td><td>

-   sn\_gsm\_soc\_bnfts.agency\_manager\_contributor
-   sn\_gsm.agency\_relationship\_manager

</td></tr><tr><td>

social\_benefits\_business\_agent\[sn\_gsm\_soc\_bnfts.business\_agent\]

</td><td>

Provides users the ability to work on Social Benefits cases for business. It includes the ability to read/write/update all Social Benefits cases and business records.

</td><td>

-   sn\_gsm\_soc\_bnfts.case\_writer
-   sn\_gsm\_soc\_bnfts.report\_viewer
-   sn\_gsm.business\_agent
-   sn\_gsm\_soc\_bnfts.ib\_viewer

</td></tr><tr><td>

Social Benefits Case Task Agent\[sn\_gsm\_soc\_bnfts.case\_task\_agent\]

</td><td>

Enables users to work on Social Benefits case tasks.

</td><td>

-   sn\_gsm\_soc\_bnfts.case\_viewer
-   sn\_gsm\_soc\_bnfts.contributor\_editor
-   sn\_gsm.case\_task\_agent

</td></tr><tr><td>

Social Benefits Constituent Agent\[sn\_gsm\_soc\_bnfts.constituent\_agent\]

</td><td>

Provides users the ability to work on Social Benefits cases for all constituents. It includes the ability to read/write/update all cases and constituent records

</td><td>

-   sn\_gsm\_soc\_bnfts.case\_writer
-   sn\_gsm\_soc\_bnfts.report\_viewer
-   sn\_gsm.constituent\_agent
-   sn\_gsm\_soc\_bnfts.ib\_viewer

</td></tr><tr><td>

Social Benefits Manager\[sn\_gsm\_soc\_bnfts.manager\]

</td><td>

Provides users the ability to manage all work performed by agents working on Social Benefits cases \(constituent and business\). Users with this role have the ability to read/write/update/delete all Social Benefits cases and constituent/business records.

</td><td>

-   sn\_gsm\_soc\_bnfts.ib\_admin
-   sn\_gsm\_soc\_bnfts.business\_agent
-   sn\_gsm.government\_service\_manager
-   sn\_gsm\_soc\_bnfts.constituent\_agent
-   sn\_majorissue\_mgt.major\_issue\_manager

</td></tr><tr><td>

Social Benefits Relationship Agent\[sn\_gsm\_soc\_bnfts.relationship\_agent\]

</td><td>

Enables users to work on Social Benefits cases only for customers with whom they have relationships.

</td><td>

-   sn\_gsm\_soc\_bnfts.report\_viewer
-   decision\_table\_reader
-   sn\_gsm.relationship\_agent
-   contract\_manager

</td></tr></tbody>
</table><table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

admin\[sn\_gsm.admin\]

</td><td>

Provides a user with delegated admin access to scoped applications created on the Public Sector Digital Services platform.

</td><td>

sn\_gsm.service\_manager

</td></tr><tr><td>

service\_offered\_admin\[sn\_gsm.service\_offered\_admin\]

</td><td>

Provides users with admin access and enables them to create, read, update, and delete services-offered records and services-received records.

</td><td>

sn\_gsm.service\_offered\_writer

</td></tr><tr><td>

grant\_program\_manager sn\_gsm\_grnt\_mgmt.program\_manager

</td><td>

Provides users with the program manager role to create grant program records.

</td><td>

-   model\_manager
-   sn\_gsm.resource\_role\_writer
-   sn\_gsm.informational\_resource\_mapping\_wrirter
-   sn\_gsm.business\_calendar\_entry\_viewer
-   sn\_gsm.business\_agent
-   sn\_gsm.scoring\_framework\_writer
-   sn\_doc.reader
-   sn\_gsm.resource\_assignment\_writer
-   sn\_pace.mapping\_admin
-   sn\_gsm.milestone\_writer
-   sn\_gsm.goal\_viewer
-   sn\_gsm.scoring\_framework\_attribute\_writer
-   sn\_gsm.scoring\_framework\_attribute\_writer
-   sn\_gsm.constituent\_agent
-   sn\_gsm.planning\_item\_writer

</td></tr><tr><td>

grant\_admin sn\_gsm\_grnt\_mgmt.grant\_admin

</td><td>

Provides users with admin access and enables them to create, read, update, and edit grant proposals in the grant setup and proposals playbooks.

</td><td>

-   sn\_gsm.admin
-   sn\_svc\_appl\_pgm\_mg.grant\_program\_director

</td></tr><tr><td>

grant\_program\_director sn\_gsm\_grnt\_mgmt.grant\_director

</td><td>

Provides users with the grant program director role, which consists of the grant program manager and the government service manager roles.

</td><td>

-   sn\_gsm\_grnt\_mgmt.program\_manager
-   sn\_gsm.government\_service\_manager

</td></tr><tr><td>

grant\_case\_writer sn\_gsm\_grnt\_mgmt.case\_writer

</td><td>

Provides users with access to create, read, and update grant management case records.

</td><td>

-   sn\_gsm\_grnt\_mgmt.case\_viewer
-   sn\_gsm.case\_writer
-   contract\_manager

</td></tr><tr><td>

grant\_case\_viewer sn\_gsm\_grnt\_mgmt.case\_viewer

</td><td>

Provides users with read-only access to grant management case records.

</td><td>

-   sn\_gsm.case\_viewer
-   decision\_table\_reader
-   sn\_gsm\_grnt\_mgmt.case\_writer

</td></tr><tr><td>

license\_permit\_admin\[sn\_gsm\_lic\_prmt.admin\]

</td><td>

Enables users to manage all work performed by agents working on License &amp; Permit cases \(constituent and business\). Users with this role have the ability to read/write/update/delete all License &amp; Permit cases and constituent/business records.

</td><td>

-   sn\_gsm\_lic\_prmt.manager
-   sn\_gsm.admin

</td></tr><tr><td>

social\_benefits\_admin\[sn\_gsm\_soc\_bnfts.admin\]

</td><td>

Provides delegated admin access to scoped applications created on the Social Benefits Playbook.

</td><td>

-   sn\_gsm.admin
-   sn\_gsm\_soc\_bnfts.manager

</td></tr><tr><td>

License &amp; Permits Install base admin\[sn\_gsm\_lic\_prmt.ib\_admin\]

</td><td>

This role provides create,read,write, and delete access to Install base items.

</td><td>

-   sn\_gsm\_lic\_prmt.ib\_writer

-   sn\_gsm\_lic\_prmt.manager

</td></tr><tr><td>

License &amp; Permits Case Writer\[sn\_gsm\_lic\_prmt.case\_writer\]

</td><td>

This role provides users access to create, read and update License &amp; Permits case records.

</td><td>

-   sn\_gsm\_lic\_prmt.case\_viewer

-   sn\_gsm.case\_writer
-   contract\_manager
-   sn\_gsm\_lic\_prmt.business\_agent

-   sn\_gsm\_lic\_prmt.constituent\_agent

</td></tr><tr><td>

service\_offered\_admin\[sn\_gsm.service\_offered\_admin\]

</td><td>

 

</td><td>

 

</td></tr><tr><td>

service\_offered\_writer\[sn\_gsm.service\_offered\_writer\]

</td><td>

Provides users with access to create, read, and update services-offered records and services-received records.

</td><td>

sn\_gsm.service\_offered\_viewer

</td></tr><tr><td>

service\_offered\_viewer\[sn\_gsm.service\_offered\_viewer\]

</td><td>

Provides users with read-only access to services offered records and services-received records.

</td><td>

sn\_customerservice.customer\_data\_viewer

</td></tr><tr><td>

case\_writer\[sn\_gsm.case\_writer\]

</td><td>

Provides agents with access to create, read, and update government service cases.

</td><td>

sn\_gsm.case\_viewer

</td></tr><tr><td>

case\_viewer\[sn\_gsm.case\_viewer\]

</td><td>

Provides agents with read-only access to government service cases.

</td><td>

None

</td></tr><tr><td>

contributor\_creator\[sn\_gsm.contributor\_creator\]

</td><td>

Enables agents or business stakeholders to create government service cases and is included in the top-level contributor roles. This role can create cases but cannot view other cases.

</td><td>

None

</td></tr><tr><td>

relationship\_agent\[sn\_gsm.relationship\_agent\]

</td><td>

Enables agents to work on government service cases for customers that they have relationship with.

</td><td>

-   sn\_gsm.report\_viewer
-   sn\_customerservice.relationship\_agent

</td></tr><tr><td>

relationship\_contributor\[sn\_gsm.relationship\_contributor\]

</td><td>

Enables business stakeholders to raise government service cases on behalf of customers that they have relationship with.

</td><td>

-   sn\_customerservice.relationship\_contributor
-   sn\_gsm.contributor\_creator
-   sn\_customerservice.case\_authorized\_contributor

</td></tr><tr><td>

Social Benefits Case Viewer\[sn\_gsm\_soc\_bnfts.case\_viewer\]

</td><td>

This role provides users read only access to Social Benefits Case records.

</td><td>

-   sn\_gsm.case\_viewer
-   decision\_table\_reader

</td></tr><tr><td>

Social Benefits Case Writer\[sn\_gsm\_soc\_bnfts.case\_writer\]

</td><td>

This role provides users access to create, read and update Social Benefits Case records.

</td><td>

-   sn\_gsm\_soc\_bnfts.case\_viewer
-   sn\_gsm.case\_writer
-   contract\_manager

</td></tr></tbody>
</table>### Granular roles

You can use predefined functional and granular roles installed with Public Sector Digital Services to establish relationships between users and public sector entities. These functional and granular roles provide different levels of access to public sector data, to help maintain data security.

-   Functional roles: A set of roles required to perform a function or meaningful action that requires access on multiple entities.
-   Granular roles: Roles that provide access to cases, services used, and related public sector entities. One or more granular roles can be bundled together as a functional role.

A granular model helps protect data by granting the appropriate level of access to the corresponding public sector entities. With this functionality, each role is associated with a set of privileges or responsibilities that determine users’ access to certain information. You can have fine-grained access control by setting granular policies that authorize individuals to access the information needed to work efficiently and effectively, ultimately helping improve the constituent experience.

For example, if you extend the Government Service Case table or other tables in the Public Sector Digital Services app, you must replicate the access control lists for the extended tables. You can assign granular roles to public sector users to control access to those extended tables.

<table id="table_gfm_vbp_g5b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

case\_create\_granular\[sn\_gsm.case\_create\_granular\]

</td><td>

Provides constituents or business stakeholders with granular create access to government service cases.

</td><td>

sn\_gsm.case\_read\_granular

</td></tr><tr><td>

case\_read\_granular\[sn\_gsm.case\_read\_granular\]

</td><td>

Provides constituents or business stakeholders with granular read access to government service cases.

</td><td>

sn\_customerservice.case\_read\_granular

</td></tr><tr><td>

case\_write\_granular\[sn\_gsm.case\_write\_granular\]

</td><td>

Provides constituents or business stakeholders with granular write access to government service cases.

</td><td>

-   sn\_gsm.case\_create\_granular
-   sn\_gsm.case\_read\_granular

</td></tr><tr><td>

service\_received\_read\_granular\[sn\_gsm.service\_received\_read\_granular\]

</td><td>

Provides constituents or business stakeholders with granular read access to services-received records.

</td><td>

sn\_install\_base.sold\_product\_read\_granular

</td></tr><tr><td>

License &amp; Permits Install base read granular\[sn\_gsm\_lic\_prmt.ib\_read\_granular\]

</td><td>

Provides granular read access to issued License and Permits.

</td><td>

-   sn\_install\_base.install\_base\_read\_granular
-   sn\_gsm.business\_contact

-   sn\_gsm.constituent

</td></tr><tr><td>

License &amp; Permits Agency Manager Core\[sn\_gsm\_lic\_prmt.agency\_manager\_core\]

</td><td>

Granular role to manage agency staff registrations and staff relationships with businesses, constituents, and households for all the agencies within the hierarchy.

</td><td>

-   sn\_gsm.agency\_manager\_core
-   contract\_manager
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor

-   sn\_gsm\_lic\_prmt.agency\_manager

</td></tr><tr><td>

License &amp; Permits Contributor Creator\[sn\_gsm\_lic\_prmt.contributor\_creator\]

</td><td>

Enables users to create license and permit cases and is included in the top-level contributor roles. It only allows record creation but does not allow visibilty to a record on its own.

</td><td>

-   sn\_gsm.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_contributor

-   sn\_gsm\_lic\_prmt.business\_contributor
-   sn\_gsm\_lic\_prmt.constituent\_contributor
-   sn\_gsm\_lic\_prmt.relationship\_contributor

</td></tr><tr><td>

Social Benefits install base admin\[sn\_gsm\_soc\_bnfts.ib\_admin\]

</td><td>

This role provides create,read,write, and delete access to Install base items.

</td><td>

sn\_gsm\_soc\_bnfts.ib\_writer

</td></tr><tr><td>

Social Benefits install base read granular\[sn\_gsm\_soc\_bnfts.ib\_read\_granular\]

</td><td>

Provides granular read access to issued Social Benefits.

</td><td>

sn\_install\_base.install\_base\_read\_granular

</td></tr><tr><td>

Social Benefits install base viewer\[sn\_gsm\_soc\_bnfts.ib\_viewer\]

</td><td>

Provides read access to Install base items.

</td><td>

None

</td></tr><tr><td>

Social Benefits install base writer\[sn\_gsm\_soc\_bnfts.ib\_writer\]

</td><td>

Provides create, read and write access to Install base items.

</td><td>

sn\_gsm\_soc\_bnfts.ib\_viewer

</td></tr></tbody>
</table>### Business Stakeholder Roles

Business Stakeholder for Public Sector Digital Services includes plugins and roles that provide access to business stakeholder features.

Admins with access to Business Stakeholder can provide Business Stakeholder users with the rights to the following actions:

-   Create cases on behalf of a business or an agency \(service organization\)
-   View cases, case tasks, and business data.
-   Approve requests.

<table id="table_thp_4gp_bvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Constituent contributor\[sn\_gsm.constituent\_contributor\]

</td><td>

Enables users to request services and raise government service cases on behalf of any constituent.

</td><td>

-   sn\_customerservice.consumer\_contributor
-   sn\_gsm.contributor\_creator

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal and external

</td></tr><tr><td>

License &amp; Permit Constituent contributor\[sn\_gsm\_lic\_prmt.constituent\_contributor\]

</td><td>

This role enables users to request for service and raise License &amp; Permit cases on behalf of any constituent. This allow business stakeholders to act as a requestor on of behalf of customers.

</td><td>

-   sn\_gsm.constituent\_contributor
-   sn\_gsm\_lic\_prmt.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor


</td><td>

 

</td><td>

 

</td></tr><tr><td>

Business contributor\[sn\_gsm.business\_contributor\]

</td><td>

Enables business stakeholders to request services and raise government service cases on behalf of any business.

</td><td>

-   sn\_customerservice.relationship\_contributor
-   sn\_gsm.contributor\_creator

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

internal and external

</td></tr><tr><td>

License &amp; Permit Business Contributor\[sn\_gsm\_lic\_prmt.business\_contributor\]

</td><td>

This role enables users to request for service and raise License &amp; Permit cases on behalf of any business. This allow business stakeholders to act as a requester on of behalf of customers.

</td><td>

-   sn\_gsm.business\_contributor
-   sn\_gsm\_lic\_prmt.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor


</td><td>

 

</td><td>

 

</td></tr><tr><td>

Relationship contributor\[sn\_gsm.relationship\_contributor\]

</td><td>

Enables business stakeholders to raise government service cases on behalf of customers with which they have a relationship.

</td><td>

-   sn\_customerservice.relationship\_contributor
-   sn\_gsm.contributor\_creator

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal and external

</td></tr><tr><td>

License &amp; Permit Relationship Contributor\[sn\_gsm\_lic\_prmt.relationship\_contributor\]

</td><td>

Enables users to raise License &amp; Permit cases on behalf of customers with whom they have relationships. This allows business stakeholder access to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.relationship\_contributors
-   n\_gsm\_lic\_prmt.contributor\_creator

</td><td>

 

</td><td>

 

</td></tr><tr><td>

License &amp; Permit Contributor Editor\[sn\_gsm\_lic\_prmt.contributor\_editor\]

</td><td>

Grants restrictive write access to the fields on the License and Permit Case form.

</td><td>

-   sn\_gsm.contributor\_creator
-   sn\_gsm\_lic\_prmt.case\_task\_agent


</td><td>

 

</td><td>

 

</td></tr><tr><td>

Social Benefits Constituent Contributor\[sn\_gsm\_soc\_bnfts.constituent\_contributor\]

</td><td>

This role enables users to request service and raise Social Benefits cases on behalf of any constituent. This allows business stakeholders to act as a requestor on behalf of customers.

</td><td>

-   sn\_gsm.constituent\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Social Benefits Contributor Creator\[sn\_gsm\_soc\_bnfts.contributor\_creator\]

</td><td>

Enables users to create Social Benefits cases and is included in the top-level contributor roles. It only allows record creation but does not allow visibility to a record on its own.

</td><td>

-   sn\_gsm.constituent\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Social Benefits Contributor Editor\[sn\_gsm\_soc\_bnfts.contributor\_editor\]

</td><td>

Grants restrictive write access to the fields on the Social Benefits Case form.

</td><td>

sn\_gsm.contributor\_creator

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Social Benefits Relationship Contributor\[sn\_gsm\_soc\_bnfts.relationship\_contributor\]

</td><td>

Enables users to raise Social Benefits cases on behalf of customers with whom they have relationships. This allows business stakeholder access to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.relationship\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table><table id="table_rks_v3p_bvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Agency contributor\[sn\_gsm.agency\_contributor\]

</td><td>

Enables agency agents to request services and raise government service cases on behalf of the agency.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_gsm.contributor\_creator

</td><td>

Agency Support Model \(com.sn\_agency\_support\_model\)

</td><td>

Internal and external

</td></tr></tbody>
</table><table id="table_ks2_flp_bvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Case viewer\[sn\_gsm.case\_viewer\]

</td><td>

Provides agents with read-only access to government service cases.

</td><td>

None

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal

</td></tr><tr><td>

Constituent viewer\[sn\_gsm.constituent\_viewer\]

</td><td>

Provides agents with read-only access to constituent records.

</td><td>

sn\_customerservice.customer\_data\_viewer

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal

</td></tr><tr><td>

Business viewer\[sn\_gsm.business\_viewer\]

</td><td>

 

</td><td>

 

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal

</td></tr><tr><td>

Services offered viewer\[sn\_gsm.service\_offered\_viewer\]

</td><td>

Provides users with read-only access to services offered records and services received records.

</td><td>

sn\_customerservice.customer\_data\_viewer

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal

</td></tr><tr><td>

Government services received viewer\[sn\_gsm.service\_received\_viewer\]

</td><td>

Provides users with read-only access to services received records.

</td><td>

 

</td><td>

com.sn\_public\_sector\_digital\_services\_core

</td><td>

Internal

</td></tr></tbody>
</table><table id="table_xxg_f4p_bvb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

report\_viewer\[sn\_gsm.report\_viewer\]

</td><td>

Enables users to view reports on the Public Sector Digital Services platform.

</td><td>

None

</td></tr><tr><td>

grant\_management\_report\_viewersn\_gsm\_grnt\_mgmt.report\_viewer

</td><td>

Enables users to view reports about the grants management playbooks.

</td><td>

None

</td></tr><tr><td>

License &amp; Permit Report Viewer\[sn\_gsm\_lic\_prmt.report\_viewer\]

</td><td>

Enables users to view reports on the Public Sector Digital Services platform.

</td><td>

sn\_gsm.report\_viewer

</td></tr><tr><td>

social\_benefit\_report\_viewer\[sn\_gsm\_soc\_bnfts.report\_viewer\]

</td><td>

Provides users access to view reports Social Benefits Playbook.

</td><td>

sn\_gsm.report\_viewer

</td></tr></tbody>
</table>**Note:** Customers who have purchased a Public Sector Digital Services subscription can provide Business Stakeholder users with rights to actions listed under [Business Stakeholder for Customer Service Management](https://www.servicenow.com/docs/access?context=business-stakeholder-for-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

### Persona-based Roles in Public Sector Digital Services

Roles and personas help you to understand the different roles involved in Public Sector Digital Services.

Public Sector Digital Services supports users with the following basic job functions \(personas\).

Personas are defined as the individual roles that perform different tasks in Public Sector Digital Services.

<table id="table_qcv_ktt_ytb"><thead><tr><th>

Job function

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

System administrator, who has access to all system features, functions, and data, regardless of security restraints:

-   Administers specific scoped apps built using different case types.
-   Manages the information for constituents.

</td></tr><tr><td>

Constituent

</td><td>

End user, such as a citizen, residents, visitors, veterans:

-   Requests services from government agencies.
-   Tracks resolution of requests.

</td></tr><tr><td>

Business stakeholder

</td><td>

End user, such as business owner, business contact, business partner:

-   Requests services from government agencies.
-   Tracks resolution of requests.

</td></tr><tr><td>

Government agent

</td><td>

Fulfiller, such as constituent agent, business agent, agency agent:

-   Works on government service cases for all constituents. Can read, write, and update all government service cases and profile records.
-   Can belong to specific teams or agencies.
-   Can work on specific case types \(for example Licenses or Unemployment\).

</td></tr><tr><td>

Contributor

</td><td>

Business stakeholder or requester for constituents:

-   Help constituents or businesses with services that they need.
-   Submits requests on behalf of constituents and acts as proxy.

</td></tr><tr><td>

Government service manager

</td><td>

Manager of constituent and business services and agents supporting constituent services:

-   Administers services delivered to constituents, business stakeholders, and agency.
-   Can read, write, update, and delete all government service cases.
-   Can read, write, update, and delete all constituent, business, and agency records.
-   Improves service delivery and constituent satisfaction.

</td></tr></tbody>
</table>