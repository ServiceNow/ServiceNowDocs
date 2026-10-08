---
title: Configuring AI Risk and Compliance
description: To use the AI Risk and Compliance application, you download and activate the application and then you must publish the assessment templates and set up the assessments and their automation logic to ensure accurate risk assessment scores.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Configuring AI Risk and Compliance

To use the AI Risk and Compliance application, you download and activate the application and then you must publish the assessment templates and set up the assessments and their automation logic to ensure accurate risk assessment scores.

## Configuration overview

Verify that required applications, reference data, life cycle integrations, workspaces, governance artifacts, and access controls are in place so AI Risk and Compliance can be used end-to-end.

**Important:**

If you are upgrading AI Risk and Compliance, AI Control Tower Core, or Enterprise Architecture for AICT plugins together, review the upgrade order and dependencies in [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md) to avoid configuration issues.

1.  [Install AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-and-compliance.md)
2.  [AI Risk and Compliance Content Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-content-pack.md)
3.  [Install AI Risk and Compliance content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-content-pack.md)
4.  [Configure AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-workspace.md)
5.  [Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-properties.md)
6.  [Set up Advanced Risk assessments properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/advanced-risk-assessments-properties-airc.md)
7.  [Configure email-based intake for AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/config-cases-inquiries-from-email.md)

For more information on assessments and publishing assessments, see [Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md).

**Note:**

Some AI capabilities are available only when the required plugins are installed.

-   AI Risk and Asset Management capabilities in AI Control Tower with Now Assist require the AI Risk and Asset Management for Now Assist plugin \(sn\_aict\_irm\_aiam\), which depends on:
    -   AI Risk and Compliance Integration with Control Tower \(sn\_grc\_ai\_irm\_intg\)
    -   AI Asset Management \(sn\_ai\_asset\_mgmt\)
-   AI Control Tower supports governance of both enterprise AI assets and ServiceNow AI assets, while AI Control Tower with Now Assist supports governance of ServiceNow AI assets only.
-   When AI Control Tower Core \(sn\_ai\_governance\) is used with AI Risk and Compliance in a new IRM deployment, the IRM Standard \(sn\_irm\_std\) plugin is required to make AI intake request forms available. These intake forms are used to submit requests through the Employee Portal for registering AI systems, AI models, and datasets for governance and risk evaluation.

    This requirement applies only to AI intake request forms and does not apply to AI cases, inquiries, or the Anonymous Reporting Center. For more information on applicable requests, see [Request an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/request-ai-system.md), [Request an AI model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/request-ai-model.md), and [Request a dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/request-dataset.md).


For information about AI Control Tower setup and plugin dependencies, see [Activation and installation of AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activation-and-installation-of-ai-control-tower.md).

If your deployment also includes the Enterprise Architecture for AICT plugin \(`com.sn_ea_aict`\), review the upgrade-order guidance for AI Risk and Compliance, EA Workspace, and AI Control Tower Core before upgrading any of these applications out of sync. For more information, see [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md).

**Related topics**  


[Install AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-and-compliance.md)

[Install AI Risk and Compliance content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/install-ai-risk-content-pack.md)

[Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-properties.md)

[Configure AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-workspace.md)

[Roles and responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/roles-installed-with-ai-risk-and-compliance.md)

[Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md)

