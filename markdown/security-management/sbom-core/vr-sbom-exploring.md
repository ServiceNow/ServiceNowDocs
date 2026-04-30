---
title: Exploring Software Bill of Materials
description: Identify the components used in your organization's applications from Software Bill of Materials \(SBOM\) files you upload into your instance. Understand any risks associated with using open-source software to help you determine your potential exposure, view license compliance, and fix vulnerabilities.
locale: en-US
release: xanadu
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2025-02-26"
reading_time_minutes: 6
breadcrumb: [Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Exploring Software Bill of Materials

Identify the components used in your organization's applications from Software Bill of Materials \(SBOM\) files you upload into your instance. Understand any risks associated with using open-source software to help you determine your potential exposure, view license compliance, and fix vulnerabilities.

## Software Bill of Materials overview

Third-party and open-source components provide you with many advantages for the rapid creation and release of your software projects. However, in some cases, there are risks associated with using publicly accessible components, such as the following:

-   Lack of visibility into component integrity
-   Vulnerabilities in the open-source software
-   Package Intelligence for open-source software
-   Non-compliant software licenses

You can upload your software bill of material files via an API or manually. View the files that you import as entities, which are inventories of the third-party component libraries used in your software, including any transitive dependencies and available licensing information.

For more information about what is included in the software inventories in CycloneDX and SPDX SBOMs, see [CycloneDX - Software Bill of Materials \(SBOM\)](https://cyclonedx.org/capabilities/sbom/) and [SPDX](https://spdx.dev/).

## Software Bill of Materials users

<table id="table_jmp_44h_scc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vulnerability managers and analysts

</td><td>

View uploaded software bill of materials files in records, data visualizations, as well as enhanced vulnerability intelligence in the Software Bill of Materials \(SBOM\) Workspace.Vulnerability managers and analysts use this information to help them determine your software licensing compliance and the potential risk exposure with using open-source software.

</td></tr><tr><td>

Users that might include but are not limited to:-   Technology or software lawyers
-   IT managers
-   Auditors
-   Software asset managers and teams

</td><td>

View uploaded proprietary and open-source software licenses for components of your uploaded SBOM files.Build a database of proprietary and open-source software licenses for the components.

Review and classify licenses with missing information according to your internal or regulatory policies.

Match your components to licenses and determine your overall license compliance and see your potential risk exposure to banned, restricted, or missing licenses.

</td></tr></tbody>
</table>## Software Bill of Materials workflow

The SBOM applications enable you to upload files and view details for entities, component inventories, vulnerabilities, and software license information in the Software Bill of Materials \(SBOM\) Workspace.

-   Upload SBOM files with an API or manually.
-   Review the components in the SBOM file you uploaded in the SBOM Workspace.
-   Review component license information from uploaded SBOM files and classify them to help you identify your exposure to restricted or banned licenses.
-   Assess your risk exposure and create vulnerable items for components that have associated vulnerabilities.
-   View reports and dashboards as well as your overall license compliance for uploaded SBOM components on the Home page in the SBOM Workspace.

## Software Bill of Materials benefits

Three Software Bill of Materials applications enable you to view an accurate inventory of your software components and associated risks:

-   Data Model for SBOM
-   SBOM Core
-   SBOM Response

For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498).

<table id="table_mmp_44h_scc"><thead><tr><th>

Benefit

</th><th>

Application

</th><th>

Supported versions

</th></tr></thead><tbody><tr><td>

This application provides the tables used to store SBOM data. This application is required. It includes the tables, ACLs, and roles that are required to read SBOM data.

</td><td>

Data Model for SBOM

</td><td>

v4.0, v3.0, v2.0

</td></tr><tr><td>

This application is required. It Includes the API required to upload SBOM documents and the business logic required to parse and import the data from those documents into your instance. You can view an inventory of your software components in the SBOM Workspace, but you cannot view the data visualizations on the landing page.Upload, parse, and process your software bill of materials files in CycloneDX and SPDX standards. Refer to the Supported versions column for the supported file formats and versions for these products. View bill of materials \(BOM\) entities and an inventory of your software components. A BOM entity is the root level component in an SBOM file. For example, for a CycloneDX SBOM, the component listed in the metadata is considered the BOM entity.

</td><td>

SBOM Core

</td><td>

v6.0, v5.0, v4.0

 Starting with version 4.0, SBOM Core supports:

 -   XML and JSON versions 1.0 through 1.6 of CycloneDX.
-   JSON versions 2.2 through 2.3 of SPDX.

</td></tr><tr><td>

-   SBOM Response is required if you want access to the features and data visualizations on the landing page in the SBOM Workspace.
-   SBOM Response requires the Vulnerability Response application.
-   View your component inventory and assess your risk exposure in the SBOM Workspace. Set up rules to create application vulnerable items \(AVITs\) automatically and remediate them with the Application Vulnerability Response workflow.
-   View component license information that is uploaded with your SBOM files in the [License administration module](vr-sbom-license-overview.md). Classify and resolve \(match\) the components you upload in your Application Vulnerability Response files to licenses so you can see the state of your over-all license compliance.
-   Starting with version 4.0 of Application Vulnerability Response Response, you can view components that are identified as stale or abandoned as ‘Non-compliant’ in the Policy as Code Engine \(PaCE\) interface that is available in the SBOM Workspace.
-   The OSV.dev and Deps.dev integrations are included when you install SBOM Response.

    -   OSV.dev is an open-source API that provides vulnerability intelligence information for a given version of a package or library.
    -   Deps.dev is an open-source API that provides a version list for a given package or library and identifies components that are in **Stale** and **Abandoned** states.
See [Configuring the Deps.dev, OSV.dev, and PaCE integrations for Software Bill of Materials](vr-sbom-config-osv-deps.md) for more information.

See [Integrating PaCE with other applications](https://www.servicenow.com/docs/access?context=pace-integrate-other-apps&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information about PaCE and PaCE policies.


</td><td>

SBOM Response

</td><td>

v6.0, v5.0, v4.0

</td></tr><tr><td>

Generate and upload Software Bill of Materials \(SBOM\) files for software throughout its continuous integration and continuous deployment development cycles.

</td><td>

SBOM Response

</td><td>

-   Data Model for SBOM: v1.4 and later.
-   SBOM Core: v3.0 and later.
-   SBOM Response: v4.0 and later.

</td></tr></tbody>
</table>## Vulnerability Response applications and CSDM tables

The Vulnerability Response, Application Vulnerability Response, third-party vulnerability integrations and Software Bill of Materials applications manage \(contribute data to\) CSDM tables. These applications also use data from CSDM tables that other applications generate. Several ServiceNow products, therefore, benefit from and add value to these Security Operations applications. See [Vulnerability Response applications and CSDM tables](../../../vulnerability-response/concept/vr-avr-sbom-csdm-guidelines.md) for more information.

## What to explore next

To learn more about configuring and using Software Bill of Materials, see:

-   [Exploring supported applications for Software Bill of Materials](vr-sbom-supported-apps.md)
-   [Configuring Software Bill of Materials](vr-sbom-configuring.md)
-   [Uploading and viewing your SBOM files in the SBOM Workspace](vr-sbom-using-parent.md)
-   [Viewing reports and dashboards in the Software Bill of Materials workspace](vr-sbom-viewing-data-overview.md)

