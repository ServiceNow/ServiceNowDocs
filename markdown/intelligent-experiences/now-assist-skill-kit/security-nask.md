---
title: Security for Now Assist Skill Kit
description: Enable security controls for Now Assist skills and custom skills through access control lists \(ACLs\) and user identities.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: concept
last_updated: "2025-09-04"
reading_time_minutes: 1
breadcrumb: [Exploring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Security for Now Assist Skill Kit

Enable security controls for Now Assist skills and custom skills through access control lists \(ACLs\) and user identities.

## Access control lists

The access control lists in Now Assist Skill Kit enhance the security of Now Assist skills and are set to determine users who can invoke a skill.

## Configure ACLs in Now Assist Skill Kit

You can configure ACLs for Now Assist Skill Kit when you create or edit a skill or when you activate a skill from Now Assist Admin console.

ACLs configured in Now Assist Skill Kit for are **Allow-If** and role-based.

The **Allow-If** logic grants access to data or resources if any of the conditions in the ACL are met. The other type of ACL is **Deny-Unless**. **Deny-Unless** ACLs block access to data or resources unless a condition is met, even if there are other conditions like **Allow-If** ACLs that would normally grant someone access.

There are two possible options for ACLs created in Now Assist Skill Kit:

-   **Any authenticated user**: Grants access to any user authenticated on the instance, regardless of role
-   **Select roles**: Requires you to select the roles that grant access

Each skill must have its own unique ACL. You can't create a skill or save changes to a skill without an ACL. To configure an ACL for a skill, see .

