---
title: Unified experience capabilities and modal screens
description: The following table below describes the capabilities and applicable screens.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Unified experience framework, SIR Workspace Orchestration, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Unified experience capabilities and modal screens

The following table below describes the capabilities and applicable screens.

<table id="simpletable_jty_xt1_dwb"><thead><tr><th>

Capability

</th><th>

UX frameworks screens applicable

</th><th>

Integrations supported

</th></tr></thead><tbody><tr><td>

Run Threat Look Up

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for Run Threat Look Up.

So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

-   Virus Total
-   Hybrid Analysis
-   Security Incident Response Integration with Zscaler
-   Phistank
-   Metadefender
-   Threatcrowd
-   Have I Been Pawned?
-   Crowd Strike Falcon Intelligence

</td></tr><tr><td>

Run Observable Enrichment

</td><td>

Only Screen 1 – Select Implementations is applicable There are no common inputs or implementation specific inputs applicable for Run Observable Enrichment.

So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

-   MISP
-   Microsoft Defender Endpoint
-   Shodan
-   RiskIQ
-   WHOIS
-   Reverse WHOIS

</td></tr><tr><td>

Run Sighting Search/Run Web Sighting Search/Run Email Sighting Search

</td><td>

Screen 1 – **Select Implementations** and Screen 2 – **Common Inputs** are applicable.Sighting search takes date and time frequency as common inputs across multiple implementations of Splunk and other integrations.

This screen will be presented to the Security Analyst to capture date and time frequencies.

For integrations that don’t require these inputs, for example FireEye HX, they will be ignored. After selecting one or more implementations and providing common inputs, the Security Analyst will be able to submit the action.

</td><td>

-   Splunk-incident Enrichment
-   Carbon Black
-   Elastic search
-   FireEye HX
-   McaFee ESM
-   MSFT Defender for endpoint
-   Splunk Sighting
-   Qradar sighting search
-   MISP

</td></tr><tr><td>

Submit to Sandbox

</td><td>

Screen 1 – Select Implementations and Screen 3 – Implementation specific inputs are applicable.Submit to Sandbox takes different inputs for different implementations. There are no common inputs for this capability currently.

For example, when the Analyst selects Crowdstrike Falcon X Quick Scan, Crowdstrike Falcon X Windows 64, Crowdstrike Falcon X Linux, and Zscaler, the inputs vary. Crowdstrike Falcon X Quick scan and Zscaler don’t need further run time inputs. Crowdstrike Falcon X Windows 64 takes optional run time inputs that differs from Crowdstrike Falcon X Linux. So, these can be provided in screen 3 specifically against individual selected implementations as applicable.

</td><td>

-   CrowdStrike Falcon X Sandbox Integration
-   Security Incident Response Integration with Zscaler

</td></tr><tr><td>

Publish to Watchlist

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for **Publish to Watchlist**.

So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

Crowdstrike Falcon Host

</td></tr><tr><td>

Allow/Block Request

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for **Allow/Block Request**.

So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

-   Palo Alto Network NGFW
-   Check Point NGFW
-   Security Incident Response Integration with Zscaler

</td></tr><tr><td>

Get Host Details

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for Get Host Details.

So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

-   FireEye HX
-   Microsoft Defender for Endpoint

</td></tr><tr><td>

Get File

</td><td>

Screen 1 – Select Implementations and Screen 2 – Common Inputs are applicable.Get File takes file name, path as common inputs. After selecting one or more implementations and providing common inputs, the Security Analyst will be able to submit the action.

</td><td>

FireEye HX

</td></tr><tr><td>

Get Network Statistics

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for Get Network Statistics. So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

-   FireEye HX
-   NetStat

</td></tr><tr><td>

Get Running Processes

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for Get Running Processes.

So, only screen 1 is presented to the Security Analyst to select one or more implementations. After selecting the implementations, the Security Analyst will be able to submit the action.

</td><td>

-   FireEye HX
-   Carbon Black
-   System Command

</td></tr><tr><td>

Get Running Services

</td><td>

Only Screen 1 – Select Implementations is applicable.There are no common inputs or implementation specific inputs applicable for Get Running Services.

 So, only screen 1 is presented to the Analyst to select one or more implementations. After selecting the implementations, the Analyst will be able to submit the action.

</td><td>

FireEye HX

</td></tr><tr><td>

Isolate Host / Un-Isolate Host

</td><td>

Screen 1 – Select Implementations and Screen 3 – Implementation specific inputs are applicable.Isolate Host/Un-isolate Host takes different inputs for different implementations.

There are no common inputs for this capability currently. For example, when the Analyst selects FireEye HX and Microsoft Defender for Endpoint, the inputs vary.

FireEye HX doesn’t need run time inputs. On the other hand Microsoft Defender takes inputs such as Isolation Type and Comments.

So, these can be provided in screen 3 specifically against individual selected implementations as applicable.

</td><td>

-   FireEye HX
-   Microsoft Defender Endpoint
-   Carbon Black

</td></tr><tr><td>

Run Additional Actions

</td><td>

Screen 1 – Select Implementations and Screen 3 – Implementation specific inputs are applicable.Run Additional Actions Host takes different inputs for different implementations. There are no common inputs for this capability currently.

For example, when the Analyst selects FireEye HX Standard Investigative Details Script, FireEye HX Triage Acquisition and Crowdstrike Falcon Insight reg unload, the inputs vary.

FireEye HX Standard Investigative Details Script and FireEye HX Triage Acquisition take Comments as the input that could be different for both. Crowdstrike Falcon Insight reg unload takes Subkey as the input.

So, these can be provided in screen 3 specifically against individual selected implementations as applicable.

**Note:** Currently supports only single selection of implementation. In future releases multi selection of implementation will be supported.

</td><td>

-   FireEye HX
-   Microsoft Defender for Endpoint
-   Crowdstrike Falcon Insight

</td></tr></tbody>
</table>**Parent Topic:**[Unified experience framework for integrations powered by Capability Framework](../concept/security-incident-response-workspace-capability-framework.md)

