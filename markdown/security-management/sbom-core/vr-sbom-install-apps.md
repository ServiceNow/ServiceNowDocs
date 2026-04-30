---
title: Install the supported applications for Software Bill of Materials
description: Download and activate the required applications for the Software Bill of Materials \(SBOM\) application prior to uploading files.
locale: en-US
release: xanadu
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2025-01-14"
reading_time_minutes: 5
breadcrumb: [Configuring Software Bill of Materials, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Install the supported applications for Software Bill of Materials

Download and activate the required applications for the Software Bill of Materials \(SBOM\) application prior to uploading files.

## Before you begin

Roles required: admin for download, installation, and activation of all applications and role assignments in your instance.

## About this task

## Procedure

1.  Download the required SBOM applications from the ServiceNow Store into your ServiceNow instance.

    These applications enable you to upload and import SBOM files into your instance. You can view BOM entity and component data in the SBOM Workspace if you have SBOM Core installed.

    You can view BOM entity, component data, and data visualizations in the SBOM Workspace if you have SBOM Response installed.

    -   Data Model for SBOM
    -   SBOM Core
    For more information about downloading and activating applications, see the following:

    -   [Security Operations and the ServiceNow Store](https://servicenow.com/docs/bundle/utah-security-management/page/product/planning-and-policy/concept/secops-and-store.html)
    -   [Download an application from the ServiceNow Store for the first time](../../../security-incident-response/reference/download-app-first-time.md)
2.  If you want to view your SBOM data in the SBOM Workspace, view imported third-party vulnerability intelligence, assess your risk exposure, and remediate vulnerabilities with the Application Vulnerability Response and Vulnerability Response workflows, download the following applications:

    -   Vulnerability Response and its dependencies
    -   Vulnerability Response Integration with NVD
    -   SBOM Response
    For more information about these and other supported SBOM applications, see [Exploring Software Bill of Materials](../concept/vr-sbom-exploring.md).

3.  After you have downloaded the applications, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

4.  Locate the SBOM applications that you downloaded and select **Install** to activate them along with their dependencies.

    A message is displayed after an application is successfully activated. Activate the applications in the following order:

    -   Vulnerability Response and its dependencies
    -   Vulnerability Response Integration with NVD
    -   Data Model for SBOM
    -   SBOM Core
    -   SBOM Response, which includes the OSV.dev and Deps.dev integrations and supports the Policy as Code Engine \(PaCE\) interface in the SBOM Workspace.
    See [Configuring the Deps.dev, OSV.dev, and PaCE integrations for Software Bill of Materials](../concept/vr-sbom-config-osv-deps.md) for more information about configuring these integration applications after you have installed SBOM Response.

5.  Activate integrations by navigating to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All** and selecting **Install**.

    For more information about these integrations and the capabilities they provide, see [Exploring Software Bill of Materials](../concept/vr-sbom-exploring.md).

    -   Vulnerability Response Integration with Veracode. See [Install the ServiceNow Vulnerability Response Integration with Veracode](../../veracode/task/install-veracode.md) for more information.
    -   Vulnerability Response Integration with NVD, which is required if you want to view the enhanced data for vulnerabilities associated with uploaded components. See [Understanding the NVD integrations](../../nvd/concept/nvd-vuln-integration.md) for more information.
    -   CWE Comprehensive 2000 Integration. See [Configure and run the scheduled job for updating CWE records](../../../vulnerability-response/task/t_ConfigureScheduledJobsCWE.md) for more information about activating this scheduled job.
    A message is displayed after an application is successfully activated.

6.  Assign the following roles to users.

    -   sn\_sbom\_dm.app\_create
    -   sn\_sbom\_dm.app\_read
    -   sn\_sbom\_dm.app\_write
    -   sn\_sbom\_core.sbom\_ingest
    -   sn\_sbom\_core.admin
    -   sn\_sbom\_resp.sbom\_analyst
    -   sn\_sbom\_resp.manage\_avi\_rule
    -   sn\_sbom\_response.managelicense
    -   sn\_sbom\_response.licenseresolver
7.  Assign users to the App-Sec Manager group if you are creating application vulnerable items for vulnerabilities in your imported SBOM data.

    Users assigned to the App-Sec Manager group prioritize and manage application vulnerable items. Users in this group inherit many of the roles required for reading and editing records and configuring the applications supported by the Application Vulnerability Response application and its remediation workflows.

8.  Deactivate the Reopen AVITs if detected \(**sn\_sbom\_resp.reopen\_avits\_if\_detected**\) system property if you don't want **Closed** AVITs to transition back to the **Open** state automatically.

    A **Closed** application vulnerable item \(AVIT\) for a component with an associated vulnerability is re-opened \(set to **Open**\) automatically and visible in the SBOM Workspace if the following conditions exist:

    -   The AVIT with the associated vulnerability is detected again by a third-party integration's vulnerability scans or the component with the vulnerability is part of a subsequent SBOM upload.
    -   You have not deactivated the Reopen AVITs if detected \(**sn\_sbom\_resp.reopen\_avits\_if\_detected**\) system property. This system property is activated by default.
    -   The substate of the **Closed** AVIT is not one of the following: **Mitigation Control in Place**, **Not Affected**, or **False Positive**. AVITs with these substates are not reopened by the system property.

## What to do next

Upload your SBOM files. See [Upload Software Bill of Materials files manually](vr-sbom-ingest.md) and [Uploading Software Bill of Materials files using a REST API](../concept/vr-sbom-preparing-upload.md) for more information.

