---
title: AI Risk and Compliance release notes
description: The ServiceNow AI Risk and Compliance application provides a centralized process for assessing AI assets, scoring risk, and driving remediation. Release notes are organized by version.Version 23.0 introduces updated playbooks, risk classification for unmanaged assets, and domain separation for governance assets are available in this release.Version 23.1 introduces direct business application associations for AI assets and improves Employee Center redirection to AI Control Tower workspace records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-airc-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [AI risk and compliance, AIRC, AI Risk and Compliance]
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

See [September 2026](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-airc-rn.md) for more information.

## Activation and other requirements

**Note:** AI Risk and Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install AI Risk and Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.

    **Warning:** If AI Risk and Compliance, EA Workspace, and AI Control Tower Core are upgraded out of sync, business application associations may be lost or unavailable. For more information, see [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md) and [Configuring AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configuring-ai-risk-and-compliance.md).


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## September 2026

Version 23.0 introduces updated playbooks, risk classification for unmanaged assets, and domain separation for governance assets are available in this release.

### What's new

-   **[Updated playbooks for governing managed assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.md)**

    After upgrading to version 23.0.3, manage AI assets through structured life cycle workflows using the updated playbooks. These playbooks automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases. Use the **Review and switch** button to review the effect on your existing playbooks, flows, and subflows before switching to the new playbook.

-   **[AI reviewer assist for risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-based-reviewer-assistant-for-assessments.md)**

    After upgrading to version 23.0.2, AI Risk and Compliance analysts reviewing assessments can review AI-assisted recommendations and assign relevant control objectives and risk statements from the compliance library. The Control Objective Recommender and Risk Statement Recommender skills generate the recommendations. The skills analyze the completed assessment responses and display relevant control objectives and risk statements from the Risk and Compliance library. Accepted recommendations apply automatically to the AI asset.


### What's changed

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-domain-separation.md)**

    Domain separation is supported for AI Control Tower. Domain separation enables separation of data, processes, and administrative tasks into logical groupings called domains. Administrators can control several aspects of this separation, including which users can see and access data. For AI Risk and Compliance, domain separation isolates each domain's risk posture while letting administrators at a parent domain see and manage risk across their child domains.

-   **[Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md) for unmanaged AI systems**

    After upgrading to version 23.0.3, unmanaged AI systems receive a risk classification and appear on the Regulatory risk classification donut chart. The risk classification is calculated from the **Use and purpose** fields completed when the asset is created. After the asset moves to the **Managed** state, the risk classification is revised based on updates to the **Use and purpose** fields or based on regulatory risk classification updates.

-   **[Continuous controls monitoring in the AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/airc-continuous-controls-monitoring.md)**

    After upgrading to version 23.0.3, the **Save** button in the Compliance evaluation enables AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] to maintain the configuration changes in **Draft** state before publishing. A dedicated **Owner** field lets you specify the owner of individual compliance evaluation configurations and displays the owner name in a column. Assigning ownership adds accountability and shows users who configured the rule.


## October 2026

Version 23.1 introduces direct business application associations for AI assets and improves Employee Center redirection to AI Control Tower workspace records.

### What's new

-   **[Direct business application associations for AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/request-ai-system-form.md)**

    Business applications can be mapped directly to AI system records during intake, without requiring Enterprise Architecture Workspace to be installed. After upgrading AI Control Tower to version 9.0.3 and AI Risk and Compliance to version 23.1.1, Enterprise Architecture for AICT \(com.sn\_ea\_aict\) decouples the AI system-to-business-application association from Enterprise Architecture Workspace. The plugin installs automatically with AI Control Tower Core at the required version.

    **Warning:** If AI Risk and Compliance, EA Workspace, and AI Control Tower Core are upgraded out of sync, business application associations may be lost or unavailable. For more information, see [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md), Enterprise Architecture for AICT plugin, and [Configuring AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configuring-ai-risk-and-compliance.md).


### What's changed

-   **Links to AI Control Tower updated for Employee Center submissions**

    After upgrading AI Risk and Compliance to version 23.1.1, for AI use case, AI model, and dataset submissions in Employee Center, the **here** link in the confirmation message and the **Open in AI Control Tower** link on the post-submission page now open the corresponding record in AI Control Tower instead of the legacy AI Control Tower workspace. You still land on the Employee Center governance-details page immediately after submitting; only the destination of these links changed.

    The Employee Center AI asset list view's redirection link was also updated to open the AI Control Tower inventory.

    The AI system, AI model, and dataset record headers also display the corresponding record name and identifier after submission.

    **Note:** AI case and AI inquiry submissions in Employee Center aren't affected by this change.


