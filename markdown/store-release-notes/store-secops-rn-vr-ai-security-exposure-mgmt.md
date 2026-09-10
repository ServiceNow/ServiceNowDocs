---
title: AI Security Exposure Management release notes
description: Version history for the ServiceNow AI Security Exposure Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-ai-security-exposure-mgmt.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Vulnerability Response version history release notes, ServiceNow Store - Security Operations version history release notes, ServiceNow Store version history release notes]
---

# AI Security Exposure Management release notes

Version history for the ServiceNow® AI Security Exposure Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.3 - September 2026**
    -   New:
        -   Employee-facing remediation tasks for AI posture findings. Remediation tasks are now generated for AI posture findings and assigned directly to the agent owner, who can resolve issues or request exceptions from Employee Center without security role access. Task outcomes update the posture finding state, and closure is verified on the next integration run. This is useful for assigning the issues on agents created by business users in platforms such as Copilot Studio.
        -   Handling of asset owner resolution during task creation. The employee task creation process synchronously resolves asset owners, eliminating race conditions between asynchronous owner lookup and task creation. Tasks are reliably created for eligible posture findings referencing newly discovered assets.
        -   Configurable assignment rules for posture findings. Admins can now configure assignment rules to route posture findings to a user reference field \(such as agent owner\) on the discovered AI asset, rather than only to a group.
        -   Link discovered asset to AI assets. Host information such as VM, container, or git repo is now linked from discovered assets to AI assets, providing additional context for posture findings. This is for findings on agents or MCP servers found running in hosts such as EC2 or containers in cloud.
        -   UI action for creating AI Exposure Tasks. Vulnerability analysts can now trigger a "Create employee" action on AISEM posture findings to assign a task an end user for a configuration issue.
        -   Configurable property in advanced settings. A new "AI Security Exposure Management" tab is available in advanced settings, allowing admins to enable or disable employee task creation for AI posture findings.
    -   Changed:
        -   Enhanced exception approval table name construction. Posture finding approval records now have improved naming logic for exception approvals.
        -   Updated handler for ingesting discovered asset references. The handler now ingests discovered asset sys IDs and populates them across AI assets, ensuring host information is accurately linked.
        -   Updated UI configuration and unit tests for employee tasks. The employee task UI has been updated and tested for improved usability and reliability.
-   **Version 2.1.2 - August 2026**
    -   New:
        -   AI exposure metrics are now available on the dashboard - The home page and dashboard now display aggregated metrics for AI-related exposures, including findings by risk rating, source, AI exposure category, and asset type. Users can view AI vulnerabilities by type, validation findings by threat category, and posture findings by platform. Remediation progress and assignment group breakdowns are also included, with drill-downs enabled for each widget.
        -   New AI metrics cards have been introduced - Users can now access dedicated AI metrics cards showing vulnerabilities by type, validation findings by threat category, posture findings by platform, and findings by AI asset type. Each card supports drill-down for detailed analysis and matches the metrics available in the AI Security Analysis section.
        -   Out-of-the-box assignment rules and risk calculators are now provided for AI security findings - Admins can use new script-based assignment rules to automatically assign AI security findings to the appropriate support group based on the affected business application. Script-based risk calculators for AI vulnerabilities, validation findings, and posture findings are now available, using vendor severity, business criticality, and MITRE ATLAS techniques as inputs.
        -   AICT data push for posture metrics is now supported - The system now pushes posture findings metrics to AICT and shares drill-downs with the AICT team. New performance analytics indicators support related widgets.
        -   Configuration updates for AI Security Exposure Management are now available - The package configuration now includes updated dependencies and versioning for AI Security Exposure Management, Vulnerability Response, and Configuration Compliance.
        -   Otto Directive branding updates have been implemented - The AI summary card in AI Security Exposure Management now uses the Otto icon and updated text, replacing previous Now Assist branding. The "Ask Now Assist" button is now labeled "Ask Otto," and associated tests have been updated.
        -   Accessibility compliance improvements have been delivered - The AI Security Exposure Management application has undergone an accessibility audit and remediation, addressing all critical and high-severity issues to meet WCAG 2.1 AA standards.
    -   Changed: Dashboard filters and widgets enhanced for AI exposures - The dashboard now includes new filter pills for posture, validation, and scan findings, and applies AI Security Exposure Management tables to existing widgets for risk rating, source, and remediation progress. Drill-down functionality has been verified for each widget.
-   **Version 2.0.2 - July 2026**
    -   New: Remediation task support for AI Security Exposure Management findings.
    -   Fixed: Addressed gaps found in USEM functionality for AI exposures.
-   **Version 2.0.1 - June 2026**
    -   Vulnerability management teams can use AI Security Exposure Management to help them import various types of security exposures in the AI assets including AI model vulnerabilities, AI model validation \(automated red teaming\) alerts, and AI posture findings \(configuration issues in AI agents or tools, etc.\) and manage these issues along with other types of exposures in the Unified Security Exposure Management workspace.
    -   The AI Exposures dashboard provides you with a view into the critical security vulnerabilities of your AI attack surface. You have the option to use a generative AI skill to help you determine if any of the threats might be already mitigated and help you prioritize high risk exposures and defer lower risk exposures that have mitigations or guardrails already in place.

**Parent Topic:**[ServiceNow Store - Vulnerability Response version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

