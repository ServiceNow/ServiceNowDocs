---
title: Security Incident Response integrations
description: Security Incident Response \(SIR\) integrates with third-party security tools to create security incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/sir\_integrations.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response integrations

Security Incident Response \(SIR\) integrates with third-party security tools to create security incidents.

## How integrations work

1.  Third-party tools \(SIEM, EDR, email security, and threat intelligence\) send events, alerts, incidents, or offenses to ServiceNow.
2.  Ingestion profiles map source fields to Security Incident \[sn\_si\_incident\] fields and filter out low-value events.
3.  Matching events create or aggregate to a security incident; enrichment integrations add sighting and threat context.
4.  Analysts run response actions \(isolate host, block value, sandbox a file\) and, where supported, updates sync back bi-directionally.

## Available integrations

|Integration|Vendor|Use case|ServiceNow Store|
|-----------|------|--------|----------------|
|**Ingest events, alerts, incidents, and findings**|
|[Micro Focus ArcSight ESM Event Ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/arcsight-esm.md)|OpenText|Ingest correlated events on a schedule to automatically create security incidents, with bi-directional updates.|[View in Store](https://store.servicenow.com/store/app/753aafe21b246a50a85b16db234bcb05)|
|[AWS Security Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/aws-security-hub-integration.md)|Amazon Web Services|Ingest Security Hub findings to auto-create security incidents, with bi-directional status and work-note sync.|[View in Store](https://store.servicenow.com/store/app/d049a7ae1be06a50a85b16db234bcb7f)|
|[Palo Alto Cortex XSIAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/cortex-xsiam-siem.md)|Palo Alto Networks|Ingest XSIAM alerts and incidents into SIR with bi-directional status and worknote synchronization.|[View in Store](https://store.servicenow.com/store/app/5fa1baf447f53a142ec7c1c4f16d439e)|
|[Microsoft Sentinel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/microsoft-azure-sentinel-integration.md)|Microsoft|Ingest Sentinel incidents to auto-create security incidents. Migrate to Defender before Azure portal deprecation \(Mar 2027\).|[View in Store](https://store.servicenow.com/store/app/093bab2a1b246a50a85b16db234bcb97)|
|[Microsoft Defender](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ms-defender.md)|Microsoft|Ingest Defender alerts and incidents for centralized case management with bi-directional sync.|[View in Store](https://store.servicenow.com/store/app/03ec7f8697633250cbe2f5411153af56)|
|[Microsoft Graph Security API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ms-graph-about.md)|Microsoft|Ingest alerts from multiple Microsoft security providers through one Graph interface to auto-create incidents.|[View in Store](https://store.servicenow.com/store/app/71cbe7ea1b246a50a85b16db234bcb9f)|
|[IBM QRadar Offense Ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/qradar-ibm.md)|IBM|Fetch QRadar offenses and convert them into security incidents with automated response actions.|[View in Store](https://store.servicenow.com/store/app/0f19ab6e1be06a50a85b16db234bcb6c)|
|[Secureworks CTP Ticket Ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/secureworks-ctp-about.md)|Secureworks|Fetch Secureworks tickets on a schedule, convert them into security incidents, and sync worklogs.|[View in Store](https://store.servicenow.com/store/app/6c4e236a1b646a50a85b16db234bcb2a)|
|[ServiceNow SecOps Add-on for Splunk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/secops-integration-with-splunk.md)|Splunk|Let a Splunk administrator collect data and create incidents and events in ServiceNow.|[View on Splunkbase](https://splunkbase.splunk.com/app/3921)|
|[Proofpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/proofpoint-integration-secops-landing.md)|Proofpoint|Ingest Proofpoint events; SIR creates an incident per event for analysts to review or work on.|[View in Store](https://store.servicenow.com/store/app/974de7e21b646a50a85b16db234bcb70)|
|**Endpoint detection and response \(EDR\)**|
|[Carbon Black](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/carbon-black-landing-page.md)|Broadcom|Query and interact with endpoints tied to a security incident for investigation and response.|[View in Store](https://store.servicenow.com/store/app/a7cb6bea1b246a50a85b16db234bcb6e)|
|[CrowdStrike Falcon Insight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/CrowdStrike-Falcon-Insight-for-Security-Operations-integration.md)|CrowdStrike|Gather host details and run real-time remediation actions on endpoints from SIR.|[View in Store](https://store.servicenow.com/store/app/fafcaf621b646a50a85b16db234bcba9)|
|[FireEye Endpoint Security \(HX\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/fireye-overview.md)|Trellix|Investigate and remediate endpoints: enrichment, containment, and Enterprise Security Search.|[View in Store](https://store.servicenow.com/store/app/780c6b2e1b246a50a85b16db234bcbf1)|
|[Microsoft Defender for Endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/microsoft-defender-for-endpoint-integration.md)|Microsoft|Enrich hosts and run response actions such as isolate host, AV scan, and restrict app execution.|[View in Store](https://store.servicenow.com/store/app/bbf9eba21b246a50a85b16db234bcb7b)|
|**Incident enrichment and sightings search**|
|[Carbon Black – Incident Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/carbon-blk-inc-enrich-landing-page.md)|Broadcom|Query endpoints tied to a security incident to add investigation context.|[View in Store](https://store.servicenow.com/store/app/a7cb6bea1b246a50a85b16db234bcb6e#linksAndDocuments)|
|[Elasticsearch – Incident Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/elasticsearch-landing-page.md)|Elastic|Search your logs and add relevant sighting information to security incidents.|[View in Store](https://store.servicenow.com/store/app/4d6c27ae1b246a50a85b16db234bcbea)|
|[HPE ArcSight Logger – Incident Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/arcsight-logger-landing-page.md)|OpenText|Search your logs and add relevant sighting information to security incidents.|[View in Store](https://store.servicenow.com/store/app/7ffaabe61b246a50a85b16db234bcb51)|
|[McAfee ESM – Incident Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcafee-esm-landing-page.md)|Trellix|Search your logs and add relevant sighting information to security incidents.|[View in Store](https://store.servicenow.com/store/app/f36b2f6a1b246a50a85b16db234bcb32)|
|[IBM QRadar – Incident Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/qradar-landing-page.md)|IBM|Search your logs and add relevant sighting information to security incidents.|[View in Store](https://store.servicenow.com/store/app/a94c6f6e1b246a50a85b16db234bcb63)|
|[Splunk – Incident Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/splunk-in-enrich-landing-page.md)|Splunk|Search your logs and add relevant sighting information to security incidents.|[View in Store](https://store.servicenow.com/store/app/f79da3661b646a50a85b16db234bcb9e)|
|**Threat intelligence and malware analysis**|
|[CrowdStrike Falcon Host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/crowdstrike-falcon-host-landing-page.md)|CrowdStrike|Push incident observables to a watchlist to generate additional alerts.|[View in Store](https://store.servicenow.com/store/app/4689e3221b246a50a85b16db234bcb19)|
|[CrowdStrike Falcon X Sandbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/crowdstrike-falcon-sandbox-overview.md)|CrowdStrike|Submit files and URLs for detailed malware and threat analysis in an isolated sandbox.|[View in Store](https://store.servicenow.com/store/app/6b69a7ee1be06a50a85b16db234bcb4d)|
|[Have I Been Pwned?](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/haveibeenpwned-landing-page.md)|Have I Been Pwned|Look up domains and email addresses to check whether data has been compromised in breaches.|[View in Store](https://store.servicenow.com/store/app/4ad8a32e1be06a50a85b16db234bcbcc)|
|[Palo Alto Networks AutoFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/palo-alto-autofocus-landing-page.md)|Palo Alto Networks|Search AutoFocus for malicious content to enrich observables.|[View in Store](https://store.servicenow.com/store/app/674a67261b246a50a85b16db234bcbd8)|
|[Palo Alto Networks WildFire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/palo-alto-wildfire-landing-page.md)|Palo Alto Networks|Enrich observables with WildFire cloud-based malware analysis.|[View in Store](https://store.servicenow.com/store/app/7f3a23261b246a50a85b16db234bcb5a)|
|[Zscaler \(ZIA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/zscaler-integration-for-security-operations.md)|Zscaler|Reputation lookups, block/allow lists, and sandbox reports from Zscaler Internet Access logs.|[View in Store](https://store.servicenow.com/store/app/9b1a67e21b246a50a85b16db234bcb8f)|
|**Email parser and phishing response**|
|[Check Point Anti-Bot – Email Parser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/checkpt-antibot-integration.md)|Check Point|Parse Check Point Anti-Bot email notifications to create security incidents.| |
|[HPE Security ArcSight ESM – Email Parser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/arcsight-emailparser-integration.md)|OpenText|Parse ArcSight ESM email notifications to create security incidents.| |
|[McAfee ESM – Email Parser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcafee-esm-emailparser-integration.md)|Trellix|Parse McAfee ESM email notifications to create security incidents.| |
|[Microsoft Exchange On-Premises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ms-exch-on-prem-landing-page.md)|Microsoft|Contain and eradicate phishing and spear-phishing email threats in on-premises Exchange.| |
|**Firewall and network containment**|
|[Palo Alto Networks Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/palo-alto-firewall-landing-page.md)|Palo Alto Networks|Block malicious values on the firewall through a MID Server for network containment.|[View in Store](https://store.servicenow.com/store/app/824e636a1b646a50a85b16db234bcbaa)|
|**Build your own integration**|
|[LLM-powered SIR integration builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sir-integration-builder-now-assist.md)|ServiceNow|Use the ServiceNow Otto for Security Incident Response \(SIR\) Integration Toolkit for a guided, UI-driven setup to build SIR integrations quickly.|Platform capability|

