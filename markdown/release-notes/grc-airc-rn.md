---
title: AI Risk and Compliance release notes
description: The ServiceNow AI Risk and Compliance application provides a centralized process for assessing AI assets, scoring risk, and driving remediation. Release notes are organized by version.Version 23.0.3 introduces updated playbooks, risk classification and compliance for unmanaged assets, and introduces domain separation for governance assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-airc-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI risk and compliance, AIRC]
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# AI Risk and Compliance release notes

The ServiceNow® AI Risk and Compliance application provides a centralized process for assessing AI assets, scoring risk, and driving remediation. Release notes are organized by version.

## About AI Risk and Compliance

-   Assess, score, and monitor risk across your AI assets, from onboarding through deployment, until retirement.
-   Centralize regulatory risk assessments, impact assessments, issue tracking, and remediation in a single workspace.
-   Manage risk and compliance scores for AI assets throughout their life cycle with workflows for ongoing oversight and risk management.
-   Manage conformity of AI assets with global regulations and frameworks.
-   Identify and address potential impacts on privacy, non- discrimination, and other human rights.

See [Version 23.0.3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-airc-rn.md) for more information.

## Activation and other requirements

**Note:** AI Risk and Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install AI Risk and Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## Version 23.0.3

Version 23.0.3 introduces updated playbooks, risk classification and compliance for unmanaged assets, and introduces domain separation for governance assets.

### What's new

-   **[Updated playbooks for governing managed assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.md)**

    Manage AI assets through structured lifecycle workflows using the updated playbooks. These playbooks automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases. Use the **Review and switch** button to understand impact to your existing playbooks, flows, and subflows before switching to the new playbook.

-   **[AI reviewer assist for risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-based-reviewer-assistant-for-assessments.md)**

    AI Risk and Compliance analysts reviewing assessments can review AI-assisted recommendations and assign relevant control objectives and risk statements from the compliance library. The Control Objective Recommender and Risk Statement Recommender skills generate the recommendations. The skills analyze the completed assessment responses and surface relevant control objectives and risk statements from the Risk and Compliance library. Accepted recommendations are scoped automatically to the AI Asset.


### What's changed

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-domain-separation.md)**

    Domain separation is supported for AI Control Tower. Domain separation enables separation of data, processes, and administrative tasks into logical groupings called domains. Administrators can control several aspects of this separation, including which users can see and access data. For AI Risk and Compliance, domain separation isolates each domain's risk posture while letting administrators at a parent domain see and manage risk across their child domains.

-   **[Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md) for unmanaged AI systems**

    Unmanaged AI systems now receive a risk classification and appear on the Regulatory risk classification donut chart. The risk classification is calculated based on the **Use and purpose** fields filled at the time of creating the asset and are assigned to the asset accordingly. Once the asset moves to the **Managed** state, the risk classification is revised based on updates to the **Use and purpose** fields or based on regulatory risk classification updates.

-   **Updates in [Continuous controls monitoring in the AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/airc-continuous-controls-monitoring.md)**

    The **Save** button in the Compliance evaluation enables AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] to maintain the configuration changes in Draft state before publishing. Additionally, the capability to specify the owner of individual compliance evaluation configurations has been introduced as a dedicated field. Assigning ownership helps introduce accountability to the rules and keep users informed who configured the rule.


