---
title: Threat Intelligence Orchestration workflows and activities
description: The base system includes workflows and workflow activities you can use to automate actions on your instance.The Threat Intelligence - Run IoC Lookup workflow checks whether there is an unexpired observable and if so, the lookup is set to Complete and updated with the data from the observable.If an unexpired observable is found, the Threat Intelligence Orchestration - Populate lookup with observable workflow activity supplies data from an existing observable to a lookup. This activity can accelerate the investigation and remediation process.The Threat Intelligence Orchestration - Perform IoC Lookup workflow activity performs a given lookup. This activity can accelerate the investigation and remediation process.The Threat Intelligence Orchestration - Update observable with lookup result workflow activity updates the observable record. If one does not exist, it creates a new observable. This activity is useful for logging information.When triggered by a workflow, Threat Intelligence - Run Default IoC Lookup Sources takes in a lookup request ID and creates multiple lookups depending on the entered data values.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Threat Intelligence Orchestration, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Threat Intelligence Orchestration workflows and activities

The base system includes workflows and workflow activities you can use to automate actions on your instance.

**Parent Topic:**[Threat Intelligence Orchestration](c_ThreatIntelligenceOrchestration.md)

## Threat Intelligence - Run IoC Lookup workflow

The **Threat Intelligence - Run IoC Lookup** workflow checks whether there is an unexpired observable and if so, the lookup is set to **Complete** and updated with the data from the observable.

### Before you begin

Role required: sn\_si.basic

**Note:** This workflow replaces Threat Intelligence Orchestration business rules \(**Populate with existing IoC tables**, **Queue the lookup**, and **Update observable**\) with activities.

If a lookup is inserted or updated and meets the conditions, the Lookup business rule triggers this workflow.

### About this task

The **Threat Intelligence - Run IoC Lookup**workflow checks whether there is an unexpired observable and if so, the lookup is set to **Complete** and updated with the data from the observable. Any indicators associated with the observable are reactivated.

If the observable is expired, the workflow runs the lookups and increments the **Sighting count** in the existing, expired observable.

If no correlating observable exists, a new observable with indicator is created.

Workflow process activities include:

-   [Populate lookup with observable activity](threat-orch-wfs-and-activities.md#)
-   [Perform IoC Lookup activity](threat-orch-wfs-and-activities.md#)
-   Wait for lookup \(core activity\)
-   [Update observable with lookup result activity](threat-orch-wfs-and-activities.md#)

![Threat Intelligence - Run IoC Lookup workflow diagram](../image/RunScanWorkflow.png "Threat Intelligence - Run IoC Lookup workflow")

### Populate lookup with observable activity

If an unexpired observable is found, the **Threat Intelligence Orchestration - Populate lookup with observable** workflow activity supplies data from an existing observable to a lookup. This activity can accelerate the investigation and remediation process.

When triggered by a workflow **Populate lookup with observable** attempts to find an existing observable for a lookup that matches the **value** and **type** of the lookup provided to the activity as input.

If the observable exists and is not expired, this activity:

-   Updates the lookup with the information found in the observable
-   Reactivates an indicator if it is inactive, increments the **Encountered count**, and updates the **Last seen** date
-   Sets **State** to Complete.

#### Input variables

Input variables determine the initial behavior of the activity.

|Input variable|Description|
|--------------|-----------|
|scanID\[string\]|lookup identifier|

#### Output variables

The output variables contain data that can be used in subsequent activities.

|Output variables|Description|
|----------------|-----------|
|True|Found valid observable and updated lookup.|
|False|Did not find valid observable. Observable is either missing or expired.|

### Perform IoC Lookup activity

The **Threat Intelligence Orchestration - Perform IoC Lookup** workflow activity performs a given lookup. This activity can accelerate the investigation and remediation process.

When triggered by a workflow, **Perform IoC Lookup** takes a scanID, looks up the lookup record, and adds the lookup to the queue by creating a lookup queue entry.

#### Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|scanID\[string\]|lookup identifier|

#### Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|True|Triggered the lookup.|
|False|Did not trigger the lookup.|

### Update observable with lookup result activity

The **Threat Intelligence Orchestration - Update observable with lookup result** workflow activity updates the observable record. If one does not exist, it creates a new observable. This activity is useful for logging information.

When triggered by a workflow **Update observable with lookup result** updates an existing observable to include the new **Sighting count**, adds a note, and, if inactive, reactivates any indicators. The **Encountered count** and **Last seen** date in the indicator are also updated.

If no correlating observable exists, the workflow creates a new observable with indicator as follows:

-   Runs the IoC lookups
-   Creates a new observable
-   Creates an indicator for the observable
-   Adds a **Sighting count** to the observable
-   Adds an **Encountered count** and **Last seen** date to the indicator
-   Adds a message indicating from which lookup it was created

.

#### Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|scanID\[string\]|Lookup identifier.|

#### Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|True|Update or creation of observable is successful.|
|False|Update or creation of observable failed.|

### Run Default IoC Lookup Sources activity

When triggered by a workflow, Threat Intelligence - **Run Default IoC Lookup Sources** takes in a lookup request ID and creates multiple lookups depending on the entered data values.

For each data type, the **include\_in\_bulk scan** column of the supported lookup type table of each lookup source is evaluated. If true, a lookup is added to the lookup request.

#### Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|scan\_request\_id|Lookup request system identifier|

#### Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|Number of scans created|Integer|

