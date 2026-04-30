---
title: Configuring Smart Assessment Engine
description: You can activate or upgrade the Smart Assessment Engine application by downloading it from the ServiceNow Store and then configuring the settings in the initial setup checklist to meet your needs.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configuring Smart Assessment Engine

You can activate or upgrade the Smart Assessment Engine application by downloading it from the ServiceNow Store and then configuring the settings in the initial setup checklist to meet your needs.

## Configuration overview

Install or upgrade ServiceNow® Smart Assessment Engine \(SAE\) by activating the required plugins. The plugins are organized into two groups: standard application plugins that provide core functionality, and advanced feature plugins that enable additional capabilities.

## Standard application plugins for SAE

Activate the following plugins to set up the core SAE application. Role required is sn\_smart\_asmt.assessment\_admin.

-   **Smart Assessment Core** plugin \(com.sn\_smart\_asmt\)
-   **Smart Assessment Designer** plugin \(com.sn\_smart\_asmt\_desg\)
-   **Smart Assessment Connected** plugin \(com.sn\_smart\_asmt\_conn\)

To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

## Advanced feature plugins for SAE

Activate the following plugins to enable additional SAE capabilities. Role required: sn\_smart\_asmt.assessment\_admin.

-   **Smart Assessment Migration Tools** plugin \(com.sn\_smart\_asmt\_mig\)

    **Note:** The migration plugin is necessary only if you have existing assessment designs. This plugin migrates your existing metric types to the new assessment templates. For more information on migrating metric types to assessment templates, see [Creating an assessment template from legacy assessment metric types](sae-asmnt-template-migrating.md).

-   **Smart Assessment Dependencies** plugin \(com.sn\_smart\_asmt\_dep\)

    **Note:** This plugin is necessary if you want to use the features domain separation and post-assessment actions.

-   **Smart Assessment Post-Assessment Actions** plugins \(com.sn\_impact\_fwk\) and \(com.sn\_smart\_imp\_auto\)

    **Note:** The dependencies plugin must be activated before activating the Smart Assessment Post-Assessment Actions plugins.

-   **Advanced Response Automation for Smart Assessment** plugin \(com.sn\_smart\_resp\_auto\)
-   **Basic Scoring for Smart Assessment** plugin \(com.sn\_smart\_scoring\)
-   **Smart Assessment Collaboration** plugin \(com.sn\_smart\_collab\)

To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

**Note:** After installing the required plugins, you can do the following:

-   Assign SAE roles to users and user groups. Roles determine the permissions and access in the Smart Assessment Engine application. For more information, see [Roles in Smart Assessment Engine](../reference/sae-roles-defined.md).
-   Activate a language. The ServiceNow AI Platform uses American English by default. You can configure SAE to use a different language. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   Refer to the upstream application documentation for further steps. For example, after installing the plugins from the setup checklist, you can refer to the Policy and Compliance Management documentation to enable smart assessments in Policy and Compliance Management.

