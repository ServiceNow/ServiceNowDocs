---
title: Configure automatic closure of past conversations
description: Use a system property to define whether a batch job can automatically close conversations that have transpired.
locale: en-US
release: zurich
product: Career Conversations
classification: career-conversations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Career Conversations, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Configure automatic closure of past conversations

Use a system property to define whether a batch job can automatically close conversations that have transpired.

## Before you begin

Role required: admin \[sn\_egd\_act.admin\]

## Procedure

1.  Navigate to the **All** menu, and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  In the **Search** field that appears underneath the Name column, enter `*egd`.

    A list of system properties associated with the Talent Developmentsuite of applications appears.

3.  Select the **sn\_egd\_act.automatic\_close** property.

4.  Use the **Value** field to specify the option that enables or deactivates a batch job from automatically closing past conversations.

    |Option|Description|
    |------|-----------|
    |**True**|The job will close past conversations.|
    |**False**|The job will not close past conversations.|

5.  Select **Update**.


**Parent Topic:**[Install and configure Career Conversations](../concept/egd-activities-install-config.md)

