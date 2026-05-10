---
title: Configuring the Deps.dev, OSV.dev, and PaCE integrations for Software Bill of Materials
description: You can edit some of the parameters for the Deps.dev and OSV.dev integrations. There are also two code trigger versions of these integrations that are used strictly for internal workflows, and you should not initiate these integrations on-demand. Additionally, you can activate a scheduled job to create policies using Policy as Code Engine \(PaCE\).
locale: en-US
release: australia
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2026-04-03"
reading_time_minutes: 3
breadcrumb: [Configure, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Configuring the Deps.dev, OSV.dev, and PaCE integrations for Software Bill of Materials

You can edit some of the parameters for the Deps.dev and OSV.dev integrations. There are also two code trigger versions of these integrations that are used strictly for internal workflows, and you should not initiate these integrations on-demand. Additionally, you can activate a scheduled job to create policies using Policy as Code Engine \(PaCE\).

## Code trigger integrations for internal workflows

Starting with v3.2 of SBOM Response, performance enhancements included the addition of two OSV.dev and Deps.dev code-trigger integrations:

-   OSV Integration \(on-demand code trigger\)
-   Deps.dev Integration \(on-demand code trigger\)

These integrations are initiated automatically by internal workflows and are for internal use only. Although you can locate them, you must not initiate these integrations on-demand with **Execute Now** button from their integration records.

## Configuring the run schedule for the Deps.dev Integration

The Deps.dev Integration is installed with SBOM Response. The integration is activated \(Active check box selected on the integration record\) by default and scheduled to run weekly. Note that this is not the on-demand Deps.dev code trigger integration, and you can edit the schedule and initiate the scheduled job on-demand from its integration record..

To modify the schedule, navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Integrations** &gt; **Deps.dev Integration**. The sn\_vul.app\_configure\_integrations role is required to edit the schedule of this integration.

This Deps.dev integration is used to identify components that are in **Stale** and **Abandoned** states. A stale component's version is more than two major versions behind the latest version and two years behind the latest version. An abandoned component has not been updated for more than two years. The two year and two version thresholds can be edited with system properties. To edit these parameters, navigate to **All** &gt; **System Properties** &gt; **All Properties** and locate the following records:

-   sn\_sbom\_resp.pkg\_abandoned\_threshold
-   sn\_sbom\_resp.pkg\_stale\_threshold
-   sn\_sbom\_resp.pkg\_stale\_version\_threshold

The threshold values for abandoned and stale are in months. The threshold value for version is numerical.

You can view imported data on the Home page of the workspace and in the BOM Queue module. Imported data is stored in the Package Groups \[sn\_sbom\_pkg\_group\] table.

## Configuring and initiating the OSV.dev Integration - Comprehensive

The OSV.dev Integration - Comprehensive integration is installed with SBOM Response. The integration is activated \(Active check box selected on the integration record\) by default. Note that this is not the on-demand OSV.dev code trigger integration, and you must initiate this integration on-demand from its integration record.

To configure and initiate this integration, navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Integrations** &gt; **OSV.dev Integration - Comprehensive**. The sn\_vul.app\_configure\_integrations role is required.

You can view imported data on the Home page of the workspace on the Vulnerability tab on records from the entities list and in the Libraries module. Imported data is stored in the Application Vulnerable Entries \[sn\_vul\_app\_vul\_entry\] and the National Vulnerability Database Entries \[sn\_vul\_nvd\_entry\] tables.

**Note:** You can configure the OSV.dev's **batchSize** integration parameter on the Integration Parameters tab on the **Open Source Vulnerabilities Instance** located at **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Integrations** &gt; **Vulnerability Integrations** &gt; **Open Source Vulnerabilities Instance**. The default is 75 Purls per API call.

You might prefer to leave this value in its default setting. Altering the value might impact performance.

## Activating PaCE

Starting with version 4.0 of SBOM Response, you can view components that are identified as stale or abandoned as ‘Non-compliant’ in the Policy as Code Engine \(PaCE\) interface that is available in the SBOM Workspace.

-   Determine if components are stale or abandoned with the **Run PaCE policies for SBOM Response** scheduled job. This scheduled job is deactivated by default.
-   View components that are identified as stale or abandoned as Non-compliant in the PaCE interface that is available and viewed in the SBOM Workspace.

See [Integrating PaCE with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-integrate-other-apps.md) for more information about PaCE and PaCE policies.

