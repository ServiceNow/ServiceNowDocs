---
title: Unified Security Exposure Management \(USEM\) release notes
description: The ServiceNow Unified Security Exposure Management \(USEM\) \(USEM\) application enhances exposure management with role-based views, enabling faster decision-making, efficient task handling, and streamlined approvals. See the following sections for release notes by release.This release adds a Change Request approval path to scheduled patch deployments, and separates risk modification from exception requests.This release rolls up SSVC decision values from CVEs to third-party entries, automatically re-evaluates remediation tasks when a finding's preferred solution changes, and adds support for deploying multiple patches in a single Microsoft SCCM or HCL BigFix deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/secops-sem-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [usem release notes, Unified Security Exposure Management, USEM, Patch Orchestration, Risk modification, Exception Management, Unified Security Exposure Management, USEM, SSVC, Patch Orchestration]
breadcrumb: [Security Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Unified Security Exposure Management \(USEM\) release notes

The ServiceNow® Unified Security Exposure Management \(USEM\) \(USEM\) application enhances exposure management with role-based views, enabling faster decision-making, efficient task handling, and streamlined approvals. See the following sections for release notes by release.

## About Unified Security Exposure Management \(USEM\)

-   Centralize exposure management workflows, improve visibility across exposures, and enforce governance through configurable rules.
-   Reduce the AI attack surface by using AI Security Exposure Management and supported integrations to remediate security exposures in AI assets.
-   Manage user and group role assignments, configure watchdogs with custom conditions, and access advanced settings directly from the Security Exposure Management Workspace.
-   Assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to define metadata and access control.
-   Normalize third-party source severity fields into standard ServiceNow severity values.

See [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/unified-security-exposure-management-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Unified Security Exposure Management \(USEM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Additional requirements**

    The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Unified Security Exposure Management \(USEM\), Security Incident Response, Threat Intelligence, and Configuration Compliance.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/security-operations-rn-landing.md)

## Brazil Early Availability

This release adds a Change Request approval path to scheduled patch deployments, and separates risk modification from exception requests.

### What's new

-   **[Schedule patch deployments through Change Request approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vr-ws-patch-schedule-change-request.md)**

    Route patch deployments scheduled from remediation tasks through Change Request approval for Microsoft SCCM and HCL BigFix integrations. This lets you align patch deployment for critical vulnerabilities with your organization's change management approval process, and optionally deploy the patch automatically once the change is approved.

-   **[Modify risk rating in bulk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-modify-risk.md)**

    Vulnerability Admins can now modify risk rating directly on individual or bulk findings across host, application, or container vulnerable item, or on a remediation task without an approval workflow. Remediation Owners can also modify risk ratings, with changes routed through a change approval process. Associating a compensating control with the change is optional for all roles.


### What's changed

-   **Risk rating options are no longer part of exception or deferral requests**

    Changing a risk rating is no longer available from the Request Exception dialog, or from the Bulk Edit dialog by selecting **Mitigating Control in Place** as a deferral reason. Risk rating and compensating control fields have been removed from both. Use **Modify risk** or **Request risk modification**, according to your role, to change a risk rating instead for individual records or in bulk.


## Brazil Early Availability

This release rolls up SSVC decision values from CVEs to third-party entries, automatically re-evaluates remediation tasks when a finding's preferred solution changes, and adds support for deploying multiple patches in a single Microsoft SCCM or HCL BigFix deployment.

### What's new

-   **[Enhancements to AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/ai-security-exposure-home.md)**
    -   Expanded AI posture findings for cloud assets. The system now stores and displays cloud account ID, region, and resource tags for AI assets hosted in cloud environments, including managed assets and agents. Cloud asset references are maintained for each discovered AI asset, enabling visibility into hosting relationships.
    -   Added remediation guidance and evidence for AI posture findings. Remediation steps for cloud configuration findings are now retrieved from Wiz and shown in a dedicated section within AI posture findings. Evidence provided by Wiz is also displayed in a scrollable section for review.
    -   Delta time supported for AI security findings integration. The integration now supports delta start time for importing findings, aligning with other Wiz integrations and improving data synchronization.
    -   Updated UI for AI posture findings. The posture rule description field is now split into a short description and a detailed description. The remediation section title is updated to "Remediation guidance," and an evidence section is added for findings. Metadata fields for managed AI assets are now displayed, including fallback to hosting asset or configuration item if direct values are unavailable.
    -   Added evidence mapping for the Wiz AI Security Findings integration. Updated the import set dictionary, REST message function, and "WizAISecurityFindingsProcessor" script include to capture and map finding evidence data from Wiz.
-   **[SSVC decision values roll up from CVEs to third-party entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/nvd-ssvc-enrichment.md)**

    USEM rolls up the Exploitation, Automatable, and Technical Impact SSVC \(Stakeholder-Specific Vulnerability Categorization\) values from CVE entries to the corresponding third-party entry \(TPE\) records. Changes to these values automatically trigger a risk score recalculation when the TPE risk calculator uses one or more of them.

-   **[Automatic re-evaluation of remediation tasks on Preferred solution change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

    Remediation tasks can now automatically re-evaluate findings when their Preferred solution changes, so items are regrouped into the appropriate remediation task without manual intervention. This helps keep remediation tasks accurate and reduces manual cleanup.

-   **[Deploy multiple patches to multiple collections with Microsoft SCCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/mspatch-integration.md)**

    Deploy more than one patch to more than one collection in a single deployment, instead of one patch to one collection at a time. When you select more than one patch for a deployment, the integration automatically creates a Software Update Group in Microsoft SCCM to bundle the patches.

-   **[Deploy multiple patches to multiple computer groups with HCL BigFix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vr-bigfix-integration.md)**

    Deploy more than one patch to more than one computer group in a single deployment, instead of one patch to one computer group at a time.

-   **[Resolve AI exposure tasks in workflow with Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/ai-security-exposure-employee-workflow.md)**

    AI Security Exposure Management integrates with Employee Center and third-party security tools to enable AI asset owners to remediate AI posture findings \(configuration issues\) directly through lightweight tasks.

-   **[Cisco AI Defense integration for AI security exposure management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/exploring-cisco-ai-defense-integration.md)**

    The Vulnerability Response Integration with Cisco AI Defense imports AI model vulnerabilities and AI model validation data \(results from automated red teaming or pentests\) into your ServiceNow AI Platform instance. You can use this data to detect security risks, drive remediation workflows, and verify compliance with AI security requirements.

-   **[Palo Alto Prisma AIRS AI Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/palo-alto-prisma-airs-ai-sgc.md)**

    This integration imports AI inventory data from Palo Alto Prisma AIRS and populates the CMDB in your ServiceNow AI Platform instance. In addition to inventory data, this integration imports key metrics related to AI model vulnerabilities, validation findings \(automated red teaming results\) that can be viewed in AI control tower.

-   **[Palo Alto Prisma AIRS Integration for AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/prisma-airs-integration.md)**

    Import AI security exposures such as model vulnerabilities, model validation findings \(automated red teaming alerts\), and posture findings \(configuration/policy violations\) into AI Security Exposure Management and automate workflows for remediation.

-   **[Configure the Wiz Test Results Integration to import AI findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/wiz-test-result-tab-filters.md)**

    Import cloud configuration findings as Test Results into Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents and AI security scans are routed into AI security exposure management tables \(AI posture findings\) if you have AI security exposure management activated.

-   **Attach findings to a penetration testing assessment request**

    Admins can now link pentest findings to existing pentest requests during manual upload, enabling consolidation of findings from multiple vendors under a single request.

-   **[Remove older SBOM records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sbom-cleanup.md)**

    SBOM cleanup lets you create a one-time rule to purge older software bill of materials records that match specified conditions that you create. Cleanup runs are permanent and can't be reversed, and you must review the conditions you set carefully before running one.


