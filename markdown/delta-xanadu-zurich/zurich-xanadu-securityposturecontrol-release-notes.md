---
title: Combined Security Posture Control release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Security Posture Control from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-securityposturecontrol-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Security Posture Control release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Security Posture Control from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Posture Control release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Posture Control to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-install&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-install&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-install&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Security Posture Control.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Mitigation Controls Monitoring with Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-mitigation-exploring&family=xanadu&ft:locale=en-US)**

From within the Security Posture Control workspace, detect mitigation controls of various types as described by MITRE on all on-premise and cloud enterprise assets. Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured.

    -   Activate mitigation control policies that are included with the application that identify MITRE mitigations on your assets.
    -   Identify your assets that have Web Application Firewall \(WAF\) protection with supported tools that include F5 BIG-IP. Automatically map a WAF mitigation to vulnerable items by analyzing the policy signatures in the firewall and the Common Vulnerabilities and Exposures \(CVE\) information.
    -   Identify exploit mitigation controls from endpoint protection or Endpoint Detection and Response \(EDR\) tools like CrowdStrike and Microsoft Defender. Automatically map the EDR exploit mitigation controls to relevant vulnerable items by analyzing the vulnerability information and the EDR mitigation control configuration.
    -   Populate vulnerable items with relevant attributes that can be used in your Vulnerability Response risk calculator rules.
    -   Import agent information from the SentinelOne product into your ServiceNow AI Platform® with the [Service Graph Connector for Sentinel One](https://servicenow-staging.fluidtopics.net/access?context=sgc-sentinelone-integration&family=xanadu&ft:locale=en-US).
    -   Import asset data from the Splunk product into your ServiceNow AI Platform® with the [Service Graph Connector for Splunk](https://servicenow-staging.fluidtopics.net/access?context=sgc-splunk-integration&family=xanadu&ft:locale=en-US).
-   **[Enhancements to custom insights in the Security Posture Control Workspace](https://servicenow-staging.fluidtopics.net/access?context=spc-custom-insight-overview&family=xanadu&ft:locale=en-US)**

The name of the Custom insights module has been changed to the Configured insights module in the Security Posture Control Workspace.

You must assign groups to organize your reports by categories when you create custom insight records. Groups determine where your data visualizations are displayed on the dashboard in the Configured insights module according to the criteria you set.

-   **[Enhancements to the Condition policy builder in the Policies and findings module](https://servicenow-staging.fluidtopics.net/access?context=spc-create-policy&family=xanadu&ft:locale=en-US)**

Select **With aggregated data** for **Connection** to ensure that your policy matches assets that have slight variations in reported data. The following properties for policies for hardware assets are supported as they’re reported by different sources:

    -   Host name
    -   FQDN
    -   OS
    -   OS Version
    -   OS Domain
    -   OS Service Pack
-   **[Test result and remediation task state transitions](https://servicenow-staging.fluidtopics.net/access?context=spc-findings-state-transition&family=xanadu&ft:locale=en-US)**

Enhancements to policy audits ensure that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://servicenow-staging.fluidtopics.net/access?context=spc-creating-sgc-template&family=yokohama&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

**Note:** You must install [Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US) of the Now Assist for Vulnerability Response application to have access to the generative AI skill for the Connector builder framework. See the [Now Assist for Security Incident Response release notes](https://servicenow-staging.fluidtopics.net/access?context=secops-now-assist-security-operations-rn&family=yokohama&ft:locale=en-US) and [Supporting information](https://servicenow-staging.fluidtopics.net/access?context=supporting-information-now-assist-vr&family=yokohama&ft:locale=en-US) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://servicenow-staging.fluidtopics.net/access?context=spc-policies-overview&family=yokohama&ft:locale=en-US)**

Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7
-   **[SentinelOne integration for mitigation controls monitoring](https://servicenow-staging.fluidtopics.net/access?context=spc-controls-policies-for-edr&family=yokohama&ft:locale=en-US)**

You can import SentinelOne mitigation controls data with this integration to help you detect which mitigation controls are on your assets. Use this integration with the asset and software data that you import with the SentinelOne Service Graph Connector to help you monitor your security tool coverage on your enterprise assets.

-   **[Netskope](https://servicenow-staging.fluidtopics.net/access?context=sgc-netskope-integration&family=yokohama&ft:locale=en-US)**

This product pulls in asset inventory data for hardware and software from the Netskope database into the ServiceNow Configuration Management Database \(CMDB\) application.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://servicenow-staging.fluidtopics.net/access?context=spc-creating-sgc-template&family=zurich&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

**Note:** You must install Zurich Patch 4 of the Now Assist for Vulnerability Response application to have access to the generative AI skill for the Connector builder framework. See the [Now Assist for Security Incident Response \(SIR\) release notes](https://servicenow-staging.fluidtopics.net/access?context=secops-now-assist-security-operations-rn&family=zurich&ft:locale=en-US) and [Supporting information](https://servicenow-staging.fluidtopics.net/access?context=supporting-information-now-assist-vr&family=zurich&ft:locale=en-US) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://servicenow-staging.fluidtopics.net/access?context=spc-policies-overview&family=zurich&ft:locale=en-US)**

Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Security Posture Control features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Security Posture Control relies on data from service graph connectors that is populated in the CMDB 360 Data \[cmdb\_multisource\_data\] table. This data is populated only when the glide.identification\_engine.multisource\_enabled system property is set to true. You must have the cmdb\_ms\_admin role to modify property values. To set the property, navigate to **All** &gt; **Configuration** &gt; **CMDB 360 Properties**.
-   The labels on the form view for the mitigation control details record associated with vulnerable item records \(VITs\) have been enhanced for more clarity. These updates make the interface more user-friendly by expanding abbreviations on the form view, such as changing "EDR" to "Endpoint Protection."

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Security Posture Control features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Security Posture Control features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Security Posture Control.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Security Posture Control by requesting the required applications from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Security Posture Control we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Security Posture Control we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Security Posture Control, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Security Posture Control we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Security Posture Control we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.
-   Search for assets based on queries that you create for data from a wide variety of supported API integrations \(service graph connectors\) or ServiceNow products.
-   Create custom insights and monitor important metrics from a dashboard. Report on your overall security posture to IT, IT and security managers, and other key stakeholders.
-   Identify priority vulnerabilities and drive resolution through insights from Security Posture Control in Vulnerability Response risk calculators and remediation target rules.
-   Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured with Mitigation Controls Monitoring.
-   Automate remediation workflows for security gaps by publishing findings from Security Posture Control policies in the ServiceNow® Configuration Compliance application.

 See [Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [Now Assist for Security Incident Response release notes](https://servicenow-staging.fluidtopics.net/access?context=secops-now-assist-security-operations-rn&family=yokohama&ft:locale=en-US) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

 See [Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [Now Assist for Security Incident Response \(SIR\) release notes](https://servicenow-staging.fluidtopics.net/access?context=secops-now-assist-security-operations-rn&family=zurich&ft:locale=en-US) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

 See [Security Posture Control](https://servicenow-staging.fluidtopics.net/access?context=spc-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

