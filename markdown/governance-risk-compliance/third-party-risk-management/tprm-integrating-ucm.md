---
title: Managing TPRM SAE templates with Unified Content Management
description: Use Unified Content Management \(UCM\) as a centralized, managed repository of pre-built smart assessment templates for Third-party Risk Management. With UCM installed, TPR managers can browse, preview, and activate templates for assessments, and update templates when newer versions are released.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-02-02"
reading_time_minutes: 3
keywords: [Unified Content Management, UCM, Third-party Risk Management, Smart Assessment templates, Smart Assessment Engine \(SAE\), questionnaires, template activation, content repository, version control]
breadcrumb: [Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Managing TPRM SAE templates with Unified Content Management

Use Unified Content Management \(UCM\) as a centralized, managed repository of pre-built smart assessment templates for Third-party Risk Management. With UCM installed, TPR managers can browse, preview, and activate templates for assessments, and update templates when newer versions are released.

In TPRM, UCM supports multiple template types, including external questionnaires, internal risk questionnaires \(IRQ\), document requests, and standardized information gathering \(SIG\) assessments. The UCM library includes versioned templates \(for example, year-based versions\) to support managed updates to template content over time.

You can install the Unified Content Management application from the ServiceNow Store. After installation, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can access UCM from the Vendor Management Workspace to browse available smart assessment templates, preview sections and question counts, and activate templates for use in new assessments. ![](../image/unified-content-mgmt-icon.png) Activation makes a template available when creating assessments. When a newer version of a template is released, TPR managers can update the template to use the newer version. For more information, see [Activate or update Smart Assessment templates](../task/activate_sae_ucm.md).

In the Vendor Management Workspace, the UCM page is designed to show only TPRM SAE templates. Classic templates remain available through existing paths, but they are not visible or managed through UCM.

To use SAE, you must set the Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property. After this property is set, SAE becomes the default assessment engine and replaces the legacy experience.

**Warning:** After this option is enabled, this selection can’t be reversed.

For more information, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md) and [Migrating from Classic Assessment Engine to Smart Assessment Engine](tprm-migrate-asmnt-sae.md).

You are responsible for ensuring compliance with applicable laws, regulations, and standards. Review and customize any activated template content as needed to match your organization’s requirements.

**Related topics**  


[Activate or update Smart Assessment templates](../task/activate_sae_ucm.md)

[Viewing third-party risk reports](unified-vrm-workspace.md)

[TPRM Unified content management page](../../grc-workspace-vrm/concept/tprm-ws-ucm-page.md)

[Monitoring your third-party risk](tprm-monitoring-tpr.md)

