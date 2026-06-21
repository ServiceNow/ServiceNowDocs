---
title: Combined Security Posture Control release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Security Posture Control from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-securityposturecontrol-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Security Posture Control release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Security Posture Control from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Posture Control release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Posture Control to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install the supported applications for Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Security Posture Control.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Enhancements to version 3.0](https://www.servicenow.com/docs/access?context=spc-policies-overview&family=washingtondc&ft:locale=en-US)**

Policy enhancements:

    -   Edit activated policies, save changes, publish changes, and exit edit mode with UI actions in policies. Versions are tracked and version numbers are displayed on the policy records and their related test results.
    -   Close existing related test results \(findings\) if you publish a new version of a policy or delete a policy. If you choose to close test results, test result and remediation task states transition in accordance with the state transition processes of the Configuration Compliance application. See [Test result and remediation task state transitions in the Security Posture Control application](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&family=washingtondc&ft:locale=en-US) for more information.
    -   Query the Security Posture Control product with **Software** as an Entity type. Look for any discrepancies that exist between the installed software reported by your vulnerability scanner products and the software reported by scanners and already accounted for in Software Asset Management \(SAM\) and other ServiceNow® products.
Policy condition builder enhancements:

    -   Select the **OR** condition to search for and monitor diverse types of assets from a single policy.
    -   Select **Reported only by** as a Connection and choose specific Sources \(third-party service graph connectors and ServiceNow products\) to report on your assets. Monitor only those assets that are reported by the specific ServiceNow® products and third-party sources you select.
Select **CMDB metadata** as a Connection in the condition builder and search for the following assets:

    -   Devices with host names that have specific patterns with **matches regex** operator for the host name Property. For example, if you enter `lp` manually, you can look for all laptops with 'lp' as the second and third characters in the host name.
    -   Assets that have been discovered for the first time with the **First seen** timestamp Property.
    -   Devices based on specific models and model information with the **Model name**, **Has model info**, and **Model data** conditions. This data can help you with security control coverage.
    -   Assets that were **Last seen** **Within the last n days**. Enter the number of days up to **30**. For example, enter **3** to monitor assets by 'last logon' from Active Directory in the last three days.
-   **[Policies \(prior to version 3.0\)](https://www.servicenow.com/docs/access?context=spc-policies-overview&family=washingtondc&ft:locale=en-US)**

Monitor your assets and cloud assets \(AWS only\) for missing endpoint protection agents, unmanaged devices, devices not scanned for vulnerabilities, and critical combinations with vulnerabilities with provided policies.

    -   Define custom policies based on asset metadata, security tool configuration data, and vulnerabilities to monitor asset compliance with your internal security standards.
    -   Chain policies together so you can monitor assets in hierarchical categories.
    -   Filter assets by using custom fields in your CMDB CI classes in policies.
    -   Exclude assets from your audits and monitoring that match other policies or assets with approved exceptions in Integrated Risk Management \(IRM\).
-   **[Service Graph Connectors](https://www.servicenow.com/docs/access?context=spc-use-connectors-policies&family=washingtondc&ft:locale=en-US)**

The application supports 31 Service Graph Connectors for various security and IT tools in the enterprise to import and consolidate asset data to provide you insights on your security posture.

-   **[Key insights and custom insights](https://www.servicenow.com/docs/access?context=spc-custom-insight-overview&family=washingtondc&ft:locale=en-US)**

Monitor critical metrics about your asset security posture and security tool coverage by creating custom insights.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Mitigation Controls Monitoring with Security Posture Control](https://www.servicenow.com/docs/access?context=spc-mitigation-exploring&family=xanadu&ft:locale=en-US)**

From within the Security Posture Control workspace, detect mitigation controls of various types as described by MITRE on all on-premise and cloud enterprise assets. Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured.

    -   Activate mitigation control policies that are included with the application that identify MITRE mitigations on your assets.
    -   Identify your assets that have Web Application Firewall \(WAF\) protection with supported tools that include F5 BIG-IP. Automatically map a WAF mitigation to vulnerable items by analyzing the policy signatures in the firewall and the Common Vulnerabilities and Exposures \(CVE\) information.
    -   Identify exploit mitigation controls from endpoint protection or Endpoint Detection and Response \(EDR\) tools like CrowdStrike and Microsoft Defender. Automatically map the EDR exploit mitigation controls to relevant vulnerable items by analyzing the vulnerability information and the EDR mitigation control configuration.
    -   Populate vulnerable items with relevant attributes that can be used in your Vulnerability Response risk calculator rules.
    -   Import agent information from the SentinelOne product into your ServiceNow AI Platform® with the [Service Graph Connector for Sentinel One](https://www.servicenow.com/docs/access?context=sgc-sentinelone-integration&family=xanadu&ft:locale=en-US).
    -   Import asset data from the Splunk product into your ServiceNow AI Platform® with the [Service Graph Connector for Splunk](https://www.servicenow.com/docs/access?context=sgc-splunk-integration&family=xanadu&ft:locale=en-US).
-   **[Enhancements to custom insights in the Security Posture Control Workspace](https://www.servicenow.com/docs/access?context=spc-custom-insight-overview&family=xanadu&ft:locale=en-US)**

The name of the Custom insights module has been changed to the Configured insights module in the Security Posture Control Workspace.

You must assign groups to organize your reports by categories when you create custom insight records. Groups determine where your data visualizations are displayed on the dashboard in the Configured insights module according to the criteria you set.

-   **[Enhancements to the Condition policy builder in the Policies and findings module](https://www.servicenow.com/docs/access?context=spc-create-policy&family=xanadu&ft:locale=en-US)**

Select **With aggregated data** for **Connection** to ensure that your policy matches assets that have slight variations in reported data. The following properties for policies for hardware assets are supported as they’re reported by different sources:

    -   Host name
    -   FQDN
    -   OS
    -   OS Version
    -   OS Domain
    -   OS Service Pack
-   **[Test result and remediation task state transitions](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&family=xanadu&ft:locale=en-US)**

Enhancements to policy audits ensure that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://www.servicenow.com/docs/access?context=spc-creating-sgc-template&family=yokohama&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

**Note:** You must install [Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US) of the Now Assist for Vulnerability Response application to have access to the generative AI skill for the Connector builder framework. See the [Now Assist for Security Incident Response release notes](https://www.servicenow.com/docs/access?context=secops-now-assist-security-operations-rn&family=yokohama&ft:locale=en-US) and [Supporting information](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&family=yokohama&ft:locale=en-US) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://www.servicenow.com/docs/access?context=spc-policies-overview&family=yokohama&ft:locale=en-US)**

Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7
-   **[SentinelOne integration for mitigation controls monitoring](https://www.servicenow.com/docs/access?context=spc-controls-policies-for-edr&family=yokohama&ft:locale=en-US)**

You can import SentinelOne mitigation controls data with this integration to help you detect which mitigation controls are on your assets. Use this integration with the asset and software data that you import with the SentinelOne Service Graph Connector to help you monitor your security tool coverage on your enterprise assets.

-   **[Netskope](https://www.servicenow.com/docs/access?context=sgc-netskope-integration&family=yokohama&ft:locale=en-US)**

This product pulls in asset inventory data for hardware and software from the Netskope database into the ServiceNow Configuration Management Database \(CMDB\) application.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://www.servicenow.com/docs/access?context=spc-creating-sgc-template&family=zurich&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

**Note:** You must install Zurich Patch 4 of the Now Assist for Vulnerability Response application to have access to the generative AI skill for the Connector builder framework. See the [Now Assist for Security Incident Response \(SIR\) release notes](https://www.servicenow.com/docs/access?context=secops-now-assist-security-operations-rn&family=zurich&ft:locale=en-US) and [Supporting information](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&family=zurich&ft:locale=en-US) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://www.servicenow.com/docs/access?context=spc-policies-overview&family=zurich&ft:locale=en-US)**

Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Security Posture Control features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Security Posture Control features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Security Posture Control features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

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

Washington DC

</td><td>

Install the Security Posture Control Core, Asset Security Posture Management \(ASPM\), and the Configuration Compliance applications for Security Posture Control by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Security Posture Control by requesting the required applications from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Security Posture Control we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Security Posture Control we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Australia

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

Washington DC

</td><td>

-   Use the policies included with the application or create your own policies to audit and monitor assets for security tool coverage, compliance with internal configuration standards for security tools, critical combinations involving vulnerabilities, and possible internet exposure.
-   Search for assets in your CMDB based on queries for specific service graph connector and ServiceNow products or for assets that have specific data. You can save your search criteria as a policy.
-   Create custom insights on a dashboard and monitor important metrics for your asset security posture.
-   Identify priority vulnerabilities and drive resolution through insights from Security Posture Control in Vulnerability Response risk calculators and remediation target rules.
-   Automate remediation workflows for security gaps by publishing findings from Security Posture Control policies into Configuration Compliance.

 See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-overview&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.
-   Search for assets based on queries that you create for data from a wide variety of supported API integrations \(service graph connectors\) or ServiceNow products.
-   Create custom insights and monitor important metrics from a dashboard. Report on your overall security posture to IT, IT and security managers, and other key stakeholders.
-   Identify priority vulnerabilities and drive resolution through insights from Security Posture Control in Vulnerability Response risk calculators and remediation target rules.
-   Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured with Mitigation Controls Monitoring.
-   Automate remediation workflows for security gaps by publishing findings from Security Posture Control policies in the ServiceNow® Configuration Compliance application.

 See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [Now Assist for Security Incident Response release notes](https://www.servicenow.com/docs/access?context=secops-now-assist-security-operations-rn&family=yokohama&ft:locale=en-US) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

 See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [Now Assist for Security Incident Response \(SIR\) release notes](https://www.servicenow.com/docs/access?context=secops-now-assist-security-operations-rn&family=zurich&ft:locale=en-US) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

 See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

