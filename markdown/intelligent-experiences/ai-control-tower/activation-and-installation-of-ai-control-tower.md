---
title: Activation and installation of AI Control Tower
description: The following section provides an order of installing the applications and their dependent plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/activation-and-installation-of-ai-control-tower.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# Activation and installation of AI Control Tower

The following section provides an order of installing the applications and their dependent plugins.

## Installation overview

When you install **AI Control Tower \(sn\_aict\)**, the following dependent plugins are installed in order:

1.  AI Control Tower Core — Combines AI assets and controls in a central hub for governance and management.
2.  AI Asset Management — Collects information, tracks changes, and manages the lifecycle of AI artifacts such as AI systems, models, datasets, and prompts.
3.  AI Risk and Compliance Management — Supports end-to-end lifecycle management of AI risks, including risk classification of AI assets, mapping to regulatory authority documents, continuous monitoring, and policy compliance.
4.  AI Case Management — Enables tracking, triaging, and resolution of incidents or inquiries related to AI systems. Compliance officers, AI stewards, and stakeholders can use it to manage AI-related exceptions, investigations, and operational events.
5.  AI Risk and Compliance integration with Control Tower — Connects AI Risk and Compliance with the AI Control Tower workspace. Users can monitor risk postures, compliance statuses, and case workflows directly within the Control Tower interface.
6.  AI Risk and Compliance content \(optional\) — Provides prebuilt content to support compliance with applicable laws, regulations, directives, and standards. Verify that the content reflects the laws, regulations, directives, and standards applicable to your organization.

<table id="table_r1n_cvq_wfc"><thead><tr><th>

Application

</th><th>

Dependent plugin

</th></tr></thead><tbody><tr><td>

AI Control Tower Core

</td><td>

Data Foundation Model \(sn\_cmdb\_foundation:1.9.1\)

</td></tr><tr><td>

AI Risk and Compliance management

</td><td>

-   AI Control Tower Core \(sn\_ai\_governance:6.2.6\)
-   GRC Feature roles \(sn\_grc\_ftr\_role:22.0.1\)
-   GRC: Common workspace elements \(sn\_grc\_workspace:22.0.4\)
-   GRC: Policy and Compliance management \(sn\_compliance:22.0.2\)
-   Post assessment actions for Smart assessments \(sn\_smart\_imp\_auto:22.0.2\)

 -   GRC: Risk management \(sn\_risk:22.0.2\)
-   Regulatory agency library \(sn\_reg\_body\_mgmt:21.1.1\)
-   Smart assessment core \(sn\_smart\_asmt:21.0.4\)
-   Smart assessment connected \(sn\_smart\_asmt\_conn:22.0.3\)
-   Smart assessment designer \(sn\_smart\_asmt\_desg:22.0.1\)

</td></tr><tr><td>

AI Risk and Compliance integration with Control Tower

</td><td>

-   AI Case Management \(sn\_ai\_case\_mgmt:22.0.1\)
-   AI Risk and Compliance management \(sn\_grc\_ai\_gov:22.2.2\)
-   GRC: Advanced Risk \(sn\_risk\_advanced:22.0.3\)

</td></tr><tr><td>

AI Control Tower

</td><td>

-   AI Asset Management \(sn\_ai\_asset\_mgmt: 5.0.1\)
-   AI Control Tower Core \(sn\_ai\_governance:6.2.6\)
-   AI Risk and Compliance integration with Control Tower \(sn\_grc\_ai\_irm\_intg:22.2.0\)
-   Engagement dashboard for AI Control Tower \(sn\_ai\_engagement:2.1.6\)
-   Value dashboard for AI Control Tower \(sn\_ai\_value:5.0.3\)
-   AI Discovery \(sn\_ai\_disc:2.0.6\)

</td></tr></tbody>
</table>After installing AI Control Tower \(sn\_aict\) from the ServiceNow Store, the required dependency plugins will be installed automatically.

For information about downloading any application from ServiceNow store, see [Download any application from ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/security-operations/download-app-first-time.md)

