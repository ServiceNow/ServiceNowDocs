---
title: Associate a playbook with a service definition
description: After creating a service definition, you can associate a playbook with the definition.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Associate a playbook with a service definition

After creating a service definition, you can associate a playbook with the definition.

## Before you begin

Role required: \(playbook\_experience.admin + sn\_csm\_case\_types.service\_definition\_manager\) or admin

## About this task

**Note:** To see the playbook record generator field and values on the list and form view, the service def manager needs the playbook\_experience.admin role in addition to sn\_csm\_case\_types.service\_definition\_manager. Please add this role to associate a playbook with a service definition.

A playbook provides agents with step-by-step guidance for resolving a specific type of case. If a service definition has an associated playbook, the agent can use the playbook in a tab on the case record.

When the agent selects **Create Case** on the [case type selector screen](../concept/csm-case-type-select-modals.md), the system displays the new case record and launches the playbook associated with the service in a tab on the record page.

**Note:** This is an optional task.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select a service definition.

3.  Select a playbook record generator in the **Playbook record generator** field.

    This field is a reference to the Playbook Experience Record Generator table \(sys\_playbook\_experience\_record\_generator\). For more information, see Playbook record generator

4.  Select **Update**.


