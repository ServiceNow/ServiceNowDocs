---
title: ServiceNow Otto for Security Operations \(SecOps\) release notes
description: Version history for the ServiceNow Otto for Security Operations \(SecOps\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-now-assist-secops.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Security Incident Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# ServiceNow Otto for Security Operations \(SecOps\) release notes

Version history for the ServiceNow Otto for Security Operations \(SecOps\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.5.2 - September 2026**
    -   New:
        -   Security Incident AI ROI Summary Dashboard.
        -   Enhancements to Quality assessment.
        -   Added version tracking for report history.
        -   Duplicate reports as editable drafts.
        -   Refresh selected report sections independently by prompting in Natural language.
        -   Configurability to add additional context, KB articles for generating consistent assessments.
    -   Fixed: PRB2059317: NACM Actions not available for post incident analysis flow in UI 16.
-   **Version 6.4.5 - August 2026**
    -   Changed: Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand.
    -   Fixed: Correlation Insight skill now supports optional security incident ID for MCP.
-   **Version 6.3.4 - July 2026**

    Changed: Default models for all skills updated from Now LLM to 3P model.

-   **Version 6.1.2 - June 2026**
    -   Fixed:
        -   Submitting feedback on AI-generated recommended actions fails for non-admin users \(e.g., analysts\).
        -   Correlation Insights - No output for certain CIs.
        -   Generate Insights action visible even when Now Assist for Security Incident Response was not installed.
    -   Changed:
        -   Summarization skill enhancement to honor chronological order of events and to give more weightage to recent activity.
        -   AI Gradient styling for Correlation Insights and Summarization.
-   **Version 6.0.1 - May 2026**

    Changed: Removed install as a dependency check.

-   **Version 6.0.0 - April 2026**

    New: Created product tiers to offer generative AI skills agents, agentic workflows, and features to help customers start with generative AI on the ServiceNow Platform.

-   **Version 4.3.5 - April 2026**

    Fixed: Role masking Gap: Added generative AI request/response validators and preprocessor/postprocessor for the Correlation Insights feature.

-   **Version 4.3.1 - March 2026**
    -   New: Skill to evaluate natural language conditions.
    -   Changed:
        -   Security Incident Resolver v2 - AI Runbooks.
        -   Extending security incident resolver agentic workflow capabilities.
-   **Version 4.2.1 - January 2026**

    Fixed: Pre-run enabled tool fixed for the Shift Handover workflow.

-   **Version 4.1.5 - December 2025 \(Zurich\)**
    -   New:
        -   Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule-set. The quality assessment report provides an overall assessment summary followed by a detailed assessment for all the rules.
        -   Provided support for all existing skills and agentic workflows with the new Now LLM LTS model.
        -   Enabled Role Masking for all existing agentic workflows.
    -   Changed:
        -   All the skills under Now Assist for Security Incident Response are now turned ON by default.
        -   Performance improvement for the Wrap Up Security Incident use case.
        -   Improved Performance for Generating Correlation Insights.
    -   Fixed: Bug fixes for Correlation Insights.
-   **Version 4.0.1 - November 2025**

    Fixed: Change Requests were not getting displayed on the correlation insights modal

-   **Version 1.1.2 - November 2024**
    -   New:
        -   Generate post-incident analysis skill:
            -   Automatically generate a post-incident analysis for a security incident that includes a root cause analysis, impact assessment, and learning and recommendations information.
            -   You have the option to edit and save generated analysis details.
            -   Post-incident analysis is supported for security incidents in the Security Incident Response Workspace and in UI16 \(legacy\).
                -   The generated post-incident analysis is saved in the Post incident analysis field on the Details tab and on the Overview tab on security incidents after you close them in the Security Incident Response Workspace.
                -   InUI16 \(legacy\), the generated post-incident analysis is displayed on the Post Incident Review tab of the security incidents.
    -   Generate security incident recommended actions skill:
        -   Within the workflow and upon request, generate the next recommended steps your analysts can follow to help them close a security incident.
        -   You have the option to edit and save recommended steps to worknotes or create a response task.
        -   This skill is supported for security incidents in the Security Incident Response Workspace and in UI16 \(legacy\).
-   **Version 1.0.0 - August 2024**

    Empower your SOC team with Generative AI capabilities for Security Incident Response.


