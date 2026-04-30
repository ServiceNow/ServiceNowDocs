---
title: Agentic Playbooks user roles
description: The following roles are required for runtime users to access Agentic Playbooks, and come with the Now Assist for Platform AI agents skill.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-09-05"
reading_time_minutes: 1
breadcrumb: [Reference, Agentic Playbooks, Playbooks, Explore, Workflow Studio, Build workflows]
---

# Agentic Playbooks user roles

The following roles are required for runtime users to access Agentic Playbooks, and come with the Now Assist for Platform AI agents skill.

You can grant users entitlement to the applications that you purchase on the ServiceNow AI Platform by allocating subscriptions in Subscription Management. You allocate subscriptions by adding one or more groups with measured roles to a product subscription.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and contact your account representative.

## Runtime user roles

Ensure that your runtime users have the following roles assigned to them:

<table id="table_smr_lgr_ygc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

playbook.agent\_user

</td><td>

Grants access to all standalone playbook agents.

</td></tr><tr><td>

playbook.agentic\_workflow\_user

</td><td>

Grants access to the Playbook Activity Assist Workflow, and includes:-   All agent-specific roles used within the workflow
-   The now\_assist\_panel\_user role \(for Now Assist Panel integration\)

</td></tr></tbody>
</table>**Note:** There are no roles specific to Agentic Playbooks for playbook authors. As long as a playbook author has admin, playbook.admin, pd\_author, or playbook.write rights, they can configure an activity to use AI agents.

**Parent Topic:**[Agentic Playbooks reference](agentic-playbook-reference.md)

