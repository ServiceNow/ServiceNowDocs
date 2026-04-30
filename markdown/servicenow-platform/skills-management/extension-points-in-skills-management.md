---
title: Extension points in Skills Management
description: Use extension points to calls scripts to add custom group types to manage skills.
locale: en-US
release: xanadu
product: Skills Management
classification: skills-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference for Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Extension points in Skills Management

Use extension points to calls scripts to add custom group types to manage skills.

To see a list of extension points that you can use for Workforce Optimization for ITSM, navigate to **System Extension Points** &gt; **Scripted Extension Points**. In the Extension Points list, open the sn\_skill\_cfg\_page.ManageSkillsExtnPt extension point.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

|Extension point name|Description|
|--------------------|-----------|
|sn\_skill\_cfg\_page.ManageSkillsExtnPt|Implement this extension point to customize the logic of creating users by groups for the Manage IT skills page.|

**Important:** You can configure additional groups using the `sn_skill_cfg_page.ManageSkillsConstants` script include. For information on script includes see, [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

