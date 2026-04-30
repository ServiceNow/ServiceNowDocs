---
title: Security Posture Control release notes
description: The ServiceNow Security Posture Control application provides cybersecurity teams with visibility into security tool coverage gaps and deviations from security tool configuration for their enterprise assets. Security Posture Control was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-01"
reading_time_minutes: 3
---

# Security Posture Control release notes

The ServiceNow® Security Posture Control application provides cybersecurity teams with visibility into security tool coverage gaps and deviations from security tool configuration for their enterprise assets. Security Posture Control was enhanced and updated in the Xanadu release.

## Security Posture Control highlights for the Xanadu release

-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.
-   Search for assets based on queries that you create for data from a wide variety of supported API integrations \(service graph connectors\) or ServiceNow products.
-   Create custom insights and monitor important metrics from a dashboard. Report on your overall security posture to IT, IT and security managers, and other key stakeholders.
-   Identify priority vulnerabilities and drive resolution through insights from Security Posture Control in Vulnerability Response risk calculators and remediation target rules.
-   Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured with Mitigation Controls Monitoring.
-   Automate remediation workflows for security gaps by publishing findings from Security Posture Control policies in the ServiceNow® Configuration Compliance application.

See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information.

**Important:** Security Posture Control is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Security Posture Control to Xanadu

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).

## New in the Xanadu release

-   **[Mitigation Controls Monitoring with Security Posture Control](https://www.servicenow.com/docs/access?context=spc-mitigation-exploring&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    From within the Security Posture Control workspace, detect mitigation controls of various types as described by MITRE on all on-premise and cloud enterprise assets. Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured.

    -   Activate mitigation control policies that are included with the application that identify MITRE mitigations on your assets.
    -   Identify your assets that have Web Application Firewall \(WAF\) protection with supported tools that include F5 BIG-IP. Automatically map a WAF mitigation to vulnerable items by analyzing the policy signatures in the firewall and the Common Vulnerabilities and Exposures \(CVE\) information.
    -   Identify exploit mitigation controls from endpoint protection or Endpoint Detection and Response \(EDR\) tools like CrowdStrike and Microsoft Defender. Automatically map the EDR exploit mitigation controls to relevant vulnerable items by analyzing the vulnerability information and the EDR mitigation control configuration.
    -   Populate vulnerable items with relevant attributes that can be used in your Vulnerability Response risk calculator rules.
    -   Import agent information from the SentinelOne product into your ServiceNow AI Platform® with the [Service Graph Connector for Sentinel One](https://www.servicenow.com/docs/access?context=sgc-sentinelone-integration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    -   Import asset data from the Splunk product into your ServiceNow AI Platform® with the [Service Graph Connector for Splunk](https://www.servicenow.com/docs/access?context=sgc-splunk-integration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   **[Enhancements to custom insights in the Security Posture Control Workspace](https://www.servicenow.com/docs/access?context=spc-custom-insight-overview&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The name of the Custom insights module has been changed to the Configured insights module in the Security Posture Control Workspace.

    You must assign groups to organize your reports by categories when you create custom insight records. Groups determine where your data visualizations are displayed on the dashboard in the Configured insights module according to the criteria you set.

-   **[Enhancements to the Condition policy builder in the Policies and findings module](https://www.servicenow.com/docs/access?context=spc-create-policy&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Select **With aggregated data** for **Connection** to ensure that your policy matches assets that have slight variations in reported data. The following properties for policies for hardware assets are supported as they’re reported by different sources:

    -   Host name
    -   FQDN
    -   OS
    -   OS Version
    -   OS Domain
    -   OS Service Pack
-   **[Test result and remediation task state transitions](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Enhancements to policy audits ensure that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.


## Activation information

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

