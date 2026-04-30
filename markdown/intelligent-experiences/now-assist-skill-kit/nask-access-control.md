---
title: Configure security controls for a skill
description: You must define an access control list \(ACL\) and role restrictions for all skills. An ACL enables you to restrict who is able to access and execute a skill to only users with the correct role. Role restrictions enable users to limit roles during skill execution.
locale: en-US
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Configure security controls for a skill

You must define an access control list \(ACL\) and role restrictions for all skills. An ACL enables you to restrict who is able to access and execute a skill to only users with the correct role. Role restrictions enable users to limit roles during skill execution.

## About this task

If you have an existing skill that does not have an ACL, the execution of the skill is not disrupted. However, if you edit the skill and republish it, you must add an ACL.

If you try to execute a skill when you don’t have permission, you see an error that you aren’t authorized.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

    A modal appears to explain ACLs. You can select **Got it** or **View skills without ACLs**.

2.  Add an ACL and role restrictions to an existing skill.

    1.  Select the skill that you want to add an ACL to.

    2.  Select the **Deployment and skill settings** tab and then select **Security controls**.

    3.  Select **Add ACL**.

    4.  Select an option.

        ![User access dialog.](../image/nask-acl.png)

<table id="table_h4k_kys_jgc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Any authenticated user

</td><td>

As long as a user is logged in, they can access and execute the skill.

</td></tr><tr><td>

Select roles

</td><td>

Select the roles that a user must have to execute the skill. **Note:** If you select multiple roles, a user must only have one of the roles to execute the skill.

</td></tr></tbody>
</table>    5.  Add role restrictions.

    6.  Select **Apply**.

3.  Add an ACL to a new skill.

    1.  [Create a skill](create-new-skill.md).

    2.  In the **Configure security controls** section, select an option for the access control list.

    3.  Apply role restrictions to the skill.

    4.  Continue creating the skill.


**Parent Topic:**[Configuring Now Assist Skill Kit](../concept/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure a skill prompt](configure-skill-prompt.md)

[Configure skill deployment settings](configure-skill-settings.md)

