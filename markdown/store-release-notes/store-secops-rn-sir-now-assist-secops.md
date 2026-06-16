---
title: Now Assist for Security Operations \(SecOps\) release notes
description: Version history for the Now Assist for Security Operations \(SecOps\) application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-sir-now-assist-secops.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Now Assist for Security Operations \(SecOps\) release notes

Version history for the Now Assist for Security Operations \(SecOps\) application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

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


