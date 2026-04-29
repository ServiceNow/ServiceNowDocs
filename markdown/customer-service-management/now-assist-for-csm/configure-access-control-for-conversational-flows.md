---
title: Customize access control for conversational flows
description: You must define an access control list \(ACL\) for conversational flows. An ACL enables you to restrict who is able to access and execute a skill to only users with the correct role.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Customize access control for conversational flows

You must define an access control list \(ACL\) for conversational flows. An ACL enables you to restrict who is able to access and execute a skill to only users with the correct role.

## Before you begin

Role required: admin

The following flows include default ACLs for the sn\_customerservice\_agent or sn\_customerservice.consumer\_agent  role:

-   Add Comment to Task
-   Add Work Note to Task
-   Create Task for Case
-   Reassign Case

**Note:** An Access Control List \(ACL\) is already configured for these flows. The steps outlined below are only required if the customer intends to use these flows with a custom role.

To assign a custom role, follow the procedure:

## Procedure

1.  Navigate to **sys\_security\_acl** table.

2.  Filter by these ACL names:

3.  Add your custom role to each ACL record.


