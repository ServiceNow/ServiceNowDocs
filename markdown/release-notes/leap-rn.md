---
title: LEAP release notes
description: The ServiceNow LEAP application uses AI driven insights to create standard and dynamic playbooks for quick incident resolution management. See the following sections for release notes by version.This release of LEAP includes automation projects, a modal to select knowledge base article locations, and an improved LEAP value dashboard. LEAP skills are now accessible to external clients through MCP tools.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/leap-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ITOM Visibility release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# LEAP release notes

The ServiceNow® LEAP application uses AI driven insights to create standard and dynamic playbooks for quick incident resolution management. See the following sections for release notes by version.

## About LEAP

-   Drive incident resolution to measure the time to resolve incidents and enhance performance.
-   Promote automation culture by interpreting existing data and automating records.
-   Optimize resource allocation by identifying and prioritizing high impact areas.
-   Integrate with Red Hat Ansible to map resolution steps with Ansible playbooks and help in incident resolution for L1 agents.
-   Automate knowledge base article creation to help L1 agent in faster resolution of similar incidents.

See [Exploring LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exploring-aiops-leap.md) for more information.

## Activation and other requirements

**Note:** LEAP is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install LEAP by requesting ServiceNow Otto for ITOM from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html). After installation, activate the skill from Workspaces &gt; LEAP &gt; Admin &gt; AI Admin Hub &gt; AI Skills &gt; Platform &gt; LEAP. For details, see [Activate LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/activate-aiops-leap.md).

-   **Additional requirements**

    You should have the following dependencies installed:

    -   ServiceNow Otto for Platform
    -   ServiceNow Otto for Creator

**Parent Topic:**[ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-visibility-rn.md)

## Version 4.3.0

This release of LEAP includes automation projects, a modal to select knowledge base article locations, and an improved LEAP value dashboard. LEAP skills are now accessible to external clients through MCP tools.

### What's new

-   **[Multi-taxonomy automation projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/automation-projects-leap.md)**

    LEAP can be configured to ingest and analyze incidents from multiple taxonomies to produce clusters and automation opportunities for all configured taxonomies. Existing single-taxonomy deployments are unaffected. Multi-taxonomy can be configured by admins using LEAP Properties.

-   **[Generate LEAP knowledge base articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/generate-aiops-leap-knowledge-base.md)**

    When creating a KB article from a LEAP automation opportunity, users are prompted to select a knowledge base and category before the article is published, with the author field and article metadata auto-populated from the opportunity record. Admins can configure an list of eligible knowledge bases in LEAP Properties to control which options appear in the modal.

-   **[LEAP MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aiops-leap-mcp-server-overview.md)**

    LEAP skills are now accessible to external clients through MCP tools, enabling integration with third-party systems and workflows.


### What's changed

-   **[Hide archived automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/automation-opportunities.md)**

    Automation opportunities \(AOs\) from an earlier GAF \(Global Automation Framework\) run are now hidden by default. Previously, old AOs with resolution steps remained visible in the workspace after remapping. It was difficult to distinguish actionable AOs from old ones. After a GAF re-run, the old AOs are archived and no longer appear on the homepage. The artifacts of archived AOs are mapped to relevant new AOs.

-   **[LEAP value dashboard expansion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/understand-the-aiops-leap-value-dashboard.md)**

    The LEAP value dashboard now surfaces metrics for all automation outcome types along with existing playbook data. New sections display Ansible execution counts, agent-hours saved, and top playbooks by tickets resolved, KB article creation counts and top contributing clusters, and problem record \(PRB\) creation counts and top clusters. A summary at the top of the dashboard breaks total automation activity and savings attribution by outcome type such as LEAP playbooks, Ansible playbooks, KB articles, and PRBs, each with a trend indicator. The dashboard also displays ServiceNow Otto consumption data to track the consumed per action.


### What's deprecated or removed

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

