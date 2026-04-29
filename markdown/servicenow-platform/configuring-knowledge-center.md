---
title: Configuring Knowledge Center
description: Configure the knowledge content recommendation skill to enable agents to utilize the context menu to elaborate or shorten a knowledge article in the TinyMCE. With the new enhance content editor available with Knowledge Center, agents can create and update the knowledge article with custom instructions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Knowledge Center

Configure the knowledge content recommendation skill to enable agents to utilize the context menu to elaborate or shorten a knowledge article in the TinyMCE. With the new enhance content editor available with Knowledge Center, agents can create and update the knowledge article with custom instructions.

The first step in configuring the Knowledge Center involves enabling the following system properties:

-   **sn\_km\_center.glide.knowman.ece.enable**
-   **sn\_km\_center.glide.knowman.enable**
-   **sn\_km\_center.glide.knowman.redirect.enable**

For more information, see [Enable system properties for Knowledge Center](../task/enable-system-properties-for-KC.md)

Configure how agents use Knowledge Center to generate, edit, and optimize knowledge articles. Refer the following:

-   [Configuring custom script based Article Optimization scans](../task/configure-custom-script-based-AO-scan.md)
-   [Activate Article Optimization skill](../task/activate-kc-AO-skill.md)
-   [Configuring Article Optimization skill and prompts](../task/configure-kc-AO-skill.md)
-   [Enable knowledge blocks in the Knowledge Center](../task/kc-enable-knowledge-blocks.md)

**Note:** You can access knowledge articles created with TinyMCE by enabling KB generation skill, see [Configuring the KB generation skill](../../knowledge-management/task/Now-Assist-configuring-km-skills.md). To use articles created with custom instructions, please activate the knowledge content recommendation skill, see [Configure skill for Now Assist context menu](../../knowledge-management/task/Now-Assist-configuring-context-menu-skill.md).

**Related topics**  


[Configure Now Assist Skills for potential gaps](../../knowledge-management/task/configure-na-km.md)

[Configure and activate the Now Assist Identify duplicate articles skill](../../knowledge-management/task/Now-Assist-configuring-identify-duplicate-article-skill.md)

[Configure skill for Now Assist context menu](../../knowledge-management/task/Now-Assist-configuring-context-menu-skill.md)

