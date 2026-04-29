---
title: Configuring AI Risk and Compliance
description: To use the AI Risk and Compliance application, you download and activate the application and then you must publish the assessment templates and set up the assessments and their automation logic to ensure accurate risk assessment scores.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Configuring AI Risk and Compliance

To use the AI Risk and Compliance application, you download and activate the application and then you must publish the assessment templates and set up the assessments and their automation logic to ensure accurate risk assessment scores.

## Configuration overview

1.  [Install AI Risk and Compliance](../task/install-ai-risk-and-compliance.md)
2.  [AI Risk and Compliance Content Pack](airc-content-pack.md)
3.  [Install AI Risk and Compliance Content](../task/install-ai-risk-content-pack.md)
4.  [Configure AI Risk and Compliance Workspace](../task/configure-airc-workspace.md)
5.  [Set up AI Risk and Compliance properties](../task/configure-airc-properties.md)
6.  [Set up Advanced Risk assessments properties](../task/advanced-risk-assessments-properties-airc.md)
7.  [Publish the assessment templates](../task/publish-the-assessment-templates.md)

**Note:**

Some AI capabilities are available only when the required plugins are installed.

-   AI Risk and Asset Management capabilities in AI Control Tower with Now Assist require the AI Risk and Asset Management for Now Assist plugin \(sn\_aict\_irm\_aiam\), which depends on:
    -   AI Risk and Compliance Integration with Control Tower \(sn\_grc\_ai\_irm\_intg\)
    -   AI Asset Management \(sn\_ai\_asset\_mgmt\)
-   AI Control Tower supports governance of both enterprise AI assets and ServiceNow AI assets, while AI Control Tower with Now Assist supports governance of ServiceNow AI assets only.
-   When AI Control Tower Core \(sn\_ai\_governance\) is used with AI Risk and Compliance in a new IRM deployment, the IRM Standard \(sn\_irm\_std\) plugin is required to make AI intake request forms available. These intake forms are used to submit requests through the Employee Portal for registering AI systems, AI models, and datasets for governance and risk evaluation.

    This requirement applies only to AI intake request forms and does not apply to AI cases, inquiries, or the Anonymous Reporting Center. For more information on applicable requests, see [Request an AI use case](../task/request-ai-system.md), [Request an AI model](../task/request-ai-model.md), and [Request a dataset](../task/request-dataset.md).


For information about AI Control Tower setup and plugin dependencies, see [Activation and installation of AI Control Tower](https://www.servicenow.com/docs/access?context=activation-and-installation-of-ai-control-tower&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

