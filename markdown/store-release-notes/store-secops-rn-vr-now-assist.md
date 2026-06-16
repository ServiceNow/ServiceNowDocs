---
title: Now Assist for Vulnerability Response release notes
description: Version history for the Now Assist Vulnerability Response application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-now-assist.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Now Assist for Vulnerability Response release notes

Version history for the Now Assist Vulnerability Response application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.0.0 - June 2026 \(USEM\)**

    New: The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to USEM. Users can now ask questions in plain language and get answers grounded in their own ServiceNow data — across all types of findings within USEM.

-   **Version 4.1.2 - April 2026**

    With enhancements for this release you might see improved performance.

-   **Version 4.0.0 - January 2026**
    -   New:
        -   The Retrieve VR Data agentic workflow.
        -   Chat with an AI agent using natural language to retrieve host \(Vulnerability Response\) and Application Vulnerability Response \(AVR\) data in the Unified Security Exposure Management \(USEM\) and legacy Vulnerability Response workspaces.
-   **Version 3.0.1 - December 2025**
    -   New:
        -   Create a custom API connector in the Security Posture Control workspace with the Connector builder framework module. You have the option to use generative AI to help your developers create custom API connectors quickly with a Now Assist skill \(SPC Setup Connector\) that is included with the Now Assist for Vulnerability Response application.
            -   Automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.
            -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment and monitor your overall security posture with the API connectors that you build.
        -   Generate insights to prioritize findings in the Security Exposure Management \(SEM\) workspace.
            -   Use generative AI to provide contextual summaries, actionable recommendations, and quick links in the Security Exposure Management \(SEM\) workspace, helping you prioritize critical risks and accelerate remediation.
        -   Generate recommendations for approval impact analysis in the SEM workspace.
            -   Use generative AI to provide on-demand recommendations to approve or reject a request directly from the Exception Change Approval record, enabling approvers to make faster, more consistent decisions while reducing manual analysis effort.
-   **Version 2.1.0 - October 2025**

    Fixed:

    -   Read and write access control with the sn\_vul\_ai.write\_rem\_insights and sn\_vul\_ai.read\_rem\_insights granular roles to the retrieved SLA metrics from the Analyze Remediation Status agentic workflow stored on the Remediation Compliance Insights \[sn\_vul\_ai\_remediation\_insights\] caching table.
    -   These granular roles are inherited automatically by the sn\_vul.vulnerability\_admin and sn\_vul.vulnerability\_analyst persona roles and by the VR.System role so background job execution for the workflow can occur.
-   **Version 1.0.4 - September 2025**
    -   New:
        -   Recommend preferred solution for VIT Now Assist skill
        -   Vulnerable item deduplication Now Assist skill
-   **Version 1.0.3 - August 2025**

    New: Enhancements to support third-party large language models \(LLMs\).

-   **Version 1.0.2 - June 2025**

    Empower your vulnerability managers and analysts with AI agents in the Now Assist with Vulnerability Response application to revolutionize how they monitor and remediate your most critical vulnerabilities.

-   **Version 1.0.1 - May 2025**

    Empower your vulnerability managers and analysts with AI agents in the Now Assist with Vulnerability Response application to revolutionize how they monitor and remediate your most critical vulnerabilities.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

