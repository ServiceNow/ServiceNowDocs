---
title: Configuring Software Bill of Materials
description: Download and activate the required applications for the Software Bill of Materials \(SBOM\) application prior to uploading SBOM files.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2025-02-26"
reading_time_minutes: 2
breadcrumb: [Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Configuring Software Bill of Materials

Download and activate the required applications for the Software Bill of Materials \(SBOM\) application prior to uploading SBOM files.

## Configuration overview

1.  Download the required SBOM applications and any additional supported applications and integrations you want from the ServiceNow Store into your ServiceNow instance. See [Exploring Software Bill of Materials](vr-sbom-exploring.md) and [Download an application from the ServiceNow Store for the first time](../../../security-incident-response/reference/download-app-first-time.md) for more information about supported applications.

    The Vulnerability Response application is required for SBOM Response. Install The Vulnerability Response application prior to installing SBOM Response.

2.  Locate the SBOM applications that you downloaded and select Install to activate them along with their dependencies in the following order. See [Install the supported applications for Software Bill of Materials](../task/vr-sbom-install-apps.md).
    -   Vulnerability Response and its dependencies
    -   Vulnerability Response Integration with NVD
    -   Data Model for SBOM
    -   SBOM Core
    -   SBOM Response, which includes the OSV.dev and Deps.dev integrations and access to the capabilities of Policy as Code Engine \(PaCE\) in the SBOM Workspace.
3.  Configure the Deps.dev and OSV.dev integrations. These integrations are included with the SBOM Response application and are installed and activated automatically. You must initiate the OSV.dev Integration - Comprehensive on-demand from its integration record. See [Configuring the Deps.dev, OSV.dev, and PaCE integrations for Software Bill of Materials](vr-sbom-config-osv-deps.md) and [Exploring Software Bill of Materials](vr-sbom-exploring.md) for more information.

    The Deps.dev Integration provides you with information about components that are in **Stale** and **Abandoned** states for a given version of a package or library that you upload in your SBOM files.

    OSV.dev pulls vulnerability data from an open source database for a version of a package or library you upload in your SBOM files.

4.  Refer to product documentation to configure any additional supported applications and integrations you installed. See [Vulnerability Response integrations](../../../vulnerability-response/concept/vuln_integrations.md) and [Integrating Application Vulnerability Response with other applications](../../../vulnerability-app-vuln-mgmt/concept/avm-integrations.md).

