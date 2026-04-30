---
title: Create application records from improvement initiatives
description: Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.
locale: en-US
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Improvement integration with other applications, Overview, Continual Improvement Management, IT Service Management]
---

# Create application records from improvement initiatives

Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.

## Before you begin

Role required: sn\_cim.improvement\_coordinator or sn\_cim.improvement\_manager

## Procedure

1.  Navigate to your improvement initiative or CIM task record.

    -   Improvement initiative: **All** &gt; **Continual Improvement** &gt; **My CIM Initiatives**
    -   CIM task: **All** &gt; **Continual Improvement** &gt; **CIM Tasks**
2.  Find and open the Improvement Initiative or CIM task record from which you want to create an application record.

3.  Create an application record by selecting the corresponding application record link in the Related Links section.

    **Note:** Related links are visible only when a CIM task is in the Open, Work in Progress, or On Hold state.

    |Record type|Link to select|
    |-----------|--------------|
    |Demand|Create Demand|
    |Project|Create Project|
    |Coaching opportunity|Create Coaching Opportunity|
    |Knowledge base articles|Create Knowledge|
    |Agile Development story|Create Story|
    |Performance Analytics automated indicator|Create PA Indicator|
    |Change|Create Change|

    **Note:**

    Default field values set in the **sn\_cim.initiative\_copy\_attributes** property are populated in the application record form. Contact your administrator to edit this property by adding or deleting fields. For more information, see [Configure CIM integration property](configure-cim-int-property.md).

4.  Select **Submit**.


## Result

The application record is created and UI changes display on the source improvement initiative or CIM task record and corresponding application records. For more information, see [Updates after application record creation from improvement initiatives](../reference/updates-app-record-from-initiative.md).

**Parent Topic:**[Improvement integration with other applications](../reference/cim-integration.md)

