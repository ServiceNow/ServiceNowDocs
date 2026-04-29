---
title: Configuring AI Control Tower workflow
description: Configure the AI Control Tower workflow.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Control Tower, Enable AI experiences]
---

# Configuring AI Control Tower workflow

Configure the AI Control Tower workflow.

## Configuration overview

1.  [Activation and installation of AI Control Tower](activation-and-installation-of-ai-control-tower.md)
2.  [Configure AI Control Tower](configuring-ai-governance.md)
3.  [Configure multi-instance management for AI Control Tower](../task/configure-multi-instance-management-for-aict.md)

**Note:**

Some AI capabilities are available only when the required plugins are installed.

-   AI Risk and Asset Management capabilities in AI Control Tower with Now Assist require the AI Risk and Asset Management for Now Assist plugin \(sn\_aict\_irm\_aiam\), which depends on:
    -   AI Risk and Compliance Integration with Control Tower \(sn\_grc\_ai\_irm\_intg\)
    -   AI Asset Management \(sn\_ai\_asset\_mgmt\)
-   AI Control Tower supports governance of both enterprise AI assets and ServiceNow AI assets, while AI Control Tower with Now Assist supports governance of ServiceNow AI assets only.
-   When AI Control Tower Core \(sn\_ai\_governance\) is used with AI Risk and Compliance in a new IRM deployment, the IRM Standard \(sn\_irm\_std\) plugin is required to make AI intake request forms available. These intake forms are used to submit requests through the Employee Portal for registering AI systems, AI models, and datasets for governance and risk evaluation.

    This requirement applies only to AI intake request forms and does not apply to AI cases, inquiries, or the Anonymous Reporting Center.


