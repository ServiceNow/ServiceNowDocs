---
title: Workflow scope
description: Workflow application scope determines the access that an application has to the information in a workflow, specifically to the data contained in the activities in that workflow.There are some restrictions to public and private application scopes.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflow concepts, Classic Workflow, Build workflows]
---

# Workflow scope

Workflow application scope determines the access that an application has to the information in a workflow, specifically to the data contained in the activities in that workflow.

When a workflow is created, it inherits the application scope from the gear menu for the logged in user. This scope cannot be changed in the Workflow Editor. When the workflow executes, it runs in this scope and can only be called from a different application if the workflow’s accessibility setting permits access to all scopes \(public\). Otherwise, the workflow’s application scope is private to the application.

**Note:** Any script that is created in the Workflow Editor, such as an advanced script in an If activity, runs in the scope of the workflow. All core activities provided in the base system or for Orchestration run in the scope of the workflow.

Custom activities run in their own scope, even if it is different from that of the workflow. The scope of a custom activity can be private or public. Any script that runs inside a custom activity with a scope can only access outside artifacts that are within the scope of that activity or artifacts that are configured to run in any scope. Conversely, an outside artifact can only access the script inside that private activity if the outside artifact is running in the same scope. Activities with public scopes can interact with outside artifacts in any application scope.

You can use private activities as part of a workflow that has a public application scope. These activities are protected from reaching outside of the workflow or from being reached from outside the workflow. For details about setting application scoping for custom activities, see the field description table for the appropriate activity template.

**Note:** Custom activities uploaded to the ServiceNow Store must be configured as accessible to all application scopes.

## Workflow scope restrictions

There are some restrictions to public and private application scopes.

During runtime, publicly scoped workflows can access other application resources, as long as these resources are set to be accessible to all application scopes. Privately scoped workflows in a private application scope can only access resources private to its scope. Due to scope access boundaries, any privately scoped workflows that make calls out to other scoped resources fail with either an exception or a hung activity while waiting for returned results. This occurs when making calls to these common global resources:

-   ECC queues
-   Tasks
-   Approvals
-   Events
-   SLA timers
-   Timers
-   Script includes
-   Business rules
-   Workflow APIs

As you design workflows, validate the visibility and accessibility of all resources prior to deployment.

See [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

For information on how to configure the scope for a workflow, see [Workflow properties](../../workflow-administration/reference/r_WorkflowProperties.md).

