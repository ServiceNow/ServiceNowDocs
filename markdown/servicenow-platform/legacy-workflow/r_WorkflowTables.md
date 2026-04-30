---
title: Workflow tables
description: For full flexibility, workflows store information over a number of different tables.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflow concepts, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflow tables

For full flexibility, workflows store information over a number of different tables.

Usually tables containing workflow information are not edited one-by-one. Instead, use the Workflow Editor to edit workflows. The following lists are provided for reference purposes.

|Table|Description|
|-----|-----------|
|Workflows|
|Column Renderer \[column\_renderer\]|A renderer widget for a stage column. Stage renderers are written in Jelly as a UI Macro. The default is Workflow-Driven; it covers most workflow related stage scenarios.|
|Version \[wf\_versionable\]|Tracks different versions of element definitions \[wf\_element\_activity\].|
|Workflow \[wf\_workflow\]|The primary records of workflows.|
|Workflow Binding \[wf\_workflow\_binding\]|History of workflows run and the triggering record. Workflow Binding records prevent the system from running workflows again when the associated Workflow Context record has been deleted.|
|Workflow Context \[wf\_context\]|Individual instances of a workflow being used.|
|Workflow Execution \[wf\_workflow\_execution\]|Synthetic "current" records for workflows that run on Global.|
|Workflow Instance \[wf\_workflow\_instance\]|Connections of workflows to subflows.|
|Workflow Version \[wf\_workflow\_version\]|Particular versions of a workflow, either published versions or versions that have been checked out.|
|Activities|
|Activity Designer \[wf\_element\_activity\]|Custom activity definitions.|
|Activity Variables \[wf\_activity\_variable\]|Variables for activities.|
|Workflow Activity \[wf\_activity\]|Activities as they are being used in workflows.|
|Workflow Activity Definition \[wf\_activity\_definition\]|Definitions of activities that can be used in a workflow.|
|Workflow Executing Activity \[wf\_executing\]|Individual instances of activities being performed in active contexts.|
|Workflow components|
|Element Provider \[wf\_element\_provider\]|Template definitions for custom activities.|
|Group approval \[sysapproval\_group\]|Group-level approvals.|
|Variable \[item\_option\_new\]| |
|Workflow Condition \[wf\_condition\]|All of the defined conditions in workflows.|
|Workflow Element Definition \[wf\_element\_definition\]|Parent table for activity definitions.|
|Workflow Estimated Runtime Configuration \[wf\_estimated\_runtime\_config\]|Runtime performance data for completed workflows.|
|Workflow Queued Command \[wf\_command\]|Temporary internal storage for workflows that are currently executing.|
|Workflow SC Variable \[wf\_variable\]|The Service Catalog variables for a workflow.|
|Workflow Schedule \[wf\_workflow\_schedule\]|Definitions of the times to run specific workflows.|
|Workflow Timing \[wf\_workflow\_timing\]|Timing performance data for workflows.|
|Workflow Transition \[wf\_transition\]|All of the defined transitions in workflows.|
|History|
|Workflow Activity History \[wf\_history\]|The history of executed activities.|
|Workflow Log Entry \[wf\_log\]|All of the events and history of the workflow.|
|Workflow Transition History \[wf\_transition\_history\]|The history of executed transitions.|
|Stages|
|Stage Default \[wf\_stage\_default\]|Definitions of default stage fields for tables to use.|
|Stage Set \[stage\_set\]|A named set of stages that can be used to populate workflow stages for multiple workflows.|
|Stage Set Entry \[stage\_set\_entry\]|The stages that belong to a named stage set.|
|Stage Set for Table \[stage\_set\_table\]|Defines a relationship of a stage set to a table so that the stage set can be used as the default stages when a new workflow is created for the table. This replaces the wf\_default\_stage table and is the view that shows when you click **Default Stages \(by table\)** in the menu.|
|Workflow Stage \[wf\_stage\]|Definitions of stages used by workflows.|

