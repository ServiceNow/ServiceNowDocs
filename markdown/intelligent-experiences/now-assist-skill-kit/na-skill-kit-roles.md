---
title: AI Skill Kit roles
description: Certain roles are required to use AI Skill Kit functionality.This user can create, update, and publish skills in AI Skill Kit. This role is mandatory to use AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.html
release: yokohama
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2026-07-15"
reading_time_minutes: 2
breadcrumb: [AI Skill Kit reference, AI Skill Kit, Enable AI experiences]
---

# AI Skill Kit roles

Certain roles are required to use AI Skill Kit functionality.

## How roles work in AI Skill Kit

Three separate role concepts apply when you build and deploy a custom skill. Understanding the difference helps you plan access before you start and troubleshoot permission errors after you deploy.

-   **Roles required to use the AI Skill Kit**

    There are some roles that users need to perform an activities in AI Skill Kit, such as installing the plugin, building a skill, or activating a published skill. These roles are assigned to the people on your team who build and manage skills. For a list of the roles required for each activity, see the [Roles required for common tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.md) table.

-   **Roles required to trigger skills**

    These are roles a user must have to trigger a published skill on your instance. These roles are configured within the skill configuration as part of its access control list \(ACL\). The ACLs are separate from the roles required to build the skill. To learn more, see .

-   **Roles that a skill runs under**

    The roles that a skill operates with while it runs, which control what data and actions the skill can access on behalf of the triggering user. These are configured on the skill as role restrictions. Role restrictions are also separate from the roles required to build the skill. To learn more, see .


Two roles ship with AI Skill Kit:

-   **sn\_skill\_builder.admin** for building, editing, and publishing skills.
-   **sn\_skill\_builder.model\_admin** for managing the LLMs available to skills.

The platform **admin** role is also required at two points: to install AI Skill Kit and to activate a published skill in AI Admin Hub. In many deployments, one person holds all three roles.

**Note:** The ACL and role restriction concepts apply to the skill's runtime users, not to the people building the skill. If you're planning access for your build team, you only need the roles listed in the [Roles required for common tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.md) table.

## Roles required for common tasks in AI Skill Kit

Most work in AI Skill Kit requires the **sn\_skill\_builder.admin** role, including creating, cloning, editing, configuring, testing, evaluating, and publishing skills, and calling skills from scripts.

Two activities require the platform **admin** role instead: installing AI Skill Kit and activating a published skill in AI Admin Hub.

Triggering an activated skill from the UI requires whatever roles are configured in the skill's ACL. To learn more, see .

**Parent Topic:**[AI Skill Kit reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/na-skill-kit-reference.md)

## Skill kit admin \(sn\_skill\_builder.admin\)

This user can create, update, and publish skills in AI Skill Kit. This role is mandatory to use AI Skill Kit.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

