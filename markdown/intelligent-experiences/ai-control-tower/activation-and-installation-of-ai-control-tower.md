---
title: Activation and installation of AI Control Tower
description: The following section provides an order of installing the applications and their dependent plug-ins. These plug-ins are installed automatically when the generative AI Controller is installed as these plug-ins aren’t installed individually.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Configuring AI Control Tower workflows, AI Control Tower, Enable AI experiences]
---

# Activation and installation of AI Control Tower

The following section provides an order of installing the applications and their dependent plug-ins. These plug-ins are installed automatically when the generative AI Controller is installed as these plug-ins aren’t installed individually.

## Installation overview

Installing **AI Control Tower \(sn\_aict\)**, the dependent plug-ins are installed in the following order:

1.  AI Control Tower Core- This combines AI assets and controls in a central hub, ensuring comprehensive governance and management.
2.  AI Asset management- The ability to collect information, track changes and manage the lifecycle of AI artifacts like AI systems, models, datasets, and prompts.
3.  AI Risk and Compliance management- It’s a comprehensive framework that facilitates end-to-end lifecycle management of AI risks. It supports activities such as risk classification of AI assets, mapping to regulatory authority documents, continuous monitoring, and policy compliance to ensure responsible and accountable AI usage.
4.  AI Case management- This module enables tracking, triaging, and resolution of incidents or inquiries related to AI systems. It provides a structured case handling mechanism for AI stewards, compliance officers, and stakeholders to manage AI-related exceptions, investigations, and operational events efficiently.
5.  AI Risk and Compliance integration with Control Tower- It establishes a seamless connection between AI Risk and Compliance and the AI Control Tower workspace. This integration ensures unified visibility into AI governance activities, enabling users to monitor risk postures, compliance statuses, and case workflows directly within the Control Tower interface for a centralized oversight experience.
6.  AI Risk and Compliance content \(optional\)- Provides customers to ensure compliance with the applicable laws, regulations, directives and/, or standards and that any content provided in the product is accurate and up to date. When the customer acknowledges that the content provided with the product is easy to use, then it’s that customer’s responsibility to replace the content with the applicable laws, regulations, directives and, or standards at its own discretion.
7.  AI Control Tower- Provides a single, consolidated view of all enterprise AI assets and their relationships, empowering organizations with enhanced integration, governance, and operational efficiency.

<table id="table_r1n_cvq_wfc"><thead><tr><th>

Application

</th><th>

Dependent plug-in

</th></tr></thead><tbody><tr><td>

AI Control Tower Core

</td><td>

Data Foundation Model \(sn\_cmdb\_foundation:1.1.0\)

</td></tr><tr><td>

AI Risk and Compliance management

</td><td>

-   AI Control Tower Core \(sn\_ai\_governance:4.0.2\)
-   GRC feature roles \(sn\_grc\_ftr\_role:21.0.1\)
-   GRC: Common workspace elements \(sn\_grc\_workspace:21.0.4\)
-   GRC: Policy and Compliance management \(sn\_compliance:21.0.2\)
-   Post assessment actions for Smart assessments \(sn\_smart\_imp\_auto:20.1.0\)
-   GRC: Risk management \(sn\_risk:21.0.2\)
-   Regulatory agency library \(sn\_reg\_body\_mgmt:21.0.0\)
-   Smart assessment core \(sn\_smart\_asmt:21.0.1\)
-   Smart assessment connected \(sn\_smart\_asmt\_conn:21.0.1\)
-   Smart assessment designer \(sn\_smart\_asmt\_desg:21.0.3\)

</td></tr><tr><td>

AI Risk and Compliance integration with Control Tower

</td><td>

-   AI Case Management \(sn\_ai\_case\_mgmt:21.0.1\)
-   AI Risk and Compliance management \(sn\_grc\_ai\_gov:21.0.1\)
-   GRC: Advanced Risk \(sn\_risk\_advanced:21.0.2\)

</td></tr><tr><td>

AI Control Tower

</td><td>

-   AI Asset Management \(sn\_ai\_asset\_mgmt: 2.0.0\)
-   AI Control Tower Core \(sn\_ai\_governance:4.0.2\)
-   AI Risk and Compliance integration with Control Tower \(sn\_grc\_ai\_irm\_intg:21.0.1\)
-   Engagement dashboard for AI Control Tower \(sn\_ai\_engagement:2.1.6\)
-   Value dashboard for AI Control Tower \(sn\_ai\_value:2.1.6\)
-   Health for AI Control Tower \(sn\_ai\_health:2.5.14\)

**Note:** The Health \(sn\_ai\_health:2.5.14\) tab in the AI Control Tower is available from Zurich \(September\) onwards. The Health plugin gets installed after the Value dashboard for AI Control Tower is installed.

-   AI Discovery \(sn\_ai\_disc:1.0.4\)

</td></tr></tbody>
</table>**Important:** The AI strategy tab in AI Control Tower is available only with SPM Professional license.

**Note:** For all Pro Plus licensed customers, the AI Control Tower for Now Assist 1.01 gets auto-installed with generative AI Controller \(sn\_generative.ai 11.0.9\). Installation of Now Assist plugin will auto-install relevant AI Control Tower plugins. No additional plugins are needed.

When the dependent plug-ins are active, you can look for AI Control Tower application in the ServiceNow Store, and download the application when available.

For information about how to download any application from the ServiceNow Store, see [Download any application from ServiceNow](https://www.servicenow.com/docs/bundle/yokohama-security-management/page/product/security-incident-response/reference/download-app-first-time.html)

