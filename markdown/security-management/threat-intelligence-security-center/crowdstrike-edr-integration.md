---
title: CrowdStrike Falcon EDR integration
description: Configure CrowdStrike Falcon EDR integration to enable continuous endpoint monitoring and receive real-time security alerts based on Threat Intelligence data from TISC.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/crowdstrike-edr-integration.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-08-15"
reading_time_minutes: 1
keywords: [crowdstrike, edr, falcon, tisc integrations]
breadcrumb: [TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# CrowdStrike Falcon EDR integration

Configure CrowdStrike Falcon EDR integration to enable continuous endpoint monitoring and receive real-time security alerts based on Threat Intelligence data from TISC.

Use the CrowdStrike Falcon EDR integration to add observables from TISC to a watchlist that monitors for security events and generates alerts. You add observables as part of enrichment during an investigation.

The integration supports the Domain, IPv4, IPv6, MD5, and SHA256 observable types. Observables that are marked as AllowList aren't sent.

When you send an observable, you select the action that CrowdStrike EDR applies to it: no action, detection only, block, or block with the detection hidden. The block actions apply only to the MD5 and SHA256 observable types.

Each observable is sent with an expiration. You configure whether the expiration comes from the observable in TISC or from the expiration period that is configured for the observable type.

The IOC source that is recorded in CrowdStrike for observables sent from TISC is `TISC Intelligence`.

-   **[Configure Crowdstrike Falcon EDR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/config-cs-edr-integration.md)**  
Download and configure the CrowdStrike Falcon EDR integration to enable endpoint detection and response capabilities in your ServiceNow instance.
-   **[Send observables to EDR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/send-to-edr.md)**  
Send observables to the EDR security tool.

**Parent Topic:**[TISC Security Tools integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-edr-integrations.md)

