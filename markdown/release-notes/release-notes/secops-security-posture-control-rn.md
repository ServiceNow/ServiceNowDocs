---
title: Security Posture Control release notes
description: The ServiceNow Security Posture Control application provides cybersecurity teams with visibility into security tool coverage gaps and deviations from security tool configuration for their enterprise assets. Security Posture Control was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-01-14"
reading_time_minutes: 3
---

# Security Posture Control release notes

The ServiceNow® Security Posture Control application provides cybersecurity teams with visibility into security tool coverage gaps and deviations from security tool configuration for their enterprise assets. Security Posture Control was enhanced and updated in the Yokohama release.

## Security Posture Control highlights for the Yokohama release

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [ServiceNow Otto for Security Incident Response \(SIR\) release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/secops-now-assist-security-operations-rn.md) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

See [Security Posture Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/spc-landing.md) for more information.

**Important:** Security Posture Control is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Security Posture Control to Yokohama

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/spc-install.md).

## New in the Yokohama release

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/spc-creating-sgc-template.md)**

    Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the ServiceNow Otto for Unified Security Exposure Management application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

        **Note:** You must install [Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md) of the ServiceNow Otto for Unified Security Exposure Management application to have access to the generative AI skill for the Connector builder framework. See the [ServiceNow Otto for Security Incident Response \(SIR\) release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/secops-now-assist-security-operations-rn.md) and [Supporting information for ServiceNow Otto for Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/supporting-information-now-assist-vr.md) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/spc-policies-overview.md)**

    Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7
-   **[SentinelOne integration for mitigation controls monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/spc-controls-policies-for-edr.md)**

    You can import SentinelOne mitigation controls data with this integration to help you detect which mitigation controls are on your assets. Use this integration with the asset and software data that you import with the SentinelOne Service Graph Connector to help you monitor your security tool coverage on your enterprise assets.

-   ****

    This product pulls in asset inventory data for hardware and software from the Netskope database into the ServiceNow Configuration Management Database \(CMDB\) application.


## Activation information

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/security-operations-rn-landing.md)

