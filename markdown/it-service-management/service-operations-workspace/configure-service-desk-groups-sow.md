---
title: Configure service desk groups to access the Service Operations Workspace landing page
description: Ensure that the right users have access to the Service Operations Workspace landing page.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access controls in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure service desk groups to access the Service Operations Workspace landing page

Ensure that the right users have access to the Service Operations Workspace landing page.

## Before you begin

Role required: admin

## About this task

The landing page's access is based on the audience associated with that page. Configure the audiences with the required service desk groups and the users that are part of these service desk groups can then access the landing page. If you want users from multiple service desk groups to access the landing page, you should configure the landing page's audience with all those service desk groups.

It is applicable only for an instance that has Service Operations Workspace 1.1 installed and has upgraded to Australia.

## Procedure

1.  Configure the system property for landing page access by performing the following steps.

    1.  From the **All** menu, navigate to **sys\_properties.list**.

    2.  To ensure that the user criteria records are used instead of roles to access the landing page, set the **glide.ux.user\_criteria\_enabled** property to `true`.

    3.  Select **Update**.

2.  Add the user's service desk groups to the audience's user criteria by performing the following steps.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Building Blocks** &gt; **Audiences**.

    2.  Select an audience and perform the following steps, for example, **SOW Service Desk Audience**.

        1.  From the **User Criteria Inclusions** related list, open the audience, for example, **Service Desk Group Inclusion**.
        2.  For the **Groups** field, add the required service desk group that the user is part of.
        3.  Select **Update**.

