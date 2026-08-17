---
title: AI Skill Kit roles
description: Certain roles are required to use AI Skill Kit functionality.Create, configure, test, and publish skills in AI Skill Kit. Assign this role to anyone developing skills on your instance.Create and update custom large language models for use with AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2026-07-15"
reading_time_minutes: 6
breadcrumb: [AI Skill Kit reference, AI Skill Kit, Enable AI experiences]
---

# AI Skill Kit roles

Certain roles are required to use AI Skill Kit functionality.

## How roles work in AI Skill Kit

Three separate role concepts apply when you build and deploy a custom skill. Understanding the difference helps you plan access before you start and troubleshoot permission errors after you deploy.

-   **Roles required to use the AI Skill Kit**

    There are some roles that users need to perform an activities in AI Skill Kit, such as installing the plugin, building a skill, or activating a published skill. These roles are assigned to the people on your team who build and manage skills. For a list of the roles required for each activity, see the [Roles required for common tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.md) table.

-   **Roles required to trigger skills**

    These are roles a user must have to trigger a published skill on your instance. These roles are configured within the skill configuration as part of its access control list \(ACL\). The ACLs are separate from the roles required to build the skill. To learn more, see [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md).

-   **Roles that a skill runs under**

    The roles that a skill operates with while it runs, which control what data and actions the skill can access on behalf of the triggering user. These are configured on the skill as role restrictions. Role restrictions are also separate from the roles required to build the skill. To learn more, see [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md).


Two roles ship with AI Skill Kit:

-   **sn\_skill\_builder.admin** for building, editing, and publishing skills.
-   **sn\_skill\_builder.model\_admin** for managing the LLMs available to skills.

The platform **admin** role is also required at two points: to install AI Skill Kit and to activate a published skill in AI Admin Hub. In many deployments, one person holds all three roles.

**Note:** The ACL and role restriction concepts apply to the skill's runtime users, not to the people building the skill. If you're planning access for your build team, you only need the roles listed in the [Roles required for common tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.md) table.

## Roles required for common tasks in AI Skill Kit

Most work in AI Skill Kit requires the **sn\_skill\_builder.admin** role, including creating, cloning, editing, configuring, testing, evaluating, and publishing skills, and calling skills from scripts.

Two activities require the platform **admin** role instead: installing AI Skill Kit and activating a published skill in AI Admin Hub.

Triggering an activated skill from the UI requires whatever roles are configured in the skill's ACL. To learn more, see [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md).

**Parent Topic:**[AI Skill Kit reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-reference.md)

## Skill Kit admin \(sn\_skill\_builder.admin\)

Create, configure, test, and publish skills in AI Skill Kit. Assign this role to anyone developing skills on your instance.

### Contains roles

None.

### Groups

None. This role is not assigned to any groups by default.

### Tasks requiring this role

The **sn\_skill\_builder.admin** role is required for the following tasks:

-   [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md)
-   [Clone a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.md)
-   [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md)
-   [Configure a skill prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/configure-skill-prompt.md)
-   [Configure skill deployment settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/configure-skill-settings.md)
-   [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md)
-   [Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/add-a-tool.md)
-   [Add a retriever](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/add-retriever.md)
-   [Add a web search tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/add-web-search.md)
-   [Use prompt assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/use-prompt-assistance.md)
-   [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)
-   [Evaluate a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/evaluate-prompt.md)
-   [Finalize and publish a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/publish-skill.md)

### Special considerations

This role grants access to the AI Skill Kit application and all skill authoring functionality. It does not grant the ability to activate skills in AI Admin Hub. Activating skills requires the **admin** role.

When configuring access control lists \(ACLs\) for a skill, the roles you specify in the ACL determine which users can invoke the skill. The **sn\_skill\_builder.admin** role only controls who can author skills, not who can use them. To learn more about configuring skill ACLs, see [Configure security controls for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md).

## Skill Kit model admin \(sn\_skill\_builder.sb\_model\_admin\)

Create and update custom large language models for use with AI Skill Kit.

### Contains roles

None.

### Groups

None. This role is not assigned to any groups by default.

### Special considerations

This role is only required when working with custom large language models. AI developers who use the standard Now LLM Service provider or prebuilt external LLM spokes do not need this role. To learn more about provider options when creating a skill, see [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/create-new-skill.md).

This role does not replace the **sn\_skill\_builder.admin** role. AI developers who create skills using custom large language models require both roles.

