---
title: Activity scoping
description: Custom activities run in their own scope, even if it is different from that of the workflow.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activity scoping

Custom activities run in their own scope, even if it is different from that of the workflow.

Any script that runs inside a custom activity with a scope can only access outside artifacts that are within the scope of that activity or artifacts that are configured to run in any scope. Conversely, an outside artifact can only access the script inside that private activity if the outside artifact is running in the same scope. Activities with public scopes can interact with outside artifacts in any application scope.

You can use private activities as part of a workflow that has a public application scope. These activities are protected from reaching outside of the workflow or from being reached from outside the workflow. For details about setting application scoping for custom activities, see the field description table for the appropriate [activity template](https://www.servicenow.com/docs/access?context=c_ActivityDesignerComponents&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

**Note:** Custom activities uploaded to the ServiceNow Store must be configured as accessible to all application scopes.

**Parent Topic:**[Orchestration activity designer](c_WorkflowActivityDesigner.md)

