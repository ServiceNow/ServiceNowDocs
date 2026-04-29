---
title: Unified Security Exposure Management integrations
description: Unified Security Exposure Management supports multiple third-party integrations to help with vulnerability management, orchestration and remediation. This section provides guidelines for managing and developing integrations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [Unified Security Exposure Management, Security Operations]
---

# Unified Security Exposure Management integrations

Unified Security Exposure Management supports multiple third-party integrations to help with vulnerability management, orchestration and remediation. This section provides guidelines for managing and developing integrations.

## How integrations work

Integrations work in the following way:

1.  Vulnerability entries are imported from the National Vulnerability Database \(NVD\), Central Vulnerability Database and third-party scanners.
2.  Detection data from third-party scanners are matched against assets in your Configuration Management Database \(CMDB\).
3.  When a match is found, a finding is created.
4.  The findings are then:
    -   Grouped into remediation tasks.
    -   Risk-scored with business context.
    -   Prioritized and assigned to the appropriate teams.

The following table provides a list of Unified Security Exposure Management integrations created by ServiceNow® and partners.

<table id="table_cyh_1yv_t2c"><thead><tr><th>

Integration

</th><th>

Product installation

</th><th>

Category

</th><th>

Use case

</th><th>

Setup Guide

</th><th>

Built by

</th></tr></thead><tbody><tr><td colspan="6">

Import vulnerabilities and create vulnerable items

</td></tr><tr><td>

Tenable

</td><td>

[Vulnerability Response Integration with Tenable](https://store.servicenow.com/store/app/861aa3e21b246a50a85b16db234bcb7c)

</td><td>

Vulnerability Response

</td><td>

Match assets, import third-party vulnerabilities to create vulnerable items.

**Note:** Tenable.io doesn’t support launching rescan on agent-based machines.

</td><td>

[Understanding the Tenable Vulnerability Integration](../../secops-integration-vr/tenable/concept/tenableIntegration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

AWS

</td><td>

[AWS Integration for Security Exposure Management](../../security-exposure-management-integrations/concept/aws-integration-for-security-exposure-management-overview.md)

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Rapid7

</td><td>

[Rapid7 Integration for Security Operations](https://store.servicenow.com/store/app/7f9ee14647a72690def56992e36d43b8)

</td><td>

Vulnerability Response

</td><td>

Match assets, import third-party vulnerabilities to create vulnerable items.

</td><td>

[Understanding the Rapid7 Vulnerability Integration](../../secops-integration-vr/rapid7/concept/r7-vuln-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Qualys

</td><td>

[Qualys Integration for Security Operations](https://store.servicenow.com/store/app/ce8ead02c323aa10ef46d0af0501315e)

</td><td>

Vulnerability Response

</td><td>

Match assets, import third-party vulnerabilities to create vulnerable items.

**Note:** On-demand rescan is available.

</td><td>

[Understanding the Qualys Vulnerability Integration](../../secops-integration-vr/qualys/concept/c_QualysVulnIntegration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

CrowdStrike

</td><td>

[CrowdStrike Falcon Exposure Management for Vulnerability Response](https://store.servicenow.com/store/app/ca6ca7ae1b246a50a85b16db234bcb87)

</td><td>

Vulnerability Response

</td><td>

Match assets and use NVD to create vulnerable items. Supports tag-based filtering on import.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Microsoft

</td><td>

[Vulnerability Response Integration with Microsoft Threat and Vulnerability Management](https://store.servicenow.com/store/app/b98ee10e47ebea1039e06507e26d4387)

</td><td>

Vulnerability Response

</td><td>

Match assets and import endpoint vulnerabilities to create vulnerable items.

</td><td>

[Understanding the Microsoft Threat and Vulnerability Management Vulnerability integration](../../secops-integration-vr/mstvm/concept/mstvm-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Microsoft

</td><td>

[Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)](https://store.servicenow.com/store/app/349ce3ee1b246a50a85b16db234bcb40)

</td><td>

Vulnerability Response

</td><td>

Import vulnerabilities into ServiceNow Operational Technology Vulnerability Response and take risk-based action with production process context.

</td><td>

[Understanding the Vulnerability Response patch orchestration integration with Microsoft SCCM](../../secops-integration-vr/ms-sccm-patch-orchestration/concept/mspatch-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Cisco

 \(Kenna\)

</td><td>

[Kenna.VM \(Vulnerability Management\)](https://store.servicenow.com/store/app/5b7d2b261b646a50a85b16db234bcb43)

</td><td>

Vulnerability Response

</td><td>

Match assets and use NVD to create vulnerable items. Includes Kenna Risk score.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Tanium

</td><td>

[Tanium Vulnerability Management](https://store.servicenow.com/store/app/b13aafe21b246a50a85b16db234bcb0e)

</td><td>

Vulnerability Response

</td><td>

Match assets and import third-party vulnerabilities to create vulnerable items.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Orca

</td><td>

[Orca Security for Vulnerability Response](https://store.servicenow.com/store/app/20b9a3621b246a50a85b16db234bcb31)

</td><td>

Vulnerability Response

</td><td>

Match assets and import third-party vulnerabilities to create vulnerable items.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Onapsis

</td><td>

[Onapsis Vulnerability Integration](https://store.servicenow.com/store/app/c8b963621b246a50a85b16db234bcb69)

</td><td>

Vulnerability Response

</td><td>

Match assets and import third-party vulnerabilities to create vulnerable items for SAP assets and applications.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Synack

</td><td>

[Synack - Vulnerability Response](https://store.servicenow.com/store/app/2960bbe21ba46a50a85b16db234bcbc0)

</td><td>

Vulnerability Response

</td><td>

Import vulnerabilities from Synack.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Wiz.io

</td><td>

[Wiz Integration for Security Operations](https://store.servicenow.com/store/app/d069e3ee1be06a50a85b16db234bcb1d)

</td><td>

Vulnerability Response

</td><td>

Match cloud assets and import third-party vulnerabilities to create vulnerable items.

</td><td>

[Understanding the Wiz Vulnerability Response Integration](../../secops-integration-vr/wiz-host-vuln-integration/concept/vr-wiz-exploring-host-cf.md)

</td><td>

Partner

</td></tr><tr><td>

Lacework

</td><td>

Lacework

</td><td>

Vulnerability Response

</td><td>

Import infrastructure vulnerabilities from your cloud asset sources. Supports vulnerability calculator and filtering by severity.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Recorded Future

</td><td>

[Attack Surface Intelligence](https://store.servicenow.com/store/app/8519e76e1be06a50a85b16db234bcbbb)

</td><td>

Vulnerability Response

</td><td>

External attack surface assets and exposures imported into ServiceNow Vulnerability Response. Create vulnerable items from external asset detections. Includes Recorded Future threat and vulnerability enrichment.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Mandiant

</td><td>

Mandiant Attack Surface Management

</td><td>

Vulnerability Response

</td><td>

Import information about vulnerabilities and vulnerable items from the Mandiant Attack Surface Management platform.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

IBM

</td><td>

[IBM Guardium Data Protection](https://store.servicenow.com/store/app/36bc63221b646a50a85b16db234bcbc1)

</td><td>

Vulnerability Response

</td><td>

Integrate IBM Guardium database vulnerability scan results with ServiceNow.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

CyCognito

</td><td>

[CyCognito App for Vulnerability Response](https://store.servicenow.com/store/app/fc4c2f6e1b246a50a85b16db234bcb98)

</td><td>

Vulnerability Response

</td><td>

Import issues and assets from Cycognito SAAS platform.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

VMware

</td><td>

Carbon Black Cloud

</td><td>

Vulnerability Response

</td><td>

Ingest vulnerability data and context from Carbon Black Cloud.

 Create configuration items from Carbon Black Cloud endpoints and workload.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Nucleus

</td><td>

[Nucleus Security for Vulnerability Response](https://store.servicenow.com/store/app/4aaaef661b246a50a85b16db234bcbab)

</td><td>

Vulnerability Response

</td><td>

-   Import findings from Nucleus Security Auto-update Vulnerable Items.
-   Bi-directional update via comments field.
-   Map custom fields.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

InfoSec Global \(ISG\)

</td><td>

[InfoSec Global \(ISG\) AgileSec Analytics Integration for Vulnerability Response Module](https://store.servicenow.com/store/app/9d4bef2a1b246a50a85b16db234bcb30)

</td><td>

Vulnerability Response

</td><td>

Import vulnerability findings on Cryptographic assets:

 Cryptographic Keys, Keystores, and Libraries

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Censys

</td><td>

[Censys ASM to Vulnerability Response Integration](https://store.servicenow.com/store/app/68603be21ba46a50a85b16db234bcba1)

</td><td>

Vulnerability Response

</td><td>

Scan, discover, and catalog vulnerabilities on internet-facing assets.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td colspan="6">

Import container findings, vulnerabilities, and images

</td></tr><tr><td>

Palo Alto

</td><td>

[Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute](https://store.servicenow.com/store/app/d4ae2dc6536faa1072c95a01a0490e35)

</td><td>

Container Vulnerability Response

</td><td>

Ingest container vulnerabilities from Prisma Cloud Compute \(formerly Twistlock\) and use runtime context \(cluster/ namespace and so on\) to automate remediation workflow.

</td><td>

[Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute integration](../../secops-integration-vr/prisma/concept/pcc-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Aqua

</td><td>

[Aqua Security Platform integration with Vulnerability Response for Containers](https://store.servicenow.com/store/app/fedb6fea1b246a50a85b16db234bcb7c)

</td><td>

Container Vulnerability Response

</td><td>

Import container vulnerabilities from Aqua Platform.

 Docker and MID Server support.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

AWS

</td><td>

[AWS Integration for Security Exposure Management](../../security-exposure-management-integrations/concept/aws-integration-for-security-exposure-management-overview.md)

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sysdig

</td><td>

[Sysdig Container Vulnerability Response](https://store.servicenow.com/store/app/cf3927ae1be06a50a85b16db234bcba0)

</td><td>

Container Vulnerability Response

</td><td>

Import container vulnerabilities from Sysdig. Supports VI granularity, container, kubernetes, and host security

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Lacework

</td><td>

Lacework

</td><td>

Container Vulnerability Response

</td><td>

Import container vulnerabilities and attempt to match based on docker configuration items \(CIs\).

 Supports vulnerability calculator and filtering by severity.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

WIZ

</td><td>

[Wiz Integration for Container Vulnerability Response](https://store.servicenow.com/store/app/225b676a1b246a50a85b16db234bcb18)

</td><td>

Container Vulnerability Response

</td><td>

Import all container vulnerabilities from Wiz.

</td><td>

[Exploring the Wiz Container Vulnerability Integration](../../secops-integration-vr/wiz-cvr-container-vuln-integration/concept/wiz-exploring-cvr-vuln-intcf.md)

</td><td>

Partner

</td></tr><tr><td>

Qualys

</td><td>

[Qualys Container Vulnerability Response Integration](https://store.servicenow.com/store/app/c309276e1be06a50a85b16db234bcbb8)

</td><td>

Container Vulnerability Response

</td><td>

Import all container vulnerabilities from QCS.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

CrowdStrike

</td><td>

[CrowdStrike Falcon Cloud security for Container Vulnerability Response](https://store.servicenow.com/store/app/10728f441b9dea10a85b16db234bcb4e)

</td><td>

Container Vulnerability Response

</td><td>

Import all container vulnerabilities from FCS.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td colspan="6">

Solution Intelligence

</td></tr><tr><td>

Microsoft

</td><td>

[Vulnerability Solution Management](https://store.servicenow.com/store/app/8f2e6b2a1b646a50a85b16db234bcb2a)

</td><td>

Vulnerability Response - Content

</td><td>

Provides solution content for vulnerabilities.

</td><td>

[Microsoft Security Response Center Solution Integration](../../secops-integration-vr/msrc/concept/mscr-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Red Hat

</td><td>

Red Hat Security Data

</td><td>

Vulnerability Response - Content

</td><td>

Provides solution content for vulnerabilities.

</td><td>

[Red Hat Solution Integration](../../secops-integration-vr/redhat/concept/redhat-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Rapid 7

</td><td>

[Rapid7 Integration for Security Operations](https://store.servicenow.com/store/app/7f9ee14647a72690def56992e36d43b8)

</td><td>

Vulnerability Response - Content

</td><td>

Provides solution content for vulnerabilities.

</td><td>

[Rapid7 solution management](../../secops-integration-vr/rapid7/concept/rapid-7-solution-management.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Tanium

</td><td>

[Tanium Vulnerability Management](https://store.servicenow.com/store/app/b13aafe21b246a50a85b16db234bcb0e)

</td><td>

Vulnerability Response - Content

</td><td>

Provides solution content for vulnerabilities.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

CVRF Generic Framework

</td><td>

Supports CVRF Format

</td><td>

Vulnerability Response - Content

</td><td>

Provides solution content for vulnerabilities.

</td><td>

-   [Generic framework to ingest data from any solution vendor](../../vulnerability-response/concept/ingest-data-solution-vendors-generic-framework.md)
-   [Setting up vulnerability solution providers](../../vulnerability-response/concept/setup-vulnerability-solution-providers.md)

</td><td>

ServiceNow

</td></tr><tr><td>

CSAF Generic Framework

</td><td>

Supports CSAF Format

</td><td>

Vulnerability Response - Content

</td><td>

Provides solution content for vulnerabilities.

</td><td>

-   [Generic framework to ingest data from any solution vendor](../../vulnerability-response/concept/ingest-data-solution-vendors-generic-framework.md)
-   [Setting up vulnerability solution providers](../../vulnerability-response/concept/setup-vulnerability-solution-providers.md)

</td><td>

ServiceNow

</td></tr><tr><td colspan="6">

Vulnerability enrichment and threat scoring

</td></tr><tr><td>

Recorded Future

</td><td>

Vulnerability Intelligence

</td><td>

Vulnerability Response - Intelligence

</td><td>

Use Recorded Future vulnerability intelligence to prioritize vulnerabilities.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Flashpoint

</td><td>

[Flashpoint Ignite for Vulnerability Response](https://store.servicenow.com/store/app/d54e236a1b646a50a85b16db234bcbdb)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Consume alerts as security incidents \(email\), Import TI and vulnerability context.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Cisco \(Kenna\)

</td><td>

[Kenna.VI+ \(Kenna Vulnerability Intel\)](https://store.servicenow.com/store/app/d5c92b621b246a50a85b16db234bcbb0)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Use Kenna.vi vulnerability intelligence to prioritize vulnerabilities.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Risk Based Security by Flashpoint

</td><td>

[Flashpoint VulnDB](https://store.servicenow.com/store/app/bb3ceb6e1b246a50a85b16db234bcba4)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Import RBS records into third-party vulnerabilities.

 Risk scores and software-based vulnerability matching.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Digital Shadows \(Grey Matter by Reliaquest\)

</td><td>

[GreyMatter Digital Risk Protection Vulnerability Intelligence for Vulnerability Response](https://store.servicenow.com/store/app/6f7d2b261b646a50a85b16db234bcb86)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Prioritize vulnerabilities using Digital Shadows risk factors and scoring based on analyst-curated threat intelligence.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Mandiant \| Google

</td><td>

[Google Threat Intelligence for SecOps](https://store.servicenow.com/store/app/07f781de4798bed4392d3369126d4370)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Enriches vulnerability item records with Mandiant vulnerability intelligence for better prioritization.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

CISA

</td><td>

[Vulnerability Response Integration with CISA](https://store.servicenow.com/store/app/02ea27e61b246a50a85b16db234bcb2e)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Use known exploitedvulnerabilities.

 Catalog to prioritize vulnerabilities.

</td><td>

[CISA Known Exploit Vulnerability \(KEV\) Integration](../../secops-integration-vr/CISA/concept/cisa-vuln-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

First.org

</td><td>

EPSS

</td><td>

Vulnerability Response - Intelligence

</td><td>

Use the Exploit prediction scoring system to prioritize vulnerabilities.

</td><td>

[Understanding the Exploit Prediction Scoring System \(EPSS\) integration](../../secops-integration-vr/epss/concept/epss-vr-integration-overview.md)

</td><td>

ServiceNow

</td></tr><tr><td>

XM Cyber

</td><td>

[XM Cyber - Vulnerability Response](https://store.servicenow.com/store/app/d8f9a7a21b246a50a85b16db234bcbac)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Asset Ingestion

 Link Additional Risk Data

 Application Risk Measures

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Zafran

</td><td>

[Zafran Threat Exposure Management Platform](https://store.servicenow.com/store/app/ccebefea1b246a50a85b16db234bcb21)

</td><td>

Vulnerability Response - Intelligence

</td><td>

Ingest vulnerabilities from scanning tools, provide Zafran enrichment and then link to vulnerable items in Vulnerability Response.

 Intelligence includes mitigation factors, internet-facing, and custom risk score.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td colspan="6">

Patch orchestration in solution management

</td></tr><tr><td>

Microsoft

</td><td>

[Vulnerability Response Patch Orchestration with Microsoft SCCM](https://store.servicenow.com/store/app/c1dbabea1b246a50a85b16db234bcbdf)

</td><td>

Vulnerability Response - Patching

</td><td>

Ingest the patch details and correlate the patch, solution, and asset details to suggest Security and IT which assets are missing patches.

</td><td>

[Understanding the Vulnerability Response patch orchestration integration with Microsoft SCCM](../../secops-integration-vr/ms-sccm-patch-orchestration/concept/mspatch-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

HCL

</td><td>

[Vulnerability Response Patch Orchestration with HCL Bigfix](https://store.servicenow.com/store/app/02196b6e1be06a50a85b16db234bcb05)

</td><td>

Vulnerability Response - Patching

</td><td>

Ingest the patch details and correlate the patch, solution, and asset details to suggest Security and IT which assets are missing patches.

</td><td>

[Understanding the HCL BigFix patch orchestration integration with Vulnerability Response](../../secops-integration-vr/bigfix/concept/vr-bigfix-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Tanium

</td><td>

[Tanium Patch Management for Vulnerability Response](https://store.servicenow.com/store/app/b41a63e21b246a50a85b16db234bcb1e)

</td><td>

Vulnerability Response - Patching

</td><td>

Patches CIs through the Vulnerability Response Patch Orchestration module. This can be used in addition to the Tanium VR integration to close the loop from identifying vulnerabilities with Tanium Comply to patching those vulnerabilities with Tanium Patch.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td colspan="6">

Import test, policies, results

</td></tr><tr><td>

Qualys

</td><td>

[Qualys Integration for Security Operations](https://store.servicenow.com/store/app/ce8ead02c323aa10ef46d0af0501315e)

</td><td>

Configuration Compliance

</td><td>

Import test, policies, results.

</td><td>

[Qualys integration with Configuration Compliance](../../secops-integration-cc/qualys/concept/Qualys-cc-Integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Qualys

</td><td>

[Qualys CSPM Integration](https://store.servicenow.com/store/app/8cfda1d71b792210f4b3dc28b04bcbcc)

</td><td>

Configuration Compliance

</td><td>

Import test, policies, results.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

AWS

</td><td>

[AWS Integration for Security Exposure Management](../../security-exposure-management-integrations/concept/aws-integration-for-security-exposure-management-overview.md)

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Tenable

</td><td>

[Vulnerability Response Integration with Tenable](https://store.servicenow.com/store/app/ce8e6186476f6e10392d3369126d43c2)

</td><td>

Configuration Compliance

</td><td>

Import test, policies, results.

</td><td>

[Understanding the Tenable Vulnerability Integration](../../secops-integration-vr/tenable/concept/tenableIntegration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Tanium

</td><td>

[Tanium Configuration Compliance Integration](https://store.servicenow.com/store/app/19517b2a1ba46a50a85b16db234bcb87)

</td><td>

Configuration Compliance

</td><td>

Import test, policies, results.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Palo Alto Networks

</td><td>

[Expander Configuration Compliance](https://store.servicenow.com/store/app/c3d9ef621b246a50a85b16db234bcb8d)

</td><td>

Configuration Compliance

</td><td>

Import attack surface and alerts from Expander.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Trend Micro

</td><td>

[Conformity Connector](https://store.servicenow.com/store/app/bc1e632a1b646a50a85b16db234bcb36)

</td><td>

Configuration Compliance

</td><td>

Import misconfiguration and test results from Trend Micro Cloud One into ServiceNow.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td colspan="6">

Import cloud misconfiguration data \(Cloud Security\)

</td></tr><tr><td>

Microsoft

</td><td>

Defender for Endpoint

</td><td>

Configuration Compliance

</td><td>

Import test, policies, results.

</td><td>

 

</td><td>

ServiceNow

</td></tr><tr><td>

Microsoft

</td><td>

[Microsoft Defender for Cloud Integration for Security Operations](https://store.servicenow.com/store/app/a68eed0a972f66903fa8b84bf253af7e)

</td><td>

Configuration Compliance

</td><td>

Import the cloud resource configuration issues from Microsoft Defender for Cloud and automate remediation workflow.

</td><td>

[Microsoft Defender for Cloud Integration for Security Operations](../../secops-integration-vr/azure-security-center/concept/cc_asc_overview.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Palo Alto

</td><td>

[Vulnerability Response Integration with Palo Alto Prisma Cloud](https://store.servicenow.com/store/app/d98e210a47eb221082f632c4f16d4372)

</td><td>

Configuration Compliance

</td><td>

Import the cloud resource configuration issues from Prisma Cloud \(formerly RedLock\) and automate remediation workflow.

</td><td>

[Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud](../../secops-integration-vr/prisma/concept/prisma-cloud-overview.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Wiz

</td><td>

[Wiz Integration for Configuration Compliance](https://store.servicenow.com/store/app/81d96f621b246a50a85b16db234bcb56)

</td><td>

Configuration Compliance

</td><td>

Import the cloud resource configuration issues from Microsoft Defender for Cloud and automate remediation workflow.

</td><td>

[Exploring the Wiz Test Results and Issues Integrations with Configuration Compliance](../../secops-integration-cc/wiz-test-results-integration/concept/exploring-wiz-ctest-results-int.md)

</td><td>

Partner

</td></tr><tr><td>

Rapid7

</td><td>

[Rapid7 InsightCloudSec CC Integration](https://store.servicenow.com/store/app/b04f67ae1b646a50a85b16db234bcb97)

</td><td>

Configuration Compliance

</td><td>

Import cloud misconfigurations and compliance issues

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Lacework

</td><td>

Lacework Code to Cloud

</td><td>

Configuration Compliance

</td><td>

Import cloud misconfigurations and compliance issues.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

AWS

</td><td>

[AWS Integration for Security Exposure Management](../../security-exposure-management-integrations/concept/aws-sem-integrations.md)

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td colspan="6">

Import dynamic, static analysis results and SCA

</td></tr><tr><td>

Veracode

</td><td>

[Vulnerability Response Integration with Veracode](https://store.servicenow.com/store/app/89588e41c323ee505ce25ddf05013120)

</td><td>

Application Vulnerability Response

</td><td>

Import test, policies, results, DAST findings, SAST findings and SCA findings.

</td><td>

[Veracode Vulnerability Integration](../../secops-integration-vr/veracode/concept/veracode-vuln-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Qualys WAS

</td><td>

[Vulnerability Response Integration with Qualys WAS](https://store.servicenow.com/store/app/be6e2f6a1b646a50a85b16db234bcbb1)

</td><td>

Application Vulnerability Response

</td><td>

Import Dynamic Scan results from Qualys WAS application.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Microfocus

 Fortify

</td><td>

[Fortify Application Vulnerability Integration](https://store.servicenow.com/store/app/c68e2142c323aa10ef46d0af0501310e)

</td><td>

Application Vulnerability Response

</td><td>

Import DAST and SAST findings.

</td><td>

[Fortify Vulnerability Integration](../../secops-integration-vr/fortify-on-demand/concept/fortify-vuln-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Snyk

</td><td>

[Snyk Security for Application Vulnerability Response](https://store.servicenow.com/store/app/bc2ae7e21b246a50a85b16db234bcb88)

</td><td>

Application Vulnerability Response

</td><td>

Import SCA and SAST findings.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td colspan="6">

Open source vulnerability intelligence \(SBOM workflows\)

</td></tr><tr><td>

Snyk

</td><td>

[Snyk API and Web for Application Vulnerability Response](https://store.servicenow.com/store/app/0a5317329797ea103fa8b84bf253afe4)

</td><td>

Application Vulnerability Response

</td><td>

Web App Scanning findings

 API Security findings

</td><td>

 

</td><td>

ServiceNow

</td></tr><tr><td>

GitHub

</td><td>

[Github Application Vulnerability Integration](https://store.servicenow.com/store/app/006dafe21b646a50a85b16db234bcba2)

</td><td>

Application Vulnerability Response

</td><td>

Code Scanning Secret Scanning Dependabot alerts.

</td><td>

[GitHub Application Vulnerability Integration](../../secops-integration-vr/github-vulnerability/concept/github-vuln-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

HCL AppScan

</td><td>

[Vulnerability Response Integration with HCL AppScan](https://store.servicenow.com/store/app/a73a23261b246a50a85b16db234bcb3b)

</td><td>

Application Vulnerability Response

</td><td>

Import Dynamic Scan results from HCL AppScan.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Checkmarx

</td><td>

[Checkmarx CxSAST Vulnerability Integration](https://store.servicenow.com/store/app/cf19ab6e1be06a50a85b16db234bcb55)

</td><td>

Application Vulnerability Response

</td><td>

Import SAST findings.

**Note:** Uses CxSAST API.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Checkmarx

</td><td>

[Checkmarx One Vulnerability Integration](https://store.servicenow.com/store/app/cbc8efea1be06a50a85b16db234bcb97)

</td><td>

Application Vulnerability Response

</td><td>

Import SAST and SCA findings from Cx VulnerabilityOne API.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Invicti

</td><td>

[Invicti Application Vulnerability Integration](https://store.servicenow.com/store/app/c8635e664717aa1002872f46736d43b0)

</td><td>

Application Vulnerability Response

</td><td>

-   Import applications, scan summaries, results
-   Import IAST findings.
-   Import SAST findings.

</td><td>

[Invicti Vulnerability Integration](../../secops-integration-vr/invicti/concept/invicti-vuln-integration.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Synopsys

</td><td>

[Vulnerability Response Integration with Black Duck](https://store.servicenow.com/store/app/c7b3d2a293d72a10a0f2fc1d6cba10a3)

</td><td>

Application Vulnerability Response

</td><td>

Import SCA findings.

</td><td>

[Vulnerability Response Integration with Black Duck](../../secops-integration-vr/blackduck-integration/concept/vulnerability-response-integration-blackduck-overview.md)

</td><td>

ServiceNow

</td></tr><tr><td>

Sonatype

</td><td>

[Sonatype Security for Application Vulnerability Response](https://store.servicenow.com/store/app/fb6aef261b246a50a85b16db234bcb0e)

</td><td>

Application Vulnerability Response

</td><td>

SCA – import open source vulnerabilities from Sonatype Lifecycle product.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Apiiro

</td><td>

[Apiiro ASPM for Application Vulnerability Response](https://store.servicenow.com/store/app/945d2be21b646a50a85b16db234bcb5f)

</td><td>

Application Vulnerability Response

</td><td>

Application Security Posture Management vulnerabilities, fix issues by assigning to code owners [CMDB App](https://store.servicenow.com/store/app/c3be7a921bd666d02ca2a643604bcb80) is also available.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Rapid7

</td><td>

[Rapid7 InsightAppSec Application VR Integration](https://store.servicenow.com/store/app/335dafe21b646a50a85b16db234bcb73)

</td><td>

Application Vulnerability Response

</td><td>

Fetch apps, scans, vulnerabilities, attacks, attack modules into ServiceNow Vulnerability Response. Web application scanning results.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

NoName \(by Akamai\)

</td><td>

[Akamai API Security Integration for AVR](https://store.servicenow.com/store/app/3432376e1ba46a50a85b16db234bcb03)

</td><td>

Application Vulnerability Response

</td><td>

Create and update vulnerable items from NoName on API detections.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Tenable

</td><td>

Tenable WAS

</td><td>

Application Vulnerability Response

</td><td>

Application security findings.

</td><td>

 

</td><td>

Partner

 \(Tenable\)

</td></tr><tr><td>

Snyk

</td><td>

[Snyk Vulnerability Intelligence for SBOM](https://store.servicenow.com/store/app/994d67e21b646a50a85b16db234bcb56)

</td><td>

Application Vulnerability Response - SBOM

</td><td>

Vulnerability Intelligence on Open-source components in SBOM.

</td><td>

 

</td><td>

Partner

</td></tr><tr><td>

Google \(open source\)

</td><td>

[SBOM Response](https://store.servicenow.com/store/app/0bd8e32e1be06a50a85b16db234bcba1)

</td><td>

Application Vulnerability Response - SBOM

</td><td>

Vulnerability intelligence information for a given version of a package or library.

</td><td>

 

</td><td>

ServiceNow

</td></tr><tr><td>

Google \(open source\)

</td><td>

[SBOM Response](https://store.servicenow.com/sn_appstore_store.do%23!/store/application/6e1505c977007110adaf0da3fa5a99e1/3.0.3?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dosv&sl=sh)

</td><td>

Application Vulnerability Response - SBOM

</td><td>

License and dependency information for a given version of a package or library.

</td><td>

 

</td><td>

ServiceNow

</td></tr><tr><td>

Veracode

</td><td>

[Vulnerability Response Integration with Veracode](https://store.servicenow.com/store/app/89588e41c323ee505ce25ddf05013120)

</td><td>

Application Vulnerability Response - SBOM

</td><td>

-   Upload exported vulnerabilities to create AVITs.
-   Prioritize by NVD severity.

</td><td>

 

</td><td>

ServiceNow

</td></tr><tr><td colspan="6">

Agile task creation for remediation

</td></tr><tr><td>

Atlassian

</td><td>

[Vulnerability Response Integration with Atlassian Jira](https://store.servicenow.com/store/app/a83a2fe21b246a50a85b16db234bcb22)

</td><td>

Vulnerability Response - Agile Tools

</td><td>

Create Jira tasks/ issues for Application and Container vulnerabilities. Bi-directional status updates between Vulnerability Response and Jira.

</td><td>

[Understanding the Atlassian Jira integration with Vulnerability Response](../../secops-integration-vr/jira/concept/jira-vuln-integration.md)

</td><td>

ServiceNow

</td></tr></tbody>
</table>## Custom integrations

You can manually create integrations not available in the ServiceNow Store. See [Manually create a vulnerability integration](../../vulnerability-response/concept/c_VulnerabilityIntegrations.md) for more information.

## Configuring and managing integrations

-   You can install, configure, schedule, and launch many integration applications.
-   For integrations supporting multiple deployments, refer to [Create domain-separated imports for an integration](../../vulnerability-response/task/create-domain-separated-imports.md).
-   The Rapid7 Vulnerability Integration application can be installed from Setup Assistant, but its configuration isn’t supported within Setup Assistant. See [Install the Rapid7 Vulnerability Integration](../../secops-integration-vr/rapid7/task/install-and-configure-r7.md) for more information. You can install, configure, schedule, and launch on-demand many of the integration applications from within Setup Assistant.

## Performance and timeout handling

During integration execution, multiple processes are generated, and data is received in the form of pages. Each process can contain one or more import queue entries with attached data in pages. These entries must process the data within the one-hour time limit. However, if the payload size is large, the processing time may exceed one hour or get stuck, resulting in an integration timeout error. The integration continues to process the data despite the timeout error. To avoid this miscommunication, timestamps \(heartbeats\) are sent periodically to indicate if the queue is active and processing data. The **Last Record Processed** field in the Import Queue Entry page is updated based on the count of records the import queue creates or updates. In case an import queue entry exceeds the one-hour time limit, the system checks the **Last Record Processed** field to see if it’s also older than one hour. If it is, this indicates that the import queue entry is stuck, and it’s timed out to prevent any further delays in processing.

**Note:** The **Last Record Processed** field is updated based on what is defined in the following system properties:

-   **sn\_sec\_cmn.record\_threshold\_heartbeat**: Defines the number of processed records, after which the heartbeat \(timestamp\) is sent to the import queue entry.
-   **sn\_sec\_cmn.maximum\_heartbeat\_delay**: Defines the time after which the import queue entry must be timed out.

-   **[Review Unified Security Exposure Management integrations](../../security-exposure-management-administration/concept/review-usem-integrations.md)**  
The integration dashboard provides an overview of the installed third-party applications and the status of the integration runs.

**Related topics**  


[Review Unified Security Exposure Management integrations](../../security-exposure-management-administration/concept/review-usem-integrations.md)

