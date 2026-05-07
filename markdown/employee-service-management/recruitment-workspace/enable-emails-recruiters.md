---
title: Enable recruiters to view email details in the activity stream
description: Add the recruiter role to a system property. The recruiter can view the details of the email in the activity stream of the Recruitment workspace.
locale: en-US
release: australia
product: Recruitment Workspace
classification: recruitment-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Recruitment Workspace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Enable recruiters to view email details in the activity stream

Add the recruiter role to a system property. The recruiter can view the details of the email in the activity stream of the Recruitment workspace.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for `glide.ui.activity.email_roles`.

3.  Select the **glide.ui.activity.email\_roles** property.

4.  In the **Value** field, add the `sn_ta_hiring_core.recruiter` role.

5.  Select **Update**.


**Parent Topic:**[Configuring Recruitment Workspace](../concept/config-recruitment.md)

