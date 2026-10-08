---
title: Enterprise Architecture for AICT plugin installation and upgrade considerations
description: Upgrading AI Risk and Compliance, Enterprise Architecture Workspace, and AI Control Tower Core out of sync with each other temporarily affects the AI system-to-business application association.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-ea-common-upgrade-considerations.html
release: brazil
topic_type: reference
last_updated: "2026-09-17"
reading_time_minutes: 3
keywords: [upgrade, plugin dependency, Enterprise Architecture for AICT]
breadcrumb: [Reference, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Enterprise Architecture for AICT plugin installation and upgrade considerations

Upgrading AI Risk and Compliance, Enterprise Architecture Workspace, and AI Control Tower Core out of sync with each other temporarily affects the AI system-to-business application association.

## About the Enterprise Architecture for AICT plugin

The Enterprise Architecture for AICT plugin \(**com.sn\_ea\_aict**\) provides the shared many-to-many data model connecting AI systems and business applications, independently of the Enterprise Architecture Workspace plugin. Because the association no longer depends on Enterprise Architecture Workspace licensing, you can associate AI systems with business applications, and see that context in AI Control Tower, whether or not you use Enterprise Architecture Workspace.

## Why upgrade order matters

The Enterprise Architecture for AICT plugin \(**com.sn\_ea\_aict**\) installs automatically as a dependency of AI Control Tower Core. AI Risk and Compliance, Enterprise Architecture Workspace, and AI Control Tower Core can be upgraded independently. Each handles the AI system-to-business application association differently before and after Enterprise Architecture Workspace version 10.1.3. Upgrading only one of the three can temporarily create inconsistent data between workspaces.

AI Control Tower Core is itself a required dependency for AI Risk and Compliance, and the Enterprise Architecture for AICT plugin is a required dependency for AI Control Tower Core. Upgrading AI Risk and Compliance without AI Control Tower Core is not possible; the scenarios below cover the combinations that are.

## Recommended path

-   Upgrade AI Control Tower Core, Enterprise Architecture Workspace, and AI Risk and Compliance together in the same maintenance window.
-   If you can't upgrade all three together, upgrade AI Control Tower Core first. It brings in the Enterprise Architecture for AICT plugin automatically. Upgrade the other two as soon as possible afterward.

## Consequences of a partial upgrade

|If you upgrade|without also upgrading|You may see|
|--------------|----------------------|-----------|
|All three plugins together|—|Best case: everything works on the new data model immediately. Run the migration job once to move existing associations.|
|Enterprise Architecture Workspace only|AI Control Tower Core, AI Risk and Compliance|The AI systems related list and Business portfolio widget disappear from the business application record in Enterprise Architecture Workspace. The intake form field and the BA related list in AI Control Tower keep working on the old data model. Upgrade AI Control Tower Core at the same time to avoid this gap.|
|AI Control Tower Core + AI Risk and Compliance|Enterprise Architecture Workspace|Everything keeps working — Enterprise Architecture Workspace stays on the old data model while AI Control Tower and the intake form use the new one. The AI Control Tower home page shows a single Business portfolio, from the Enterprise Architecture for AICT plugin.|
|AI Control Tower Core + AI Risk and Compliance \(no Enterprise Architecture Workspace installed\)|—|New capability: the intake form field, the BA related list, and the Business portfolio widgets all become available for the first time, with no dependency on Enterprise Architecture Workspace.|
|AI Control Tower Core only \(no Enterprise Architecture Workspace installed\)|AI Risk and Compliance|The BA related list and Business portfolio widgets in AI Control Tower become available, but the intake form field still won't appear until AI Risk and Compliance is upgraded too.|

## After upgrading

You must run the [Migrate BA Product Model Map from EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-run-migrate-ba-product-model-map-job.md) job manually to move your existing associations into the new data model because the job does not run automatically.

**Related topics**  


[Components installed with AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-installed-with.md)

[Run the Migrate BA Product Model Map job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-run-migrate-ba-product-model-map-job.md)

[AI Control Tower integration with Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-aict.md)

