---
title: Glide events relative to workflows
description: Workflow uses several Glide events.
locale: en-US
release: xanadu
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow events in the base system, Workflow events, Workflow management, Classic Workflow, Build workflows]
---

# Glide events relative to workflows

Workflow uses several Glide events.

|Event|Description|Purpose|To Use|Source|Thread|Listeners|
|-----|-----------|-------|------|------|------|---------|
|Insert|Global event set upon the insert of a GlideRecord that causes the script engine, and through that the workflow engine, to wake up.|Starts workflows that are associated with the current GlideRecord either by reference, as in request items and SLA timers, or by conditions associated with the GlideRecord's table.|There is no explicit customer-facing use for this in a workflow. It is part of the Glide engine, and with this event, the only thing workflows can do is start. Workflows can also be started manually using a script.|Workflow Engine, RunEngine|Current thread, current mutex|User action of insert|
|Update|Global event set upon the update of a GlideRecord that causes the script engine, and through that the workflow engine, to wake up.|Looks to the Workflow Context \[wf\_context\] table to find running workflows that are associated with the current GlideRecord by document ID.|There is no explicit customer-facing use for this in a workflow. It is part of the Glide engine, and with this event, the only thing workflows can do is advance through the next set of transitions.|Workflow Engine, RunEngine|Current thread, current mutex|User action of update of a GlideRecord|
|Delete|Global event set upon the delete of a GlideRecord that causes the script engine, and through that the workflow engine, to wake up.|Looks to the Workflow Context \[wf\_context\] table to find running workflows that are associated with the current GlideRecord by document ID.|There is no explicit customer-facing use for this in a workflow. It is part of the Glide engine, and with this event, the only thing workflows can do is advance through the next set of transitions.|Workflow Engine, RunEngine|Current thread, current mutex|User action of delete of a GlideRecord|
|Query|Global event set upon the query of the Glide database that causes the script engine, and through that the workflow engine, to wake up.|Looks to the Workflow Context \[wf\_context\] table to find running workflows that are associated with the current GlideRecord by document ID.|There is no explicit customer-facing use for this in a workflow. It is part of the Glide engine, and with this event, the only thing workflows can do is advance through the next set of transitions.|Workflow Engine, RunEngine|Current thread, current mutex|User action of query of a GlideRecord|

**Parent Topic:**[Workflow events in the base system](r_WorkflowEventsInTheBaseSystem.md)

