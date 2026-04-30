---
title: Set up a record generator for case type
description: Create a record for a case type by using a playbook record generator. With a record generator, the system creates a record as the first step in the playbook.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Playbooks for Customer Service Management, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up a record generator for case type

Create a record for a case type by using a playbook record generator. With a record generator, the system creates a record as the first step in the playbook.

## Before you begin

Role required: playbook\_experience.admin

## About this task

A record generator is set up for a specific table. You can specify the name of the record generator activity, the form view, and the playbook that a user sees before a record is created. You can also configure the declarative action that are used to submit the form. For more information on declarative actions, see [Declarative actions](../concept/migration-form-declarative-actions.md).

## Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Record Generators**.

2.  Select **New**.

3.  Fill in the fields on the form.

4.  |Field|Description|
|-----|-----------|
|Table|Table that the new record page should use for the record generator entry.|
|Process Definition|Process definition that you want to display before a record is created. All activities are marked pending. If no process is running after the record is created, a playbook manually triggers this process definition.|
|Create Record Activity Name|Name to display on the record generator activity that is inserted as the first step within the specified process definition.|
|Active|Option to activate the record generator.|
|Order|Integer that determines the precedence of this configuration in relation to other activities in a Playbook experience. The lower the number means that it's more likely a user selects it over another configuration. Use numbers that are in the hundreds. For example, 100, 200, 300, or 400.|
|Create Record Form View|Form view for the new record form embedded within the inserted activity.|
|Template Fields|Optional field values that can be pre-filled in the new record form.|

5.  Select **Submit**.


