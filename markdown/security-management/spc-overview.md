---
title: Exploring Security Posture Control
description: Security Posture Control enables cybersecurity teams to get visibility into their complete enterprise asset inventory and determine their overall security posture.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-08-18"
reading_time_minutes: 4
breadcrumb: [Security Posture Control, Security Operations]
---

# Exploring Security Posture Control

Security Posture Control enables cybersecurity teams to get visibility into their complete enterprise asset inventory and determine their overall security posture.

Security analysts gain insights into how well security tools are deployed and covering their assets based on their asset inventory and imported data from service graph connectors and ServiceNow products such as Hardware Asset Management \(HAM\) and ITOM Discovery.

Security analysts can also create custom policies and configure insights to monitor the compliance of assets with internal security standards. Vulnerability managers can use insights from Security Posture Control \(SPC\) to prioritize remediation of vulnerabilities on high-risk assets.

The SPC product is based on Cloud Security Posture Management \(CSPM\) and Cyber Asset Hygiene Management \(CAHM\). Security Posture Control consists of two applications that are available by separate subscription from the ServiceNow® Store.

<table id="id_o2h_qpf_gbc"><thead><tr><th>

Release version

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Security Posture Control Core: v6.2, v6.1, v6.0.

</td><td>

For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498)

[Security Posture Control release notes](https://www.servicenow.com/docs/access?context=secops-security-posture-control-rn&version=xanadu&pubname=xanadu-release-notes&ft:locale=en-US)

</td></tr><tr><td>

Asset Security Posture Management: v5.3, v5.1, v5.0

</td><td>

 

</td></tr><tr><td>

Mitigation Controls Monitoring v4.0, v3.0, v2.0

</td><td>

 

</td></tr></tbody>
</table>Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

With the SPC product, Info-Sec teams can perform the following tasks:

-   View security posture insights for your on-premise and cloud assets. SPC helps your Info-Sec teams identify assets that are missing endpoint protection, unmanaged assets, assets exposed to the internet, and any high-risk combinations involving vulnerabilities.
-   Monitor your assets for their compliance with internal security tool configuration standards. For example, ensure that the latest version of an endpoint protection product is being used.
-   Automate your remediation workflow for the security posture gaps you find with the ServiceNow Configuration Compliance application.
-   Create custom policies and insights based on asset metadata, security tool coverage data, and vulnerability data.
-   Gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured with [Mitigation Controls Monitoring](spc-mitigation-exploring.md).

## How Asset Security Posture Management works

![How it works workflow](../image/spc-How-it-works-1.png)

Asset Security Posture Management \(ASPM\) identifies security tool coverage gaps in assets by using API integrations with various third-party tools \(Service Graph Connectors\) along with ServiceNow products.

ASPM relies on data populated in your CMDB about your assets. The asset data is imported by various categories of monitoring tools and compared to identify any potential security gaps.

For example, say there is asset data populated in the CMDB that is reported by tools that cover infrastructure monitoring and networking tools. However, this data for those same assets is not populated or reported by endpoint protection tools. If you compare the asset data reported by these different tools you can see that there are assets missing an endpoint protection agent.

Asset Security Posture Management identifies security tool coverage gaps in assets by using API integrations with various tools \(Service Graph Connectors\) and ServiceNow products. Categories include but are not limited to the following:

-   Digital Employee Experience
-   Discovery
-   Endpoint Management
-   IT Asset Management
-   Infrastructure Monitoring 
-   Networking
-   Network Security
-   Network Performance Monitoring
-   Configuration and Patch Management  
-   Endpoint Protection
-   Cloud Provider
-   Application Performance Monitoring
-   Directory Services
-   Vulnerability Assessment

## The Security Posture Control workflow

Identifying security tool gaps involves the following steps:

1.  Set up and activate API connections with any of the tools that you are using in various categories. You can use Service Graph Connectors for products that are available from the ServiceNow Store for the API connections that are required. For more information about the supported service graph connectors, see [Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-sgc-available&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Supported service graph connectors are available from the ServiceNow® Store with separate subscriptions.
2.  Activate the policies shipped with the Security Posture Control application. The Security Posture Control product finds security tool gaps by performing the following tasks:
    1.  Identifies the list of all unique assets populated by various Service Graph Connectors in the CMDB.
    2.  Identifies assets that are not reported by specific categories from this asset pool, for example, Endpoint Protection. Assets are identified based on the active policy that is being evaluated.
    3.  Assets identified as not reported by specific categories are reported as ‘Findings’ or ‘Test Results’ in the Configuration Compliance application.
3.  Automatically assign ‘Findings’ to different teams for remediation with the Configuration Compliance application.

## High-risk combinations

With Asset Security Posture Management, you can also identify assets that have high-risk combinations. An example of a high-risk combination might show assets that are missing security tools, have critical vulnerabilities, and are exposed to the internet.

Some of the policies shipped with the Security Posture Control application look for these high-risk combinations of critical vulnerabilities and security tool coverage gaps. However, for these combination policies to work, you must have the Vulnerability Response application and at least one vulnerability scanner integration product such as Qualys, Rapid7, or the Tenable Vulnerability Integration application installed. These applications are available with separate subscriptions from the ServiceNow Store.

## Mitigation Controls Monitoring

From within in the Security Posture Control \(SPC\) Workspace, gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured. See [Mitigation Controls Monitoring](spc-mitigation-exploring.md) for more information.

