---
title: Roles installed with Public Sector Digital Services
description: The Public Sector Digital Services application uses roles to provide access to information, identify internal and external users, and establish different types of relationships between users. These roles control access to public sector data through UI-based features such as forms and lists.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 24
breadcrumb: [Components and roles installed, Reference, Public Sector Digital Services \(PSDS\)]
---

# Roles installed with Public Sector Digital Services

The Public Sector Digital Services application uses roles to provide access to information, identify internal and external users, and establish different types of relationships between users. These roles control access to public sector data through UI-based features such as forms and lists.

## Persona-based Roles in Public Sector Digital Services

Roles and personas help you to understand the different roles involved in Public Sector Digital Services.

Public Sector Digital Services supports users with the following basic job functions \(personas\). Personas are defined as the individual roles that perform different tasks in Public Sector Digital Services.

The following graphic shows the most common personas used throughout Public Sector Digital Services. ![Common Public Sector Digital Services personas](../image/PSDS_user_personas.png)

<table id="table_qcv_ktt_ytb"><thead><tr><th>

Job function

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Constituents

</td><td>

End user, such as citizens, visitors, residents, soldiers, veterans, etc. Constituents can:

-   Request services from government agencies.
-   Track resolution of requests.

</td></tr><tr><td>

Government case agents

</td><td>

Staff member of an agency​, such as a constituent agent, business agent, agency agent, that delivers services to constituents or other agencies, and can​ requests services from other agencies. Agents can:

-   Works on government service cases for all constituents. Can read, write, and update all government service cases and profile records.
-   Can belong to specific teams or agencies.
-   Can work on specific case types \(for example Licenses or Unemployment\).

</td></tr><tr><td>

Contributors

</td><td>

Business stakeholder or requester for constituents:

-   Help constituents or businesses with services that they need.
-   Submits requests on behalf of constituents and acts as proxy.

</td></tr><tr><td>

Admins

</td><td>

System administrator, who has access to all system features, functions, and data, regardless of security restraints. Admins can:

-   Administers specific scoped apps built using different case types.
-   Manages the information for constituents.

</td></tr><tr><td>

Business stakeholder

</td><td>

End user, such as business owner, business channel, or business partner. Business stakeholders can:

-   Request services from government agencies.
-   Track resolution of requests.

</td></tr><tr><td>

Business contact

</td><td>

An end user that is employed by a business. Business contacts can:-   Request services from the government agencies
-   Register and create a login
-   Create and monitor cases
-   Track the resolution of requests and all services received

</td></tr><tr><td>

Government service agency manager

</td><td>

Manager or leader of an agency​ that provides constituent and business services. Manages agents supporting constituent services:

-   Administers services delivered to constituents, business stakeholders, and agency.
-   Can read, write, update, and delete all government service cases.
-   Can read, write, update, and delete all constituent, business, and agency records.
-   Manages staff of agency and can override agent actions​.
-   Tracks the resolution of requests and improves service delivery and constituent satisfaction.

</td></tr></tbody>
</table>## Core Roles

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

constituent\_viewer\[sn\_gsm.constituent\_viewer\]

</td><td>

Provides agents with read-only access to constituent records.

</td><td>

sn\_customerservice.customer\_data\_viewer

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

agency\_contributor\[sn\_gsm.agency\_contributor\]

</td><td>

Enables agency agents to request services and raise government service cases on behalf of the agency.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_gsm.contributor\_creator
-   sn\_customerservice.case\_authorized\_contributor

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

relationship\_manager\[sn\_gsm.agency\_relationship\_manager\]

</td><td>

Enables users to view cases across all the external agencies where they have location\_relationship\_manager responsibility.

</td><td>

-   sn\_bus\_loc.location\_relationship\_manager
-   sn\_gsm.agency\_manager\_contributor

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

service\_offered\_admin\[sn\_gsm.service\_offered\_admin\]

</td><td>

 

</td><td>

None

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

</td></tr></tbody>
</table>## Roles by Application

<table id="icm-Roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

icm.investigator\[sn\_gsm\_icm.investigator\]

</td><td>

Provides users the ability to create and work on the investigative cases. It includes read access to all the cases and write access to the cases which are assigned to the investigator.

</td><td>

-   sn\_gsm\_icm.case\_writer
-   sn\_gsm\_icm.case\_viewer
-   sn\_gsm\_icm.entity\_viewer
-   sn\_gsm\_icm.entity\_writer
-   sn\_gsm\_icm.report\_viewer
-   sn\_gsm.government\_service\_manager
-   sn\_gsm\_icm.investigative\_contributor

</td></tr><tr><td>

supervisory\_agent\[sn\_gsm\_icm.supervisory\_agent\]

</td><td>

Provides users the ability to create and work on investigative cases. It includes read access to all the cases and write access to the cases belonging to the user's assignment group.

</td><td>

-   sn\_gsm\_icm.investigator
-   sn\_gsm\_icm.case\_admin

</td></tr><tr><td>

special\_agent\[sn\_gsm\_icm.special\_agent\]

</td><td>

Provides users the ability to create and fulfill all cases.

</td><td>

-   sn\_gsm\_icm.investigator
-   sn\_gsm\_icm.case\_admin

</td></tr><tr><td>

expert\_analyst\[sn\_gsm\_icm.expert\_analyst\]

</td><td>

Provides read or write access to the cases where these users are team members of the case or assigned to a case task of the case.

</td><td>

-   sn\_gsm\_icm.case\_viewer
-   sn\_gsm\_icm.case\_writer
-   sn\_gsm\_icm.event\_viewer
-   sn\_gsm\_icm.entity\_writer
-   sn\_gsm\_icm.event\_viewer

</td></tr><tr><td>

investigative\_contributor\[sn\_gsm\_icm.investigative\_contributor\]

</td><td>

Provides read or write access to the cases where these users are team members of the case or assigned to a case task of the case.

</td><td>

-   sn\_gsm\_icm.case\_viewer
-   sn\_gsm\_icm.case\_writer
-   sn\_gsm\_icm.event\_viewer
-   sn\_gsm\_icm.entity\_viewer

</td></tr><tr><td>

case\_viewersn\_gsm\_icm.case\_viewer

</td><td>

Provides users read only access to Investigative Case records.

</td><td>

sn\_gsm.case\_viewer

</td></tr><tr><td>

entity\_viewersn\_gsm\_icm.entity\_viewer

</td><td>

Provides read access to all the investigative case management entities such as Person, Organization, Property, Vehicle, or Evidence.

</td><td>

None

</td></tr><tr><td>

event\_viewersn\_gsm\_icm.event\_viewer

</td><td>

Provides read access to all the investigative case management events.

</td><td>

None

</td></tr><tr><td>

report\_viewersn\_gsm\_icm.report\_viewer

</td><td>

Provides users access to view reports containing Information Request data.

</td><td>

sn\_gsm.report\_viewer

</td></tr><tr><td>

case\_admin\[sn\_gsm\_icm.case\_admin\]

</td><td>

Provides read and write access to all the investigative cases.

</td><td>

-   sn\_gsm\_icm.case\_writer

-   sn\_gsm\_icm.case\_viewer
-   sn\_gsm\_icm.event\_writer
-   sn\_gsm\_icm.entity\_writer
-   sn\_gsm\_icm.report\_viewer

</td></tr><tr><td>

icm.admin\[sn\_gsm\_icm.admin\]

</td><td>

Provides delegated admin access to the investigative case management application.

</td><td>

-   sn\_gsm\_icm.supervisory\_agent

-   sn\_gsm\_icm.special\_agent


</td></tr><tr><td>

case\_task\_agent\[sn\_gsm\_icm.case\_task\_agent\]

</td><td>

Provides read access for administrative purposes to cases where users are assigned to a case task of the case.

</td><td>

sn\_gsm.case\_task\_agent

</td></tr><tr><td>

case\_writersn\_gsm\_icm.case\_writer

</td><td>

Provides users write only access to investigative case records that are assigned to the users or where the users are team members or where the case task of the case is assigned to the user.

</td><td>

-   sn\_gsm.case\_writer
-   sn\_gsm\_icm.case\_viewer

</td></tr><tr><td>

entity\_writersn\_gsm\_icm.entity\_writer

</td><td>

Provides write access to all the investigative case management entities like Person, Organization, Property, Vehicle or Evidence.

</td><td>

sn\_gsm\_icm.entity\_viewer

</td></tr><tr><td>

event\_writersn\_gsm\_icm.event\_writer

</td><td>

Provides write access to all the events which the user has access to.

</td><td>

sn\_gsm\_icm.event\_viewer

</td></tr></tbody>
</table><table id="gm-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

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

external\_reviewer\[sn\_gsm\_grnt\_mgmt.external\_reviewer\]

</td><td>

Enables merit review users to review and score grant proposals from within the Reviewer Service Portal.

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

grant\_management\_report\_viewersn\_gsm\_grnt\_mgmt.report\_viewer

</td><td>

Enables users to view reports about the grants management playbooks.

</td><td>

None

</td></tr></tbody>
</table><table id="lp-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

License &amp; Permits Install base writer\[sn\_gsm\_lic\_prmt.ib\_writer\]

</td><td>

Provides create, read, and write access to Install base items.

</td><td>

sn\_gsm\_lic\_prmt.ib\_writer

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

License &amp; Permit Constituent contributor\[sn\_gsm\_lic\_prmt.constituent\_contributor\]

</td><td>

This role enables users to request for service and raise License &amp; Permit cases on behalf of any constituent. This allow business stakeholders to act as a requestor on of behalf of customers.

</td><td>

-   sn\_gsm.constituent\_contributor
-   sn\_gsm\_lic\_prmt.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor


</td></tr><tr><td>

License &amp; Permit Business Contributor\[sn\_gsm\_lic\_prmt.business\_contributor\]

</td><td>

This role enables users to request for service and raise License &amp; Permit cases on behalf of any business. This allow business stakeholders to act as a requester on of behalf of customers.

</td><td>

-   sn\_gsm.business\_contributor
-   sn\_gsm\_lic\_prmt.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor


</td></tr><tr><td>

License &amp; Permit Relationship Contributor\[sn\_gsm\_lic\_prmt.relationship\_contributor\]

</td><td>

Enables users to raise License &amp; Permit cases on behalf of customers with whom they have relationships. This allows business stakeholder access to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.relationship\_contributors
-   n\_gsm\_lic\_prmt.contributor\_creator

</td></tr><tr><td>

License &amp; Permit Contributor Editor\[sn\_gsm\_lic\_prmt.contributor\_editor\]

</td><td>

Grants restrictive write access to the fields on the License and Permit Case form.

</td><td>

-   sn\_gsm.contributor\_creator
-   sn\_gsm\_lic\_prmt.case\_task\_agent


</td></tr><tr><td>

License &amp; Permit Agency Contributor\[sn\_gsm\_lic\_prmt.agency\_contributor\]

</td><td>

Enables users to request service and raise License &amp; Permit cases for their service organization \(business location\). This role is agnostic to internal and external.

</td><td>

-   sn\_gsm.agency\_contributor
-   sn\_gsm\_lic\_prmt.contributor\_creator
-   sn\_gsm\_lic\_prmt.agency\_manager\_contributor


</td></tr></tbody>
</table><table id="sb-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Social Benefits Constituent Contributor\[sn\_gsm\_soc\_bnfts.constituent\_contributor\]

</td><td>

This role enables users to request service and raise Social Benefits cases on behalf of any constituent. This allows business stakeholders to act as a requestor on behalf of customers.

</td><td>

-   sn\_gsm.constituent\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td></tr><tr><td>

Social Benefits Contributor Creator\[sn\_gsm\_soc\_bnfts.contributor\_creator\]

</td><td>

Enables users to create Social Benefits cases and is included in the top-level contributor roles. It only allows record creation but does not allow visibility to a record on its own.

</td><td>

-   sn\_gsm.constituent\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td></tr><tr><td>

Social Benefits Contributor Editor\[sn\_gsm\_soc\_bnfts.contributor\_editor\]

</td><td>

Grants restrictive write access to the fields on the Social Benefits Case form.

</td><td>

sn\_gsm.contributor\_creator

</td></tr><tr><td>

Social Benefits Relationship Contributor\[sn\_gsm\_soc\_bnfts.relationship\_contributor\]

</td><td>

Enables users to raise Social Benefits cases on behalf of customers with whom they have relationships. This allows business stakeholder access to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.relationship\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

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
</table><table id="ir-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Adminsn\_gsm\_info\_req.admin

</td><td>

Provides delegated admin access to scoped applications created on the Information Request Playbook platform.

</td><td>

-   sn\_gsm\_info\_req.manager
-   sn\_gsm.admin

</td></tr><tr><td>

Agency Agentsn\_gsm\_info\_req.agency\_agent

</td><td>

Provides users the ability to create and fulfill cases for the accounts and contacts in the agent's agency.

</td><td>

sn\_gsm.agency\_agent

</td></tr><tr><td>

Agency Constituent Agentsn\_gsm\_info\_req.agency\_constituent\_agent

</td><td>

Provides users the ability to create and fulfill cases for the constituents and households in the agent's agency.

</td><td>

sn\_gsm.agency\_constituent\_agent

</td></tr><tr><td>

Agency Contributorsn\_gsm\_info\_req.agency\_contributor

</td><td>

Enables users to request service and raise Information Request cases for their service organization \(business location\).

</td><td>

-   sn\_gsm\_info\_req.contributor\_creator
-   sn\_gsm.government\_agency\_contributor

</td></tr><tr><td>

Agency Managersn\_gsm\_info\_req.agency\_manager

</td><td>

Provides users the ability to manage data for agencies in the manager's agency hierarchy.

</td><td>

-   sn\_gsm\_info\_req.agency\_constituent\_agent
-   sn\_gsm.agency\_manager
-   sn\_gsm\_info\_req.agency\_agent

</td></tr><tr><td>

Business Agentsn\_gsm\_info\_req.business\_agent

</td><td>

Provides users the ability to work on Information Request cases for business. It includes the ability to read, write, and update all Information Request cases and business records.

</td><td>

-   sn\_gsm.business\_agent
-   sn\_gsm\_info\_req.case\_writer
-   sn\_gsm\_info\_req.report\_viewer

</td></tr><tr><td>

Business Contributorsn\_gsm\_info\_req.business\_contributor

</td><td>

Enables users to request for service and raise Information Request cases on behalf of any business. This allow business stakeholders to act as a requester on of behalf of customers.

</td><td>

-   sn\_gsm\_info\_req.contributor\_creator
-   sn\_gsm.business\_contributor

</td></tr><tr><td>

Case Task Agentsn\_gsm\_info\_req.case\_task\_agent

</td><td>

Enables users to work on Information Request case tasks.

</td><td>

-   sn\_gsm\_info\_req.case\_viewer
-   sn\_gsm.case\_task\_agent
-   sn\_gsm\_info\_req.contributor\_editor

</td></tr><tr><td>

Case Viewersn\_gsm\_info\_req.case\_viewer

</td><td>

Provides users read only access to Information Request Case records.

</td><td>

sn\_gsm.case\_viewer

</td></tr><tr><td>

Case Writersn\_gsm\_info\_req.case\_writer

</td><td>

Provides users access to create read and update Information Request Case records.

</td><td>

-   sn\_gsm.case\_writer
-   sn\_gsm\_info\_req.case\_viewer

</td></tr><tr><td>

Constituent Agentsn\_gsm\_info\_req.constituent\_agent

</td><td>

Provides users the ability to work on Information Request cases for all constituents. It includes the ability to read, write, and update all Information Request cases and constituent records.

</td><td>

-   sn\_gsm\_info\_req.case\_writer
-   sn\_gsm\_info\_req.report\_viewer
-   sn\_gsm.constituent\_agent

</td></tr><tr><td>

Constituent Contributorsn\_gsm\_info\_req.constituent\_contributor

</td><td>

Enables users to request for service and raise Information Request cases on behalf of any constituent. This allows business stakeholders to act as a requestor on behalf of customers.

</td><td>

-   sn\_gsm\_info\_req.contributor\_creator
-   sn\_gsm.constituent\_contributor

</td></tr><tr><td>

Contributor Creatorsn\_gsm\_info\_req.contributor\_creator

</td><td>

Enables users to create Information Request cases and is included in the top-level contributor roles. It only allows record creation but does not allow visibility to a record on its own.

</td><td>

sn\_gsm.contributor\_creator

</td></tr><tr><td>

Contributor Editorsn\_gsm\_info\_req.contributor\_editor

</td><td>

Grants restrictive write access to the fields on the Information Request Case form.

</td><td>

sn\_gsm.contributor\_editor

</td></tr><tr><td>

Request Managersn\_gsm\_info\_req.manager

</td><td>

Provides users the ability to manage all work performed by agents working on Information Request cases \(constituent and business\). Users with this role have the ability to read, write, update, and delete all Information Request service cases and constituent or business records.

</td><td>

-   sn\_majorissue\_mgt.major\_issue\_manager
-   sn\_gsm\_info\_req.business\_agent
-   sn\_gsm.government\_service\_manager
-   sn\_gsm\_info\_req.constituent\_agent

</td></tr><tr><td>

Relationship Agentsn\_gsm\_info\_req.relationship\_agent

</td><td>

Enables users to work on Information Request cases only for customers with whom they have relationships.

</td><td>

-   sn\_gsm.relationship\_agent
-   sn\_gsm\_info\_req.report\_viewer

</td></tr><tr><td>

Relationship Contributorsn\_gsm\_info\_req.relationship\_contributor

</td><td>

Enables users to raise Information Request cases on behalf of customers with whom they have relationships. This allows business stakeholder access to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.relationship\_contributor
-   sn\_gsm\_info\_req.contributor\_creator

</td></tr><tr><td>

Report Viewersn\_gsm\_info\_req.report\_viewer

</td><td>

Provides users access to view reports containing Information Request data.

</td><td>

sn\_gsm.report\_viewer

</td></tr></tbody>
</table><table id="SApM-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Program Admin \(sn\_svc\_appl\_pgm\_mg.admin\)

</td><td>

Provides delegated admin access to scoped applications created on the Service Applicant Program Management platform

</td><td>

None

</td></tr><tr><td>

Grant Program Admin \(sn\_svc\_appl\_pgm\_mg.grant\_program\_admin\)

</td><td>

Provides access to all Grant Programs.

</td><td>

sn\_svc\_appl\_pgm\_mg.grant\_program\_writer

</td></tr><tr><td>

Grant Program Director \(sn\_svc\_appl\_pgm\_mg.grant\_program\_director\)

</td><td>

Provides access to all Grant Programs.

</td><td>

-   sn\_gsm.government\_service\_manager
-   sn\_svc\_appl\_pgm\_mg.grant\_program\_manager

</td></tr><tr><td>

Grant Program Writer \(sn\_svc\_appl\_pgm\_mg.grant\_program\_manager\)

</td><td>

Creates or updates Grant Programs if they are a part of.

</td><td>

-   sn\_gsm.business\_agent
-   sn\_svc\_appl\_pgm\_mg.grant\_program\_writer
-   sn\_smart\_asmt.assessment\_admin
-   sn\_svc\_appl\_pgm\_mg.planning\_item\_writer
-   sn\_svc\_appl\_pgm\_mg.resource\_mapping\_writer
-   sn\_svc\_appl\_pgm\_mg.scoring\_framework\_writer
-   sn\_svc\_appl\_pgm\_mg.resource\_assignment\_writer
-   sn\_svc\_appl\_pgm\_mg.milestone\_writer
-   sn\_svc\_appl\_pgm\_mg.resource\_role\_writer
-   sn\_gsm.goal\_viewer
-   sn\_svc\_appl\_pgm\_mg.business\_calendar\_entry\_viewer
-   sn\_svc\_appl\_pgm\_mg.pace\_reader
-   sn\_pace.mapping\_admin
-   sn\_svc\_appl\_pgm\_mg.scoring\_framework\_attribute\_writer

</td></tr><tr><td>

Grant Program Viewer \(sn\_svc\_appl\_pgm\_mg.grant\_program\_writer\)

</td><td>

Provides write access to Grant Program records.

</td><td>

-   sn\_svc\_appl\_pgm\_mg.grant\_program\_viewer
-   sn\_svc\_appl\_pgm\_mg.planning\_item\_writer

</td></tr><tr><td>

Planning Item Writer \(sn\_svc\_appl\_pgm\_mg.grant\_program\_viewer\)

</td><td>

Provides read access to Grant Program records.

</td><td>

sn\_svc\_appl\_pgm\_mg.planning\_item\_viewer

</td></tr><tr><td>

Planning Item Viewer \(sn\_svc\_appl\_pgm\_mg.planning\_item\_writer\)

</td><td>

Provides write access to Planning Item records.

</td><td>

sn\_svc\_appl\_pgm\_mg.planning\_item\_viewer

</td></tr><tr><td>

Budget Allocation Writer \(sn\_svc\_appl\_pgm\_mg.planning\_item\_viewer\)

</td><td>

Provides read access to Planning Item records.

</td><td>

None

</td></tr><tr><td>

\(sn\_svc\_appl\_pgm\_mg.budget\_allocation\_writer\)

</td><td>

Provides write access to Budget Allocation records.

</td><td>

sn\_svc\_appl\_pgm\_mg.budget\_allocation\_viewer

</td></tr><tr><td>

\(sn\_svc\_appl\_pgm\_mg.budget\_allocation\_viewer\)

</td><td>

Provides read access to Budget Allocation records.

</td><td>

None

</td></tr><tr><td>

\(sn\_svc\_appl\_pgm\_mg.milestone\_writer\)

</td><td>

Provides write access to Milestone records.

</td><td>

sn\_svc\_appl\_pgm\_mg.milestone\_viewer

</td></tr><tr><td>

\(sn\_svc\_appl\_pgm\_mg.milestone\_viewer\)

</td><td>

Provides read access to Milestone records.

</td><td>

None

</td></tr><tr><td>

Resource Assignment Writer \(sn\_svc\_appl\_pgm\_mg.resource\_assignment\_writer\)

</td><td>

Provides write access to Resource Assignment records.

</td><td>

sn\_svc\_appl\_pgm\_mg.resource\_assignment\_viewer

</td></tr><tr><td>

Resource Assignment Viewer \(sn\_svc\_appl\_pgm\_mg.resource\_assignment\_viewer\)

</td><td>

Provides read access to Resource Assignment records.

</td><td>

None

</td></tr><tr><td>

Informational Resource Mapping Writer \(sn\_svc\_appl\_pgm\_mg.resource\_mapping\_writer\)

</td><td>

Provides write access to Informational Resource Mapping records.

</td><td>

sn\_svc\_appl\_pgm\_mg.resource\_mapping\_viewer

</td></tr><tr><td>

Informational Resource Mapping Viewer \(sn\_svc\_appl\_pgm\_mg.resource\_mapping\_viewer\)

</td><td>

Provides read access to Informational Resource Mapping records.

</td><td>

None

</td></tr><tr><td>

Resource Role Writer \(sn\_svc\_appl\_pgm\_mg.resource\_role\_writer\)

</td><td>

Provides write access to Resource Role records.

</td><td>

sn\_svc\_appl\_pgm\_mg.resource\_role\_viewer

</td></tr><tr><td>

Resource Role Viewer \(sn\_svc\_appl\_pgm\_mg.resource\_role\_viewer\)

</td><td>

Provides read access to Resource Role records.

</td><td>

None

</td></tr><tr><td>

Scoring Framework Writer \(sn\_svc\_appl\_pgm\_mg.scoring\_framework\_writer\)

</td><td>

Provides write access to Scoring Framework records.

</td><td>

sn\_svc\_appl\_pgm\_mg.scoring\_framework\_viewer

</td></tr><tr><td>

Scoring Framework Viewer \(sn\_svc\_appl\_pgm\_mg.scoring\_framework\_viewer\)

</td><td>

Provides read access to Scoring Framework records.

</td><td>

None

</td></tr><tr><td>

Scoring Framework Attribute Writer \(sn\_svc\_appl\_pgm\_mg.scoring\_framework\_attribute\_writer\)

</td><td>

Provides write access to Scoring Framework Attributes records.

</td><td>

sn\_svc\_appl\_pgm\_mg.scoring\_framework\_attribute\_viewer

</td></tr><tr><td>

Scoring Framework Attribute Viewer \(sn\_svc\_appl\_pgm\_mg.scoring\_framework\_attribute\_viewer\)

</td><td>

Provides read access to Scoring Framework Attributes records.

</td><td>

None

</td></tr><tr><td>

Business Calendar Entry Viewer \(sn\_svc\_appl\_pgm\_mg.business\_calendar\_entry\_viewer\)

</td><td>

Provides read access to Business Calendar Entry and Business Calendar Entry Name tables.

</td><td>

None

</td></tr><tr><td>

Pace Reader \(sn\_svc\_appl\_pgm\_mg.pace\_reader\)

</td><td>

Provides read access to PaCE records.

</td><td>

None

</td></tr><tr><td>

Report Viewer \(sn\_svc\_appl\_pgm\_mg.report\_viewer\)

</td><td>

Provides users the access to view reports of Program records.

</td><td>

None

</td></tr></tbody>
</table>## Roles by Plugin

<table id="SAp-roles"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

\(sn\_svc\_appl\_info.admin\)

</td><td>

Provides delegated admin access to scoped applications created on the Service Application Information.

</td><td>

-   sn\_svc\_appl\_info.point\_in\_time\_content\_admin
-   sn\_svc\_appl\_info.applicant\_admin
-   sn\_svc\_appl\_info.financial\_details\_admin

</td></tr><tr><td>

\(sn\_svc\_appl\_info.applicant\_admin\)

</td><td>

Provides create,read,write and delete access to applicant records.

</td><td>

sn\_svc\_appl\_info.applicant\_writer

</td></tr><tr><td>

\(sn\_svc\_appl\_info.applicant\_viewer\)

</td><td>

Provides read access to applicant records.

</td><td>

 

</td></tr><tr><td>

\(sn\_svc\_appl\_info.applicant\_writer\)

</td><td>

Provides create,read and write access to applicant records.

</td><td>

sn\_svc\_appl\_info.applicant\_viewer

</td></tr><tr><td>

\(sn\_svc\_appl\_info.financial\_details\_admin\)

</td><td>

Provides create,read,write and delete access to financial details records.

</td><td>

sn\_svc\_appl\_info.financial\_details\_writer

</td></tr><tr><td>

\(sn\_svc\_appl\_info.financial\_details\_viewer\)

</td><td>

Provides read access to financial details records.

</td><td>

None

</td></tr><tr><td>

\(sn\_svc\_appl\_info.financial\_details\_writer\)

</td><td>

Provides create,read and write access to financial details records.

</td><td>

sn\_svc\_appl\_info.financial\_details\_viewer

</td></tr><tr><td>

\(sn\_svc\_appl\_info.point\_in\_time\_content\_admin\)

</td><td>

Provides create,read, write and delete access to point-in-time content records.

</td><td>

sn\_svc\_appl\_info.point\_in\_time\_content\_writer

</td></tr><tr><td>

\(sn\_svc\_appl\_info.point\_in\_time\_content\_viewer\)

</td><td>

Provides read access to point-in-time content records.

</td><td>

None

</td></tr><tr><td>

\(sn\_svc\_appl\_info.point\_in\_time\_content\_writer\)

</td><td>

Provides create,read and write access to point-in-time content records.

</td><td>

sn\_svc\_appl\_info.point\_in\_time\_content\_viewer

</td></tr><tr><td>

\(sn\_svc\_appl\_info.report\_viewer\)

</td><td>

Provides users the access to view reports on the Service Applicant Information platform.

</td><td>

None

</td></tr></tbody>
</table>|Role|Description|Persona|
|----|-----------|-------|
|sn\_pace.execution\_reader|A read-only user with view-only access. This user can view policies, categories, and executions.|Policy user, internal auditor.|
|sn\_pace.code\_reader|Can review PaCE versions, policy code, and run tests.|Internal auditor|
|sn\_pace.code\_editor|This user has all the sn\_pace\_code\_reader permissions plus the ability to create PaCE policy versions.|Policy developer|
|sn\_pace.policy\_reader|This user has all the sn\_pace\_code\_reader permissions plus the ability to review policy details and mapping information.|Policy user, internal auditor|
|sn\_pace.policy\_editor|This user has all the sn\_pace\_policy\_reader and sn\_pace.code\_editor permissions plus the ability to create policies and mappings.|Policy developer|
|sn\_pace.mapping\_admin|This user can map policies and edit config parameters for policy mappings.|Mapping admin|
|sn\_pace.admin|This user has the permissions of all the other roles plus the ability to create categories, policies, mappings, and code.|Policy admin|
|sn\_pace.super\_admin|This user has all the sn\_pace.admin role permissions across all calling services.|Not applicable|
|Maint role|Internal user who can create default content.|Not applicable|

## Granular roles

You can use predefined functional and granular roles installed with Public Sector Digital Services to establish relationships between users and public sector entities. These functional and granular roles provide different levels of access to public sector data.

-   Functional roles: A set of roles required to perform a function or meaningful action that requires access on multiple entities.
-   Granular roles: Roles that provide access to cases, services used, and related public sector entities. One or more granular roles can be bundled together as a functional role.

A granular model controls access to data through UI-based interactions by granting the appropriate level of access to the corresponding public sector entities. With this functionality, each role is associated with a set of privileges or responsibilities that determine users' access to information via forms, lists, and application features. You can have fine-grained access control by setting granular policies that authorize individuals to access the information needed to work efficiently and effectively, ultimately helping improve the constituent experience.

**Note:** Role-based access controls govern UI interactions. They do not restrict access by users with system-level scripting privileges or elevated platform roles. These roles control access to public sector data through UI-based features such as forms and lists.

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

case\_admin\[sn\_gsm\_icm.case\_admin\]

</td><td>

Provides read and write access to all the investigative cases.

</td><td>

-   sn\_gsm\_icm.case\_writer

-   sn\_gsm\_icm.case\_viewer
-   sn\_gsm\_icm.event\_writer
-   sn\_gsm\_icm.entity\_writer
-   sn\_gsm\_icm.report\_viewer

</td></tr></tbody>
</table>## Business Stakeholder Roles

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

</td></tr><tr><td>

Social Benefits Business Contributor\[sn\_gsm\_soc\_bnfts.business\_contributor\]

</td><td>

Enables users to request service and raise Social Benefits cases on behalf of any business. This allows business stakeholders to act as a requester on behalf of customers.

</td><td>

-   sn\_gsm.business\_contributor
-   sn\_gsm\_soc\_bnfts.contributor\_creator

</td><td>

 

</td><td>

 

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

None

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

None

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

sn\_gsm.report\_viewer

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

</td></tr><tr><td>

\(sn\_svc\_appl\_info.report\_viewer\)

</td><td>

Provides users the access to view reports on the Service Applicant Information platform.

</td><td>

None

</td></tr></tbody>
</table>**Note:** Customers who have purchased a Public Sector Digital Services subscription can provide Business Stakeholder users with rights to actions listed under [Business Stakeholder for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/business-stakeholder-for-csm.md).

**Parent Topic:**[Components and Roles installed with Public Sector Digital Services Core](installed-with-public-sector-digital-services-core.md)

