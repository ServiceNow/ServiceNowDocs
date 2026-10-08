---
title: Access control rules
description: Access control rules operate at the platform level, independently of playbook permissions. A user can satisfy every playbook permission and still be blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/access-control-rules-playbooks.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing playbook permissions, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Access control rules

Access control rules operate at the platform level, independently of playbook permissions. A user can satisfy every playbook permission and still be blocked.

Playbook tables are subject to access control rules in the same way as any other table. Access control rules are the platform-level access mechanism and operate independently of playbook permissions. For general information, see [Access Control Lists \(ACLs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control-rules.md).

Because the two are independent, a user can satisfy every playbook permission and still be blocked by an access control rule. The following sections cover where this happens.

## Content access filtering

Access control rules for read operations on playbook tables can call into content access filtering and resource filter rule logic. A user can be blocked by an access control rule even when a content filtering rule grants access to the same content.

**Note:** When a user can't see content that a content filtering rule grants them, check the access control rules on the playbook table before revising the filtering rule.

## Completing and skipping activities

Whether a user can complete or skip an activity depends on write access to that activity's Experience Status record, which is usually a Flow Data record. This dependency is separate from playbook roles, content access filtering, and runtime permissions.

A non-admin user has write access to a Flow Data record in three cases.

-   The **Assignment Group** and **Assigned to** fields are both empty, so any user can write to the record.
-   The **Assignment Group** field is empty and the user is named in the **Assigned to** field.
-   The **Assignment Group** field names a group that the user belongs to.

To give a user access to complete an activity, set the **Assigned to** field on the Flow Data record to that user. Alternatively, set the **Assignment Group** field and add the user to that group.

Access is enforced by access control rules on the sys\_flow\_data table.

**Note:** When a user can see an activity but can't complete it, check the **Assignment Group** and **Assigned to** fields before reviewing playbook roles or runtime permissions.

## Public access playbooks

Guest users reach the playbook runtime through access control rules on the runtime APIs and messaging channels. Those rules determine what an unauthenticated user can retrieve. Guest users also need access to the parent record.

For the rules required and how to configure them, see [Configure guest user access to playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-guest-user-access.md). For the roles and restrictions that apply, see [Public access playbooks permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/public-access-playbooks-permissions.md).

**Parent Topic:**[Managing playbook permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-permissions.md)

