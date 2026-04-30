---
title: Configure Service Level Agreement \(SLA\) properties
description: You can configure the SLA engine, logging, and repair properties based on the requirements within your organization.Administrators can manage the SLA engine using SLA engine properties.Administrators can configure SLA logging using SLA properties.Administrators can manage the SLA repair function using system properties.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Configure Service Level Agreement \(SLA\) properties

You can configure the SLA engine, logging, and repair properties based on the requirements within your organization.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **Properties**.

2.  Select one of the following:

    -   **SLA Engine**

        configure properties for the SLA engine.

    -   **SLA Logging**

        configure logging properties for SLA Script Includes and logging output destination.

    -   **SLA Repair**

        configure properties for the SLA Repair process.


**Parent Topic:**[Service Level Management reference](../concept/service-level-management-reference.md)

## SLA engine properties

Administrators can manage the SLA engine using SLA engine properties.

Navigate to **Service Level Management** &gt; **Properties** &gt; **SLA Engine** to view SLA engine properties.

<table id="table_dfk_jkh_gr"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**com.snc.sla.calculation.percentage**

</td><td>

Maximum 'Actual elapsed percentage' value after which the 'SLA - update calculations' scheduled job will stop regularly calculating the SLA's time values. This is used to prevent 'long since breached' records from being unnecessarily updated. Setting to '0' will stop all calculations and leaving this blank will allow all SLAs to be calculated.

 By default, this is set to 1,000%, so that recalculation stops after the breach is exceeded by a factor of 10.

 -   Type: integer
-   Default value: 1000

</td></tr><tr><td>

**com.snc.sla.maximum\_duration**

</td><td>

Maximum duration in days that is allowed in the SLA definition.-   Type: integer
-   Default value: 1095

</td></tr><tr><td>

**com.snc.sla.engine.version**

</td><td>

Run the 2011 SLA engine \(2010, 2011\)

 -   Type: choice list
-   Default value: 2011

</td></tr><tr><td>

**com.snc.sla.engine.async**

</td><td>

Run the 2011 SLA engine asynchronously after task insert or update operations.

 -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**com.snc.sla.compatibility.breach**

</td><td>

Enable compatibility with 2010 'breached' status of SLAs \(default: false\)

 Only enable if you require the old way of showing breached status \(in the stage value\), for reporting purposes. Using only the 'breached flag' is preferred

 -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**com.snc.sla.default\_conditionclass**

</td><td>

The name of the Script Include class that will be used to evaluate SLA Conditions for the 2011 SLA engine \(use to override with your own extension of the SLAConditionBase class\)

 -   Type: String
-   Default value: SLAConditionBase

</td></tr><tr><td>

**com.snc.sla.workflow.run\_for\_breached**

</td><td>

An update to a Task can result in an SLA being attached that is already breached - for example when an Incident that has already been open for a while is upgraded to a high priority with a short resolution SLA.

 By default if there is a workflow specified in the SLA Definition it will not run if the Task SLA is attached and the Planned End Time has already passed.

 Enable this property if you would like the workflow to run for a Task SLA that is already breached when it is attached to the Task.

 -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**com.snc.sla.calculate\_planned\_end\_time\_after\_breach**

</td><td>

Continue to re-calculate the "Planned End Time" of SLAs after they have breached

 -   Type: true \| false
-   Default value: false

 **Note:** zboot customers do not have this property available in the SLA Engine Properties page.

</td></tr><tr><td>

**com.snc.sla.calculation.use\_time\_left**

</td><td>

Use field business\_time\_left to calculate breach time instead of business\_percentage field. Using business\_time\_left is more accurate because the business\_percentage field is rounded to 2 decimal places. This means that once the business percentage reaches 99.995%, it is recorded as 100%, and the task SLA is marked as breached.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**glide.sla.calculate\_on\_display**

</td><td>

Recalculate Task SLA records when a Task form is displayed. This ensures that the task SLAs calculations are up to date but this may increase form load time.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

**com.snc.sla.always\_populate\_business\_fields**

</td><td>

When this property is set to true, the business fields such as Business elapsed time will be populated with the same values as those in the actual fields when there is no schedule specified on the Task SLA.

 If the property is false, the business fields will be empty when a Task SLA has no schedule.

 -   Type: true \| false
-   Default value: true for new instances, false for upgraded instances

</td></tr></tbody>
</table>## SLA logging properties

Administrators can configure SLA logging using SLA properties.

Navigate to **Service Level Management** &gt; **Properties** &gt; **SLA Logging** to view SLA logging properties.

The **Logging level for...** properties set logging levels for relevant script includes. This allows you to activate extra logging targeted at whenever that script include is invoked via a task SLA. For example, if you know of an issue with the **TaskSLAworkflow** script include, you can use **the com.snc.sla.workflow.log** property to enable logging on that script include. These properties are all set to **Notice** level by default.

<table id="table_z2v_q3y_2r"><thead><tr><th>

SLA Logging Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.sla.task\_sla\_controller.log

</td><td>

Logging level for TaskSLAController

</td></tr><tr><td>

com.snc.sla.task\_sla.log

</td><td>

Logging level for TaskSLA

</td></tr><tr><td>

com.snc.sla.condition.log

</td><td>

Logging level for SLAConditionBase

</td></tr><tr><td>

com.snc.sla.workflow.log

</td><td>

Logging level for TaskSLAworkflow

</td></tr><tr><td>

com.snc.sla.calculatorng.log

</td><td>

Logging level for SLACalculatorNG

</td></tr><tr><td>

com.snc.sla.repair.log

</td><td>

Logging level for SLARepair \([SLA repair](../concept/c_RepairSLAs.md) must be enabled to use this\)

</td></tr><tr><td>

com.snc.sla.log.destination

</td><td>

Logging output destination.Select the log destination: either output to both the Database and node logs \(the default\), or output to node logs only.

 Database and node logs \(**gs.log**\) are visible as system logs from ServiceNow, node logs \(**gs.print**\) only appear in log files.

</td></tr></tbody>
</table>### Logging levels

The following logging levels are available for the **Logging level for...** properties:

|Level|Name|Description|
|-----|----|-----------|
|Emerg|Emergency|Total failure.|
|Alert|Alert|System corruption of a database, for example.|
|Crit|Critical|Typically used for hardware errors, for example.|
|Err|Errors|Errors|
|Warning|Warnings|Warnings|
|Notice|Notice|Possible action required but not essential.|
|Info|Informative|No action required.|
|Debug|Debugging|Generally not used except for capturing everything for fault-finding.|

**Note:** By default, logging levels are set to **Notice**

## SLA repair properties

Administrators can manage the SLA repair function using system properties.

Navigate to **Service Level Management** &gt; **Properties** &gt; **SLA Repair** to view [SLA repair](../concept/c_RepairSLAs.md) properties.

<table id="table_dfk_jkh_gr"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.sla.repair.enabled

</td><td>

Enable SLA repair. When enabled the Repair modules and UI Actions will be activated.-   Type: true / false
-   Default value: true for new instances and false for upgraded instances

</td></tr><tr><td>

com.snc.sla.repair.use\_repair\_workflow

</td><td>

When repairing SLAs, use the Repair workflow instead of the one configured on the SLA Definition.-   Type: true / false
-   Default value: false for new instances, true for upgraded instances
-   Learn more: [Configure SLA repair](../reference/r_ManageSLARepair.md)

</td></tr><tr><td>

com.snc.sla.repair.workflow

</td><td>

The name of the Repair workflow.-   Type: string
-   Default value: Default SLA Repair workflow

</td></tr></tbody>
</table>