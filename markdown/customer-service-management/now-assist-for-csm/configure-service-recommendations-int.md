---
title: Configure service recommendations for interactions
description: Configure the service recommendations for interactions skill in the Now Assist Admin console to streamline case creation. This skill reduces cognitive effort, saves time, and promotes accurate case routing.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Generative AI, Generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure service recommendations for interactions

Configure the service recommendations for interactions skill in the Now Assist Admin console to streamline case creation. This skill reduces cognitive effort, saves time, and promotes accurate case routing.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console for configuring the service recommendations for interactions skill by specifying the roles permitted to use the skill and the role restrictions.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    Access the skills configuration page.

    Verify you have admin role.

2.  Select the **Customer** workflow and choose **CSM**

    This determines the product context for the skill.

    Workflow and product must match your configuration requirements.

3.  Select **Turn on** to activate skill for the service recommendations for interactions skill.

4.  Select **Add user access** to determine who can access this skill.

    Default and Custom Roles:

    -   If no changes are made, the default roles `sn_csm_case_types.service_definition_viewer`and `sn_esm_agent` automatically appear in **Add user access**.
    -   If custom roles were added before the upgrade, they’re updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in **Add user access**.
5.  Configure role restrictions to define which data and resources the skill can access when invoked \(default: `sn_csm_case_types.service_definition_viewer`\).

6.  Select **Turn on** to activate the skill.

    A screen appears showing **Successfully activated**.

7.  Select **Back to skills** to return to the skills menu.


## What to do next

Clone the skill to ground it in your environment for your specific needs.

**Related topics**  


[Clone the Now Assist for CSM skills](../concept/clone-the-now-assist-for-csm-skills.md#)

[Customizing a Now Assist for CSM skill](../concept/customizing-now-assist-skills.md)

