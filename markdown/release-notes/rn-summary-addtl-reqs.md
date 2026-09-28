---
title: Additional requirements for all Brazil features and products
description: Cumulative release notes summary on additional requirements for Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-addtl-reqs.html
release: brazil
topic_type: reference
last_updated: "2026-09-25"
reading_time_minutes: 5
breadcrumb: [Release notes summaries for Brazil features, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Additional requirements for all Brazil features and products

Cumulative release notes summary on additional requirements for Brazil features and products.

To use certain products, specific setups or third-party requirements are required.

<table id="rn-summary-additional-reqs-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Agent Studio

</td><td>

You must first install the supported version of the ServiceNow AI Platform to be able to use AI agents and AI Agent Studio. For more information, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-ai-agents-plugins.md).

Next Experience UI Framework must be enabled before you can use the ServiceNow Otto panel.

</td></tr><tr><td>

AI Desktop Actions

</td><td>

The following are required to use defined AI Desktop Actions:

-   Operating system: Microsoft Windows 11.
-   .NET 9.0 runtime v9.0.10 or .NET 9 Desktop Runtime v9.0.10.
-   No extended monitors are connected.

You must first install the supported ServiceNow Otto version of ServiceNow to be able to use the ServiceNow Otto AI agents. For more information, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-ai-agents-plugins.md).

You must enable Next Experience UI Framework before you can use the ServiceNow Otto panel.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   ****

You must have the Usage Insights API application installed from the ServiceNow Store to use Advanced AI Search Management Tools.


</td></tr><tr><td>

Autonomous Workforce

</td><td>

-   ****

Your instance must be on Brazil EA.


</td></tr><tr><td>

Build Agent and Autonomous Engineer

</td><td>

-   ****

Build Agent is dependent on ServiceNow Otto for Creator.


</td></tr><tr><td>

CRM Outlook Add-in

</td><td>

-   ****

Configuring email promotion requires the User Mailbox Integration plugin to be active on your instance so that emails associated through the add-in are promoted from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table, making them visible to agents in the workspace.


</td></tr><tr><td>

Clone Admin Console

</td><td>

-   ****
    -   The `clone_admin` role is required to request, cancel, or schedule clones.
    -   OAuth-based clone target authentication requires Australia Patch 5 or later on both the source and target instances. The `oauth_admin` role is required on the target instance during initial OAuth setup only. See [OAuth 2.0 authentication for clone targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-oauth-authentication.md).
    -   A Now Assist license is required to use the Clone FAQ Agent. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.
    -   Both the source and target instances must be on Australia Patch 5 or later to use Multi-Instance View.

</td></tr><tr><td>

Customer Engagement Sequences

</td><td>

-   ****

Email-based sequences requires the User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) to be active on your instance so that the sequence can detect email replies from prospects.


</td></tr><tr><td>

Customer self-service for Sales Customer Relationship Management

</td><td>

-   ****

Sales Cart REST APIs require the Billing Account Core \(sn\_billing\_account\) and Order Management \(sn\_ind\_tmt\_orm\) applications for supporting end-to-end ordering, billing, and payment flows.


</td></tr><tr><td>

Data Privacy and Discovery

</td><td>

-   ****
    -   Appropriate user roles assigned: Data Privacy Admin, Data Discovery Admin, and other role-based permissions for specific features.
    -   For OCR image discovery: Modern browser with JavaScript enabled; image file size limits apply \(typically 10 MB or less\).
    -   For reversible tokenization: Cryptographic key management system configured with authorized roles defined for de-anonymization access.
    -   For bring your own PII detection: External PII service endpoint accessible with credentials securely stored.
    -   For granular findings storage: Sufficient database storage for storing individual record references; retention policies should be defined.

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   ****

Requires Financial Services Card Operations \(sn\_bom\_credit\_card\).


</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

-   ****

Requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.


</td></tr><tr><td>

Domain Separation

</td><td>

-   ****
    -   Appropriate user roles assigned: Domain Separation Admin, Domain Policy Admin, and other role-based permissions for domain management and configuration.

</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   ****

ServiceNow Otto features are available with activation of the ServiceNow Otto for Enterprise Architecture \(EA\) plugin. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).


</td></tr><tr><td>

External Content Connectors

</td><td>

-   ****

Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

-   ****

Requires ITOM Visibility base plugins and appropriate role assignments for firewall management.


</td></tr><tr><td>

Kubernetes Visibility Agent \(KVA\)

</td><td>

-   ****

Requires ITOM Visibility base plugins, Discovery, and appropriate Kubernetes cluster access permissions. The agent must be deployed in each Kubernetes cluster you want to monitor.


</td></tr><tr><td>

LEAP

</td><td>

-   ****

You should have the following dependencies installed:

    -   ServiceNow Otto for Platform
    -   ServiceNow Otto for Creator

</td></tr><tr><td>

Live Connect

</td><td>

-   ****
    -   ODBC or JDBC drivers must be installed on client systems.
    -   User accounts must be configured with appropriate table access controls.

</td></tr><tr><td>

ReleaseOps

</td><td>

-   ****

ReleaseOps is not supported in regulated environments or on-premise. Check your entitlements to determine whether you have access to ReleaseOps.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   ****

The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Security Incident Response, Vulnerability Response, Threat Intelligence, and Configuration Compliance.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   ****

Microphone permission is required for WebRTC calls on mobile devices.


</td></tr><tr><td>

ServiceNow Lux Lab for VS Code

</td><td>

-   ****

The ServiceNow Lux Lab for VS Code extension requires the following:

<table id="table_imf_rfb_dkc"><thead><tr><th>

Application

</th><th>

Version

</th><th>

Resources for more information

</th></tr></thead><tbody><tr><td>

Visual Studio Code

</td><td>

1.97 later

</td><td>

[Visual Studio Code updates](https://code.visualstudio.com/updates/v1_132)

</td></tr><tr><td>

Node.js

</td><td>

24 or later

</td><td>

[Node.js](https://nodejs.org/en/download)

</td></tr><tr><td>

pnpm

</td><td>

10 or later

</td><td>

[pnpm](https://pnpm.io/installation)

</td></tr><tr><td>

ServiceNow SDK

</td><td>

4.10 or later

</td><td>

[ServiceNow SDK](https://www.npmjs.com/package/@servicenow/sdk)

</td></tr><tr><td>

ServiceNow instance

</td><td>

-   Australia Patch 5 or later
-   Zurich Patch 12 or later


</td><td>

[Prepare your upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/rn-prepare-landing-page.md)

</td></tr></tbody>
</table>


</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

-   ****

ServiceNow Otto for Virtual Agent requires at least one ServiceNow Otto product or the Requestor Agents - Foundation plugin.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   ****
    -   The CrowdStrike vulnerability intelligence feed requires a CrowdStrike subscription that includes vulnerability intelligence, such as Falcon Adversary Intelligence or Falcon Adversary Intelligence Premium.
    -   Sighting search with CrowdStrike NextGen SIEM requires the CrowdStrike API base URL, a client ID, and a client secret. Which log repositories you can search depends on the Falcon subscriptions enabled on your account.
    -   The Extract information from documents skill must be enabled for the AI-powered intelligence import.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\)

</td><td>

-   ****

The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Unified Security Exposure Management \(USEM\), Security Incident Response, Threat Intelligence, and Configuration Compliance.


</td></tr><tr><td>

Vulnerability Response

</td><td>

-   ****

The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Vulnerability Response, Security Incident Response, Threat Intelligence, and Configuration Compliance.


</td></tr><tr><td>

Zero Copy Connectors

</td><td>

-   ****
    -   Role required: df\_connection\_admin to create connections. Data steward access is also required to view mapped tables.
    -   REST connectors require network connectivity to the target REST-enabled system.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/release-notes-summaries.md)

