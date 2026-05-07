---
title: Now Assist Skill Kit roles
description: Certain roles are required to use Now Assist Skill Kit functionality.Create, configure, test, and publish skills in Now Assist Skill Kit. Assign this role to anyone developing skills on your instance.Create and update custom large language models for use with Now Assist Skill Kit.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Now Assist Skill Kit reference, Now Assist Skill Kit, Enable AI experiences]
---

# Now Assist Skill Kit roles

Certain roles are required to use Now Assist Skill Kit functionality.

Now Assist Skill Kit uses two distinct roles that map to the two main user types. AI developers who create and manage skills require the **sn\_skill\_builder.admin** role. Platform administrators who install Now Assist Skill Kit and activate published skills require the **admin** role. These are separate responsibilities that may be held by the same person or by different people depending on your organization.

|Role|User type|Used for|
|----|---------|--------|
|**sn\_skill\_builder.admin**|AI developer|Creating, configuring, and publishing skills and prompts. Required for all skill authoring tasks including adding tools, testing, evaluating, and configuring security controls.|
|**admin**|Now Assist admin|Installing Now Assist Skill Kit, activating published skills in Now Assist Admin, and calling custom skills from scripts.|
|**sn\_skill\_builder.sb\_model\_admin**|AI developer|Creating and updating custom large language models for use with Now Assist Skill Kit.|

**Note:** The **sn\_skill\_builder.admin** role must be assigned to AI developers after Now Assist Skill Kit is installed. It is not assigned automatically. To learn more about installation, see .

**Parent Topic:**[Now Assist Skill Kit reference](na-skill-kit-reference.md)

## Skill Kit admin \(sn\_skill\_builder.admin\)

Create, configure, test, and publish skills in Now Assist Skill Kit. Assign this role to anyone developing skills on your instance.

### Contains roles

None.

### Groups

None. This role is not assigned to any groups by default.

### Tasks requiring this role

The **sn\_skill\_builder.admin** role is required for the following tasks:

-   [Create a skill](../task/create-new-skill.md)
-   [Clone a skill](../task/clone-and-edit-servicenow-skill.md)
-   [Create a prompt](../task/create-prompt-template.md)
-   [Configure a skill prompt](../task/configure-skill-prompt.md)
-   [Configure skill deployment settings](../task/configure-skill-settings.md)
-   [Configure security controls for a skill](../task/nask-access-control.md)
-   [Add a tool](../concept/add-a-tool.md)
-   [Add a retriever](../task/add-retriever.md)
-   [Add a web search tool](../task/add-web-search.md)
-   [Use prompt assistance](../task/use-prompt-assistance.md)
-   [Test a prompt](../task/test-prompt-template.md)
-   [Evaluate a prompt](../task/evaluate-prompt.md)
-   [Finalize and publish a skill](../task/publish-skill.md)

### Special considerations

This role grants access to the Now Assist Skill Kit application and all skill authoring functionality. It does not grant the ability to activate skills in Now Assist Admin. Activating skills requires the **admin** role.

When configuring access control lists \(ACLs\) for a skill, the roles you specify in the ACL determine which users can invoke the skill. The **sn\_skill\_builder.admin** role only controls who can author skills, not who can use them. To learn more about configuring skill ACLs, see [Configure security controls for a skill](../task/nask-access-control.md).

## Skill Kit model admin \(sn\_skill\_builder.sb\_model\_admin\)

Create and update custom large language models for use with Now Assist Skill Kit.

### Contains roles

None.

### Groups

None. This role is not assigned to any groups by default.

### Special considerations

This role is only required when working with custom large language models. AI developers who use the standard Now LLM Service provider or prebuilt external LLM spokes do not need this role. To learn more about provider options when creating a skill, see [Create a skill](../task/create-new-skill.md).

This role does not replace the **sn\_skill\_builder.admin** role. AI developers who create skills using custom large language models require both roles.

