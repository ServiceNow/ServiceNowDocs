---
title: Security Posture Control release notes
description: The ServiceNow Security Posture Control application provides cybersecurity teams with visibility into security tool coverage gaps and deviations from security tool configuration for their enterprise assets. Security Posture Control was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-28"
reading_time_minutes: 4
---

# Security Posture Control release notes

The ServiceNow® Security Posture Control application provides cybersecurity teams with visibility into security tool coverage gaps and deviations from security tool configuration for their enterprise assets. Security Posture Control was enhanced and updated in the Zurich release.

## Security Posture Control highlights for the Zurich release

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/secops-now-assist-security-operations-rn.md) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

See [Security Posture Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/spc-landing.md) for more information.

**Important:** Security Posture Control is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Security Posture Control to Zurich

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/spc-install.md). Starting with Zurich Patch 12, Now Assist for Vulnerability Response is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. The change is reflected in the name of ServiceNow® products, including Now Assist for Vulnerability Response which is called ServiceNow Otto for Unified Security Exposure Management. See [ServiceNow Otto for Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-usem-landing-ties.md) for more information.

## New in the Zurich release

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/spc-creating-sgc-template.md)**

    Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the ServiceNow Otto for Unified Security Exposure Management application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

        **Note:** You must install Zurich Patch 4 of the ServiceNow Otto for Unified Security Exposure Management application to have access to the generative AI skill for the Connector builder framework. See the [ServiceNow Otto for Security Incident Response \(SIR\) \(SIR\) release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/secops-now-assist-security-operations-rn.md) and [Supporting information for Unified Security Exposure Management AI skills and agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/supporting-information-now-assist-vr.md) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/spc-policies-overview.md)**

    Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7

## Changed in this release

-   Security Posture Control relies on data from service graph connectors that is populated in the CMDB 360 Data \[cmdb\_multisource\_data\] table. This data is populated only when the glide.identification\_engine.multisource\_enabled system property is set to true. You must have the cmdb\_ms\_admin role to modify property values. To set the property, navigate to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**.
-   The labels on the form view for the mitigation control details record associated with vulnerable item records \(VITs\) have been enhanced for more clarity. These updates make the interface more user-friendly by expanding abbreviations on the form view, such as changing "EDR" to "Endpoint Protection."

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install Security Posture Control by requesting the required applications from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/security-operations-rn-landing.md)

