---
title: Now Assist for Security Incident Response release notes
description: Version history for the Now Assist for Security Incident Response application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-now-assist.html
release: store
topic_type: reference
last_updated: "2025-10-16"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Now Assist for Security Incident Response release notes

Version history for the Now Assist for Security Incident Response application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.0.0 - October 2025**
    -   Changed: Updated the dependent applications "Now Assist for Platform" versions to 9.2.2v \(performance optimizations\).
    -   Fixed:
        -   Recommended actions refresh is not removing old entries.
        -   Remove the Generate Insights button from the Related Records tab.
-   **Version 3.5.0 - September 2025**
    -   New: Added a new agentic workflow, "Generate Shift Handover Report for a Security Incident".
    -   Changed: Added ACLs for all the existing skills and agents.
-   **Version 3.3.0 - August 2025**
    -   New: Support for both skills and agents with all 4 models \(Azure Open AI, Now LLM, Google Gemini, Amazon Bedrock\).
    -   Fixed: Stabilized the Resolve Security Incident Workflow.
-   **Version 3.2.2 - June 2025**
    -   New:
        -   Security Incident Resolving: This agentic workflow helps security analysts resolve security incidents by leveraging existing runbooks and historical security incidents. By analyzing similar past cases, it generates a clear and effective plan to resolve ongoing security incidents.
        -   SOC Efficiency Analyzing: This agentic workflow helps SOC managers assess the quality of security incidents and track the key performance metrics, providing insights to explain and improve SOC operations.
            -   Generate Key Metrics for Security Incident Response \(SIR\): Track case volume, Mean Time to Assign \(MTTA\), and Mean Time to Resolve \(MTTR\) over a customizable date range.
            -   Metrics Analysis and Insights: Receive actionable insights into how to optimize MTTR, MTTA, and case volume, along with recommendations for improvement based on the data.
    -   Changed:
        -   Recommended Actions:
            -   Enhanced to incorporate a feedback option on the overall recommendation provided, enabling continuous improvement of future recommendations.
            -   Additionally, the top \(N\) number of recommendation cards are displayed based on the configuration settings.
-   **Version 3.0.1 - May 2025**
    -   New:
        -   Analyze security operations metrics
            -   The Analyze security operations metrics agentic workflow empowers security managers to evaluate their team's performance.
                -   Generate Key Metrics for Security Incident Response \(SIR\): Track case volume, Mean Time to Assign \(MTTA\), and Mean Time to Resolve \(MTTR\) over a customizable date range.
                -   Metrics Analysis and Insights: Receive actionable insights into how to optimize MTTR, MTTA, and case volume, along with recommendations for improvement based on the data.
        -   The Resolve security incident agentic workflow can help your SOC teams resolve security incidents.
            -   SOC analysts and managers can chat with an AI agent in the Now Assist panel to help them resolve security incidents.
    -   Changed:
        -   Enhancements to correlation insights
        -   -   You can generate and view results for correlation insights in the Security Incident Response Workspace.
-   Correlation insights are not limited to the primary configuration item \(CI\) or affected users associated with a security incident. You can base your correlation insights on any CI or affected user for a security incident.
-   You can generate correlation insights from the Investigation tab for a security incident in any state in the Security Incident Response Workspace.
-   You can generate insights for multiple items simultaneously for Associated Observables, Configuration items, and Affected Users.
-   Results are displayed in a modeless dialog that you can size and move.
-   **Version 2.0.3 - March 2025**
    -   New:
        -   The "Close Security Incident" use case assists analysts in closing a security incident from the "Now Assist panel" by generating the Post Incident Analysis, Closure notes, and close code, while overriding all mandatory task closures and assessments.
        -   Additionally, it supports closing a security incident as a false positive, which skips the generation of Post Incident Analysis, Closure notes, and close code, and directly closes the incident by marking it as False Positive.
-   **Version 2.0.1 - February 2025**

    Empower your SOC team with Generative AI capabilities for Security Incident Response.


