---
title: Customize access control for suggested steps
description: Replace the default sn\_esm\_agent role with a custom role.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-08-20"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure Now Assist for Customer Service Management \(CSM\), Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Customize access control for suggested steps

Replace the default sn\_esm\_agent role with a custom role.

## Before you begin

Role required: admin

## Procedure

1.  Update role permissions

    In the sys\_user\_role table, open your custom role and add sn\_gaf.data\_writer to the Contains Role related list.

2.  Update ACLs

    In the sys\_security\_acl table, filter for ACL names starting with gaf\_suggested\_steps\_csm. Add your custom role to each of the four matching records.

3.  Configure skill access

    In Now Assist Admin, complete the setup for the CSM Suggested Steps Generation skill:

    -   Add your custom role in the **Define Access** step.
    -   Add the same role in the **Select Display** step.

## Result

By default, the sn\_esm\_agent role is used. These steps allow you to configure a custom role if needed.

