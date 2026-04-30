---
title: Components installed with Software Bill of Materials applications
description: Several types of components are installed with activation of the Software Bill of Materials applications, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Components installed with Software Bill of Materials applications

Several types of components are installed with activation of the Software Bill of Materials applications, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_djn_vnw_zyb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_sbom\_response.managelicense

</td><td>

This role is installed with the SBOM Response application.

 This role permits you to resolve licenses to components.

</td><td>

None

</td></tr><tr><td>

sn\_sbom\_response.licenseresolver

</td><td>

This role is installed with the SBOM Response application.

 This role permits you to view uploaded license information and determines which licenses are permitted and which are banned.

</td><td>

None

</td></tr><tr><td>

SBOM write \[sn\_sbom\_dm.app\_write\], SBOM create \[sn\_sbom\_dm.app\_create\], SBOM read \[sbom\_dm.app\_read\]

</td><td>

These roles are installed with the Data Model for SBOM application.

 They permit you to read, create, and edit records in SBOM tables.

</td><td>

None

</td></tr><tr><td>

SBOM Cores ingests \[sn\_sbom\_core.sbom\_ingest\] and SBOM Core admin \[ sn\_sbom\_core.admin\]

</td><td>

These roles are installed with the SBOM Core application.

 The sn\_sbom\_core.sbom\_ingest role permits you to upload SBOMs manually and via the REST API. The sn\_sbom\_core.admin role permits you to create, read, edit data, and upload SBOMs.

 This role also gives you access to the SBOM Core modules in your instance. It inherits the roles from the Data Model for SBOM application.

</td><td>

-   sn\_sbom\_dm.app\_write
-   sn\_sbom\_dm.app\_create
-   sn\_ sbom\_dm.app\_read

</td></tr><tr><td>

SBOM Analyst

 \[sn\_sbom\_resp.sbom\_analyst\]

</td><td>

This role is installed with the SBOM Response application.

 It inherits the sn\_sbom\_core.admin role and enables you to access the SBOM Workspace.

</td><td>

-   sn\_sbom\_core.admin
-   sn\_sbom\_dm.app\_write
-   sn\_sbom\_dm.app\_create
-   sn\_ sbom\_dm.app\_read
-   sn\_sbom\_resp.manage\_avi\_rule
-   sn\_sbom\_config\_rule table

</td></tr></tbody>
</table>## Tables installed with the SBOM applications

The tables listed in the following table are installed with the Data model for SBOM application.

<table id="table_hjn_vnw_zyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SBOM document

 \[sn\_sbom\_doc\]

</td><td>

Contains the BOM entities you've uploaded.

</td></tr><tr><td>

SBOM component

 \[sn\_sbom\_component\]

</td><td>

Contains imported SBOM components, classifiers, and versions that are included in the parent component.

</td></tr><tr><td>

SBOM component relationship

 \[sn\_sbom\_comp\_relationship\]

</td><td>

Contains components and their dependencies.

</td></tr><tr><td>

SBOM m2m bom component

 \[sn\_sbom\_m2m\_bom\_comp\]

</td><td>

Contains the BOM component mappings.

</td></tr><tr><td>

SBOM license

 \[sn\_sbom\_license\]

</td><td>

Contains the open-source license IDs used for components.

</td></tr><tr><td>

SBOM supplier

 \[sn\_sbom\_supplier\]

</td><td>

Contains the organization that supplied the component, which might be a manufacturer, distributor, or repackager.

</td></tr><tr><td>

SBOM component ID

 \[sn\_sbom\_comp\_id\]

</td><td>

Contains the component identifiers.

</td></tr><tr><td>

SBOM component properties

 \[sn\_sbom\_comp\_property\]

</td><td>

Contains the component name-value properties.

</td></tr><tr><td>

SBOM hash

 \[sn\_sbom\_hash\]

</td><td>

Contains component hashing algorithms.

</td></tr><tr><td>

SBOM contact

 \[sn\_sbom\_contact\]

</td><td>

Contains contact information for the supplier.

</td></tr><tr><td>

SBOM external references

 \[sn\_sbom\_comp\_external\_ref\]

</td><td>

Contains components, component types, and external URLs that document systems, sites, and information that might be relevant but are not included with the SBOM.

</td></tr><tr><td>

SBOM package group

 \[sn\_sbom\_pkg\_group\]

</td><td>

Contains the package group information for every component. Multiple version of libraries may be used across applications. Versions of the same components are grouped and added to this table to avoid pulling the same data multiple times.

</td></tr></tbody>
</table>The tables listred in the following table are installed with the SBOM Response application

<table id="table_gcv_mqw_zyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SBOM creation rule configuration

 \[sn\_sbom\_config\_rule\]

</td><td>

Contains AVIT creation rules used in the SBOM Workspace.

</td></tr><tr><td>

SBOM m2m component vulnerabilities

 \[sn\_sbom\_m2m\_comp\_vuln\]

</td><td>

Contains the components and associated vulnerabilities.

</td></tr><tr><td>

Component vulnerability fix information\[sn\_sbom\_comp\_vuln\_fix\_info\]

</td><td>

Contains the fix versions for each third-party vulnerability associated to a version of the component.

</td></tr><tr><td>

Component report insights\[sn\_sbom\_comp\_report\_insight\]

</td><td>

Contains insights about stale, abandoned, and fixability data for components.

</td></tr><tr><td>

Deps Integration Imports\[sn\_sbom\_deps\_integration\_import\]

</td><td>

Contains imported version list information for a given package or library.

</td></tr><tr><td>

OSV Integration Imports\[sn\_sbom\_osv\_integration\_import\]

</td><td>

Contains vulnerability intelligence information for a given version of a package or library.

</td></tr><tr><td>

Component Version Lists\[sn\_sbom\_st\_version\_list\]

</td><td>

Contains version information and published dates for components.

</td></tr></tbody>
</table>## Scheduled jobs

|Job|Description|
|---|-----------|
|Calculate Component Fixability and Vulnerability|Calculates information about how to fix components with vulnerabilities and how likely it is that you can fix components.|
|OSV Integration New Components|Retrieves all publicly known vulnerabilities associated with packages \(libraries\) that were imported after the last integration run.|
|OSV Integration Comprehensive|Retrieves all publicly known vulnerabilities associated with all packages that have been imported.|
|Deps.dev Integration|Retrieves all publicly known versions for packages and used with to identify components in **Stale** and **Abandoned** states.|
|Update vuln\_based\_criticality on bom components|Updates criticality for components with vulnerabilities.|

