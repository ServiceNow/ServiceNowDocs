---
title: Configuring Smart Assessment Engine
description: You can activate or upgrade the Smart Assessment Engine application by downloading it from the ServiceNow Store and then configuring the settings in the initial setup checklist to meet your needs.
locale: en-US
release: xanadu
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configuring Smart Assessment Engine

You can activate or upgrade the Smart Assessment Engine application by downloading it from the ServiceNow Store and then configuring the settings in the initial setup checklist to meet your needs.

## Configuration overview

Install or upgrade ServiceNow® Smart Assessment Engine \(SAE\) by completing the task on the initial setup checklist.

## Initial setup checklist for SAE

Consider printing the following checklist so that you can check off the tasks as you complete them. To generate a PDF, select **Save As PDF** \(![Save as PDF icon.](../../grc-cam/image/save-as-pdf.png)\) and then select **Selected topic**.

<table id="table_ytv_tf2_kxb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Core** plugin \(com.sn\_smart\_asmt\).Role required: admin

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Designer** plugin \(com.sn\_smart\_asmt\_desg\).Role required: admin

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Connected** plugin \(com.sn\_smart\_asmt\_conn\).Role required: admin

</td></tr></tbody>
</table>To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

<table id="table_usx_km3_h2c"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Migration Tools** plugin \(com.sn\_smart\_asmt\_mig\).Role required: admin

**Note:** The migration plugin is necessary only if you have existing assessment designs. This plugin migrates your existing metric types to the new assessment templates. For more information on migrating metric types to assessment templates, see [Creating an assessment template from legacy assessment metric types](sae-asmnt-template-migrating.md).

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Dependencies** plugin \(com.sn\_smart\_asmt\_dep\).Role required: admin

**Note:** This plugin is necessary if you want to use the features domain separation and post-assessment actions.

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Post-Assessment Actions** plugins \(com.sn\_impact\_fwk\) and \(com.sn\_smart\_imp\_auto\).Role required: admin

**Note:** The Smart Assessment Dependencies plugin must be activated before activating the Smart Assessment Post-Assessment Actions plugins.

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Advanced Response Automation for Smart Assessment** plugin \(com.sn\_smart\_resp\_auto\).Role required: admin

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Basic Scoring for Smart Assessment** plugin \(com.sn\_smart\_scoring\).Role required: admin

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

Activate the **Smart Assessment Collaboration** plugin \(com.sn\_smart\_collab\).Role required: admin

</td></tr></tbody>
</table>To see the instructions for downloading a GRC application from the ServiceNow® Store, see [Download a GRC application from the ServiceNow Store for the first time](../../grc-common/task/download-grc-first-time.md).

**Note:** After installing the required plugins, you can do the following:

-   Assign SAE roles to users and user groups. Roles determine the permissions and access in the Smart Assessment Engine application. For more information, see [Roles in Smart Assessment Engine](../reference/sae-roles-defined.md).
-   Activate a language. The ServiceNow AI Platform uses American English by default. You can configure SAE to use a different language. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Refer to the upstream application documentation for further steps. For example, after installing the plugins from the setup checklist, you can refer to the Policy and Compliance Management documentation to enable smart assessments in Policy and Compliance Management.

