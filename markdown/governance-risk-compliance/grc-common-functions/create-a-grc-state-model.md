---
title: Create a GRC state model
description: Create a GRC state model to define the states a table's records move through so an issue workflow can use it to control its lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/create-a-grc-state-model.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Issue workflows, Common GRC features, Governance, Risk, and Compliance]
---

# Create a GRC state model

Create a GRC state model to define the states a table's records move through so an issue workflow can use it to control its lifecycle.

## Before you begin

Role required: sn\_grc\_issue\_mgmt.issue\_workflow\_admin

## About this task

A GRC state model defines the states that records move through, the transitions between those states, and how the lifecycle is displayed in the stepper component. You can associate a state model with an issue workflow to define the workflow's lifecycle. A GRC state model can be used across GRC applications, including Issue Management, Risk, and AI Governance.

## Procedure

1.  Navigate to **All** &gt; **GRC State Model** &gt; **GRC State Models**.

2.  Select **New**, or open an existing state model to edit it.

3.  Fill in the state model fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|A name for the state model.|
    |**Table name**|The table that the state model applies to.|
    |**State model**|The field on the target table that stores which state model applies to the record.|
    |**State field**|The field that stores the current state of the record. For most tables, the default value is State \[state\].|
    |**Application**|The application scope for the state model. Defaults to Global.|
    |**Active**|Indicates whether the state model is available for use. Selected by default.|

4.  Select **Submit**.


## Result

The state model record is created and is active by default, with no states yet defined.

## What to do next

Add states to the model. See [Add a state to a GRC state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/add-a-state-to-a-grc-state-model.md).

**Parent Topic:**[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/issue-workflows.md)

