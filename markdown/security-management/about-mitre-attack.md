---
title: MITRE-ATT&amp;CK framework overview
description: The MITRE-ATT&amp;CK framework is a knowledge base of common tactics, techniques, and procedures \(TTP\) that your organization can access to develop specific threat models and methodologies against cyberattacks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MITRE-ATT&amp;CK framework overview

The MITRE-ATT&amp;CK framework is a knowledge base of common tactics, techniques, and procedures \(TTP\) that your organization can access to develop specific threat models and methodologies against cyberattacks.

## Overview

The MITRE Adversarial Tactics, Techniques, and Common Knowledge \(ATT&amp;CK\) framework documents and tracks various adversarial techniques that are used during different stages of a cyberattack.

By using the MITRE-ATT&amp;CK framework's knowledge base, the cyberthreat intelligence community can quickly identify threats and coordinate cyberattack responses.

## MITRE-ATT&amp;CK and Security Operations

See the following diagram to learn how the MITRE-ATT&amp;CK information flows with Security Operations applications.

![How MITRE ATT&CK works with Security Operations' applications.](../image/mitre-attack-architecture.png)

-   The [pre-loaded TAXII client](../task/setup-mitre-profile.md) connects to the TAXII server to ingest the [data collections](../task/view-mitre-collection.md) to Threat Intelligence.
-   Existing [Security Information and Event Manager \(SIEM\) integrations](auto-extract-technique-rules.md#) ingest their threat data \(alerts and events\), with relevant TTPs and are [associated with security incidents](../task/associate-mitre-with-sir.md#).
-   When an [IoC is associated to a security incident](../task/associate-mitre-observables.md), Threat Intelligence automatically searches threat feeds for relevant information and sends IoCs to third-party sources such as EDR, Sandbox, or TIP for additional analysis.
-   If any third-party source contains the MITRE-ATT&amp;CK information, then [Threat Intelligence extracts the technique information](../task/create-detection-rules.md) and enriches the data in the Threat Intelligence repository for correlation and analysis.
-   MITRE-ATT&amp;CK also shares [CVE context information](mitre-att-ck-heatmap-and-navigator.md#) for each technique. Your security team can review the exploited techniques in Vulnerability Response to determine if your business-critical assets are threatened.

## MITRE-ATT&amp;CK matrices, tactics, and techniques

The core of the MITRE-ATT&amp;CK framework is a matrix of adversary tactics and techniques. The sequence of the tactics represents what an adversary is trying to accomplish at the stage of an incident. When your security team understands this sequence, you have an opportunity to anticipate an adversary's next move and break the kill chain. ATT&amp;CK consists of the following matrices:

-   Enterprise ATT&amp;CK: Describes the behaviors and actions that an adversary takes to compromise and operate in an enterprise network and cloud.

    **Note:** The Pre ATT&amp;CK matrix has been deprecated by MITRE and is merged with the Enterprise matrix.

-   ICS ATT&amp;CK: Describes the actions that an adversary takes while operating within an Industrial Control Systems \(ICS\) network.
-   Mobile ATT&amp;CK: Describes the adversary behaviors and actions that focus on mobile devices.

Tactics represent the why of an ATT&amp;CK technique. It is the adversary’s tactical objective for performing an action.

Techniques represent how an adversary achieves a tactical objective by performing an action.

Techniques may be associated with more than one tactic. For example, Access Token Manipulation is used by an adversary to achieve either the tactic of Privilege Escalation or Defense Evasion.

## Using an intent-based approach for incident responses

An intent-based response uses a dynamic and contextual kill chain framework that can help your organization to correlate security incidents and to identify a large scope of attacks. Your security team can use an intent-based response to understand how the organization is being attacked and what the attacker might do next. This type of response enables you to predict an attacker's behavior so that you can focus your resources effectively.

Using Security Incident Response, your security team can manage the life cycle of each security incident from analysis to containment by focusing on indicators of compromise \(IOCs\) like IP addresses, file hashes, and domains.

By integrating Security Incident Response with the MITRE-ATT&amp;CK framework, security incidents are handled as links in a larger enterprise-wide attack.

## How your organization can benefit from MITRE-ATT&amp;CK in Security Operations

![Benefits of using MITRE ATT&CK](../image/mitre-attack-architecture_benefits.png)

Using the MITRE-ATT&amp;CK framework can help your organization do the following:

-   Equip security analysts with MITRE-ATT&amp;CK tactics, techniques, and procedures \(TTPs\) to better analyze and respond to security incidents.
-   Automate the incident workflows using the playbook for detecting and containing threats in the context of the MITRE-ATT&amp;CK framework.
-   Prioritize indicators of compromise and threat hunting with MITRE-ATT&amp;CK information.
-   Understand the high-level security posture of your organization in the context of the MITRE-ATT&amp;CK framework.

-   **[MITRE-ATT&amp;CK administration](mitre-att-ck-administration.md)**  
You can set up, map data sources, map overall technique detection coverage, and maintain the MITRE-ATT&amp;CK repository in the ServiceNow AI Platform.
-   **[Using MITRE-ATT&amp;CK to detect and analyze threats](mitre-att-ck-features.md)**  
Use the MITRE-ATT&amp;CK framework across the Threat Intelligence and the SIR module to detect and analyze threats to your organization.

**Parent Topic:**[Threat Intelligence](../reference/threat-intel-landing-page.md)

**Related topics**  


[Understanding Threat Intelligence](understanding-threat-intel.md)

[Set up Threat Intelligence](c_GetStartedWithThreatIntel.md#)

[IoC Repository](ioc-repository.md)

[MITRE DEFEND Framework](mitre-d3fend-framework.md)

[Threat Intelligence administration](../reference/r_ThreatRespAdmin.md)

[Threat Intelligence integrations](threat-intelligence-integrations.md)

[Threat Intelligence Orchestration](../../threat-intelligence-orchestration/concept/c_ThreatIntelligenceOrchestration.md)

[Security Case Management](../../threat-intelligence-case-management/concept/case-mgmt.md)

