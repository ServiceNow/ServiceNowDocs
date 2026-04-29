---
title: Using indicator templates
description: Indicators collect data to monitor a single control or risk. Indicator templates allow you to create multiple indicators for similar controls or risks. The Technology Controls Monitoring Accelerator application provides a collection of 171 predefined indicator templates for monitoring cybersecurity controls.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Technology Controls Monitoring Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Using indicator templates

Indicators collect data to monitor a single control or risk. Indicator templates allow you to create multiple indicators for similar controls or risks. The Technology Controls Monitoring Accelerator application provides a collection of 171 predefined indicator templates for monitoring cybersecurity controls.

## Indicators and Indicator templates

The indicators collect data to monitor the controls and risks and collect the audit evidence. Indicators monitor a single control or risk.

The indicator templates allow the creation of multiple indicators for similar controls or risks.

The indicator templates obtained with the Technology Controls Monitoring Accelerator application provide the instructions that you must run the indicators, as described in the following sections.

Supporting information can be collected for the indicators through automatic data collection or manual tasks. Indicator results are then used to perform the following tasks:

-   Create issues for the controls.
-   Update the risk scores.
-   Provide supporting information for the audit activities and control testing

The following types of indicators are available:

1.  Basic: Evidence is collected from on the source table.
2.  Manual: Evidence is not collected. This type of indicator requires a third party data source.
3.  Scripted: Evidence can be collected from multiple source tables.

## Flow of the indicator process

The indicator process consists of the following steps:

-   Set up the indicator template.
-   Apply the indicator template to a risk statement or control. When the control or risk statement is scoped with an entity type or specific entities, then all the controls or risks under that control objective or risk statement have an indicator generated for them.

Indicators can be automated or manual. The indicator tasks are generated that show the final state of the indicator.

## Examples of automated indicators and manual indicators

An example of an automated indicator would be to check that all servers in the CMDB are up to date. Another example would be that all LDAP passwords are less than three months old.

An example of a manual indicator would be to ask the network administrator to conduct the annual Network Penetration Tests are conducted and the results are attached to the task. If a result indicates failed or not passed, it is used to trigger the creation of GRC issues.

## Usage of indicator templates

You can link the indicator templates to the policy statements or risk statements so that the indicators are automatically created for the controls or risks. The status of the controls is also automatically calculated by the linked indicator results and it may affect any linked risks. For example, if the indicator tied to a control fails, then the overall status cannot be completed unless the remediation task is closed by the user.

The Calculated Risk Score for the risk is also adjusted automatically by the indicators results of the risk. The Indicator Failure Factor field in the Risk table displays the impact of the failures.

**Note:** Indicators are not weighted. When you weigh their impact on a control or risk, they are considered equalizing. Indicators are not executed when the risks and controls are in the **Retired** state.

## Indicator template collection frequency

Each indicator template includes a schedule for identifying the frequency of data collection, as shown here.

![Indicator template schedule tab](../image/indicator-template-schedule.png "Indicator template schedule")

<table id="table_schedule_tab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.-   Daily
-   Weekly: The day of the week to perform the collection.
-   Monthly: The day of the month to perform the collection.
-   Quarterly: The date of the first collection run.
-   Semi-Annually: The date of the first collection run.
-   Annually: The month and day to perform the collection.

</td></tr></tbody>
</table>## Indicator template collection method

The Method tab identifies how the results are collected, as shown here.

![Indicator template collection method](../image/indicator-template-method.png "Indicator template collection method")

|Field|Description|
|-----|-----------|
|Type|Results can be gathered manually using task assignment or automatically using basic filter conditions, Performance Analytics, or a script.|
|Target Type|Identifies whether the target is a percentage or a count.|
|Short Description|If **Type = Manual**, a brief description of the issue.|
|Instructions|If **Type = Manual**, instructions for the collection of indicator results.|
|Value Mandatory|If **Type = Manual**, the check box indicates whether the value is mandatory for the indicator task.|
|Passed/Failed|If **Type = Basic**, the conditions defined on the Supporting Data tab are met, and the results exceed the **Target** value, it indicates whether the indicator passed or failed.|
|Target|If **Type = Basic**, the threshold by which the results returned based on the conditions defined on the Supporting Data tab determine whether the indicator template passes or fails.|
|PA Threshold|If **Type = PA Indicator**, the associated PA Threshold.|
|Script|If **Type = Script**, the script that obtains the desired system information.|

## Indicator template supporting data

Starting with version 10.1, the Supporting Data tab displays actual historical data for the supporting data records from the indicator results or indicator tasks. In earlier versions, only the real-time state of the records collected could be viewed.

![Indication template supporting data](../image/indicator-template-supporting-data.png "Indicator template supporting data")

|Field|Description|
|-----|-----------|
|Collect supporting data|Indicates that you want to collect supporting data. The following three fields are displayed.|
|Table|The supporting data table.|
|Supporting Data Fields|The fields from the supporting data table to be considered.|
|Criteria|Filter conditions.|
|Use reference field|Indicates that you want to use a reference field. The following two fields are displayed.|
|Reference field|The reference field that you want to use for sampling.|
|Sample size|The number of records you want to use for data sampling.|

You can also view information on the following tabs:

-   Indicators
-   Control Objectives/Risk Statements
-   Content References

**Note:** The **Control Objectives/Risk Statements** tab allows you to reuse the same template for multiple control objectives or risk statements.

**Parent Topic:**[Technology Controls Monitoring Accelerator](../../grc-tech-controls-monitoring-accel/concept/tech-controls-monitoring-accel.md)

