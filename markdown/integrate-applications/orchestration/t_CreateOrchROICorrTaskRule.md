---
title: Create an Orchestration ROI correlated task rule
description: The correlated task rule applies configurable conditions to fields in a selected table that tell the instance which manual tasks correspond to an automation entry record.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Orchestration ROI, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Create an Orchestration ROI correlated task rule

The correlated task rule applies configurable conditions to fields in a selected table that tell the instance which manual tasks correspond to an automation entry record.

## Before you begin

Role required: orchestration\_manager

Before starting this procedure, make sure you have created [labor rate cards](t_CreateOrchROILaborRateCard.md) and the appropriate [automation entry records](t_CreateOrchROIAutoEntryRecord.md) for the automated tasks you want to evaluate.

## About this task

Create conditions that the system can use to correlate manual tasks to the automation entry. For example, a rule on the Incident \[incident\] table uses these conditions to correlate the employee on-boarding task to values configured in the Employee OnBoarding automation entry record:

-   **\[Subcategory\] \[is\] \[Employee OnBoarding\]**
-   **\[Sort description\] \[contains\] \[new employee\]**

When a new employee opens an incident to request services or assets which are typically handled manually, Orchestration applies the usual labor rate for the manual work to the potential automated solution, and then computes the actual savings.

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **ROI Task Correlation** &gt; **Correlated Tasks Rules**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Automation entry|Automation entry record that correlates to the manual task defined by these conditions. The entry record names the workflow used to automate the task and defines the labor rate used to calculate the cost of the task.|
    |Table|Table to filter, using these conditions. The rule selects records from this table that match the conditions. Information from these records is used to calculate the actual time to perform a manual task and the actual volume for that manual task.|
    |Condition|Condition builder to use to filter records for this table. Use these conditions to identify all manual tasks correlated to this automation entry.|
    |Read-only fields|
    |Processed on|Date and time that the system performs the matching records lookup. The system automatically searches for new manual tasks matching these conditions.|

4.  Select one of these submission options:

    -   **Submit**: Saves the record to the table without running any calculations.
    -   **Submit and process now**: Saves the record, looks up all matching tasks, and saves matching record information to the Correlated Tasks \[manual\_mapping\_records\] table.
5.  To view a rule, select the link in the **Table** column of the **Correlated Tasks Rules** related list for the automation entry you want to see.

6.  To view the list of tasks that match all correlated rules in the system, navigate to **Orchestration** &gt; **ROI Task Correlation** &gt; **Correlated Tasks**.

7.  To view the list of tasks that match this rule in the system, click **Correlated Tasks** under **Related Links** in this form


**Parent Topic:**[Orchestration ROI](../concept/c_OrchestrationROI.md)

