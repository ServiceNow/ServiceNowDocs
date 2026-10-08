---
title: Customize access control for conversational flows
description: You must define an access control list \(ACL\) for conversational flows. An ACL enables you to restrict who is able to access and execute a skill to only users with the correct role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/configure-access-control-for-conversational-flows.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, ServiceNow Otto for CSM, Customer Service Management]
---

# Customize access control for conversational flows

You must define an access control list \(ACL\) for conversational flows. An ACL enables you to restrict who is able to access and execute a skill to only users with the correct role.

## Before you begin

Role required: admin

The following flows include default ACLs for the sn\_esm\_agent role:

-   Add Comment to Task
-   Add Work Note to Task
-   Create Task for Case
-   Reassign Case

**Note:** An Access Control List \(ACL\) is already configured for these flows.

To assign a custom role, follow the procedure:

## Procedure

1.  Navigate to **sys\_security\_acl** table.

    The user can use the conversational subflows and actions on the case tables which they have access to. The conversational subflows and actions are executed on the case record based on the case table level access control \(ACL\).

2.  To use on the base system case table \(sn\_customerservice\_case\), add sn\_esm\_agent role to the user.

3.  To use on the custom case table, add the corresponding role \(which has access to the table\) to the user.

    For more information, see [Conversational actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/conversational-actions.md)


