---
title: Configuring Smart Assessment Engine
description: You can activate or upgrade the Smart Assessment Engine application by downloading it from the ServiceNow Store and then configuring the settings in the initial setup checklist to meet your needs.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configuring Smart Assessment Engine

You can activate or upgrade the Smart Assessment Engine application by downloading it from the ServiceNow Store and then configuring the settings in the initial setup checklist to meet your needs.

## Configuration overview

Install or upgrade ServiceNow® Smart Assessment Engine \(SAE\) by activating the required plugins. The plugins are organized into two types: required application plugins that provide core functionality, and optional feature plugins that enable additional capabilities.

## Plugins for SAE

Activate the following plugins to set up the core SAE application. Role required is sn\_smart\_asmt.assessment\_admin.

|Plugin|Plugin ID|Type|What this plugin does|
|------|---------|----|---------------------|
|Smart Assessment Dependencies|com.snc.smart\_asmt\_dep|Required|Enables domain separation and post-assessment actions. Activate this plugin before activating the other required plugins.|
|Smart Assessment Core|com.sn\_smart\_asmt|Required|Provides the foundation for SAE, including assessment templates, assessment instances, questions, sections, and the Assessment Workspace.|
|Smart Assessment Designer|com.sn\_smart\_asmt\_desg|Required|Provides the drag-and-drop template designer for building and editing assessment templates with sections, subsections, and nine question types. Without this plugin, you cannot design or modify assessment templates.|
|Smart Assessment Connected|com.sn\_smart\_asmt\_conn|Required|Enables integration between SAE and other applications. Provides the Trigger Smart Assessment flow action to generate assessment instances from published templates through Workflow Studio or scripting.|
|Smart Assessment Migration Tools|com.sn\_smart\_asmt\_mig|Optional|Migrates existing metric types to the new assessment template format. Activate this plugin only if you have existing assessment designs that need migration. For more information, see [Creating an assessment template from legacy assessment metric types](sae-asmnt-template-migrating.md).|
|Smart Assessment Post-Assessment Actions|com.sn\_impact\_fwk and com.sn\_smart\_imp\_auto|Optional|Enables automated actions that run after an assessment is submitted. You can link subflows to a template category so that specific workflows trigger automatically based on assessment results.|
|Advanced Response Automation for Smart Assessment|com.sn\_smart\_resp\_auto|Optional|Enables inline response automation that triggers when a responder selects a specific answer to a question. For example, you can configure a question to automatically create a task or record based on the selected response.|
|Basic Scoring for Smart Assessment|com.sn\_smart\_scoring|Optional|Enables scoring configuration for assessment templates, including metrics, aggregation strategies, and normalization functions. Scores are computed at the question, section, subsection, and assessment levels after an assessment is completed.|
|Smart Assessment Collaboration|com.sn\_smart\_collab|Optional|Enables multi-contributor assessments with persona-based section assignment. Multiple users can contribute to a single assessment, with each contributor assigned to specific sections based on their persona.|

To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

**Note:** After installing the required plugins, you can do the following:

-   Assign SAE roles to users and user groups. Roles determine the permissions and access in the Smart Assessment Engine application. For more information, see [Roles installed in Smart Assessment Engine](../reference/sae-roles-defined.md).
-   Activate a language. The ServiceNow AI Platform uses American English by default. You can configure SAE to use a different language. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md).
-   Refer to the upstream application documentation for further steps. For example, after installing the plugins from the setup checklist, you can refer to the Policy and Compliance Management documentation to enable smart assessments in Policy and Compliance Management.

