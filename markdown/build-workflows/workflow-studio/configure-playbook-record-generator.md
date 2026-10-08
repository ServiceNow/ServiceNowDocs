---
title: Configure a playbook record generator
description: Configure a record generator to let a user create the parent record for a process from inside the Playbook Experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/configure-playbook-record-generator.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-15"
reading_time_minutes: 1
breadcrumb: [Playbook record generator, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Configure a playbook record generator

Configure a record generator to let a user create the parent record for a process from inside the Playbook Experience.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Record Generators**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Table|Table whose new-record experience uses this record generator.|
    |Process Definition|Process definition shown to the user before the record is created. If record creation doesn't trigger a process definition on its own, the playbook manually starts this one.|
    |Create Record Activity Name|Label of the dynamically inserted first activity that contains the new record form.|
    |Create Record Form View|Form view embedded in the record generator activity.|
    |Template fields|Optional initial values for the new record.|

4.  If more than one record generator applies to the same table, set the Order field to control which one is selected by default.

    The record generator with the lowest Order value is selected by default. A caller can override this default by supplying a `processDefinitionId` or `recordGeneratorId` in the query passed to the playbook component. If both are supplied, `recordGeneratorId` takes precedence — use it when more than one record generator shares the same process definition.

5.  Select **Submit**.


## Result

The record generator is configured for the specified table.

## What to do next

To invoke the record generator, bind the playbook component on your record page to the target table and pass a sysId of `-1`. The component uses these values to find the applicable record generator for the table and open its form rather than load an existing record. This binding and the related event handling are part of general UI Builder page design, not specific to the record generator:

-   Bind Parent Table to `@context.props.table`.
-   Bind Parent SysId to `@context.props.sysId`, using `-1` to invoke record creation.
-   Handle the **Playbook Record Generated** event that the component dispatches on creation. Its payload contains the new record's table and sysId — use these to update your page context or route to the new record.

To customize the values submitted with the form, use the playbook component's query property, which can source values from URL parameters, to override the configured Template fields.

To customize the **Continue** button's label, styling, or conditions, create a declarative action with the same name and associate it with a custom Playbook Experience.

