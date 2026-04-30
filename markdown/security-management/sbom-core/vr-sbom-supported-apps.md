---
title: Exploring supported applications for Software Bill of Materials
description: Third-party vulnerability intelligence and other integrations with the Software Bill of Materials applications can enhance the data of your uploaded files.
locale: en-US
release: xanadu
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2024-10-25"
reading_time_minutes: 2
breadcrumb: [Exploring Software Bill of Materials, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Exploring supported applications for Software Bill of Materials

Third-party vulnerability intelligence and other integrations with the Software Bill of Materials applications can enhance the data of your uploaded files.

## Supported applications benefits

Third-party vulnerability intelligence and other integrations with the Software Bill of Materials applications permit you to view counts for components that are considered stale and abandoned, as well as information about if you can fix any vulnerabilities associated with components.

The ServiceNow® applications and third-party integrations listed in the following table are supported by the SBOM applications. These applications provide you with enriched vulnerability data, vulnerability intelligence, and other key information that can help you view and prioritize the vulnerabilities associated with SBOM files. All these applications and integrations are available from the ServiceNow® Store.

<table id="table_z15_lvh_scc"><thead><tr><th>

Benefit

</th><th>

Application

</th><th>

Supported versions

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Vulnerability Response is required if you install the SBOM Response application. Install The Vulnerability Response application prior to installing SBOM Response.

 Application Vulnerability Response features are installed with Vulnerability Response. These features enable access to the Vulnerability Manager Workspace in the Vulnerability Response application and the vulnerability workflow to help you remediate application vulnerable items \(AVIT\)s.

</td><td>

Vulnerability Response

</td><td>

For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498).

</td><td>

 

</td></tr><tr><td>

View enhanced NVD vulnerability and severity data. View imported data from the NVD and CWE integrations to enrich any vulnerability data you might find in your SBOM data.See [Importing data with the NVD and CWE integrations and managing third-party libraries](../../../vulnerability-response/concept/c_NVDAndCWEDataImport.md) for more information.

</td><td>

Vulnerability Response Integration with NVD and SBOM Response

</td><td>

For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498).

</td><td>

 

</td></tr><tr><td>

Import software bills of material files with the Veracode Vulnerability Integration. The Veracode Vulnerability Integration includes the following enhancements with Veracode SBOM files:-   If you have installed SBOM Response, you have the option to include vulnerabilities found by SBOM for the SBOM files you upload.
-   SBOM is mapped to the Source field for records in the Bill of Materials \[sn\_sbom\_doc\] table for the SBOM SBOM files that you upload.

See [Veracode Vulnerability Integration](../../veracode/concept/veracode-vuln-integration.md) for more information.

</td><td>

Veracode Vulnerability Integration and SBOM Response

</td><td>

Starting with version 4.3 of the Veracode Vulnerability Integration.

 If you have the Veracode Vulnerability Integration already installed, you can also upload imported Veracode SBOM data in CycloneDX \(JSON and XML\) and SPDX \(XML\) formats starting with version v3.0 of SBOM Core.

 For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498).

</td><td>

 

</td></tr><tr><td>

Upload SBOM files to the ServiceNow AI Platform from your GitHub repositories. Determine if SBOM files generated in your CI/CD \(continuous integration and continuous delivery/deployment\) pipelines have been successfully queued in your ServiceNow AI Platform instance.

 Protect your environments from potentially harmful components during software development cycles with GitHub Actions that you initiate from your GitHub environment.

</td><td>

Obtain any required GitHub Actions for SBOM upload in the GitHub Marketplace.

</td><td>

Starting with version 4.0 of SBOM Core.

</td><td>

 

</td></tr></tbody>
</table>