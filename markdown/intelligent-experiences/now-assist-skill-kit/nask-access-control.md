---
title: Configure security controls for a skill
description: Define an access control list \(ACL\) and role restrictions for every skill. The ACL limits which user roles can access and run the skill, and role restrictions limit the roles that the skill runs with.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skill-kit/nask-access-control.html
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Configure security controls for a skill

Define an access control list \(ACL\) and role restrictions for every skill. The ACL limits which user roles can access and run the skill, and role restrictions limit the roles that the skill runs with.

## About this task

Existing skills without an ACL continue to run. However, if you edit the skill and republish it, you must add an ACL.

If you try to execute a skill when you don’t have permission, you see an error that you aren’t authorized.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

    A dialog box that explains ACLs appears. You can select **Got it** or **View skills without ACLs**.

2.  Add an ACL and role restrictions to an existing skill.

    1.  Select the skill that you want to add an ACL to.

    2.  Select the **Deployment and skill settings** tab and then select **Security controls**.

    3.  Select **Add ACL**.

    4.  Select an option.

<table id="table_h4k_kys_jgc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Any authenticated user

</td><td>

Any logged-in user can access and run the skill.

</td></tr><tr><td>

Select roles

</td><td>

Select the roles that a user must have to execute the skill. **Note:** If you select multiple roles, a user needs only one of the roles to run the skill.

</td></tr></tbody>
</table>    5.  Add role restrictions.

    6.  Select **Apply**.

3.  Add an ACL to a new skill.

    1.  [Create a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/create-new-skill.md).

    2.  In the **Configure security controls** section, select an option for the access control list.

    3.  Apply role restrictions to the skill.

    4.  Continue creating the skill.


**Parent Topic:**[Configuring AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure a skill prompt]()

[Configure deployment and skill settings]()

