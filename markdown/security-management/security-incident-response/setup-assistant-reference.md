---
title: Setup Assistant reference
description: The Setup Assistant walks you through the steps you need to perform to set up the Security Incident Response base system. This section provides additional information on the complicated steps for which you may require more explanation.You can create a process definition to define the way security incidents transition from one state to the next. Process definitions give service desks and end users help tracking the problem throughout its life cycle.Security Incident Response Process Definition replaces state flows and provides end users and service desks with the status of a problem. A process definition helps track the problem through its life cycle. Security Incident Response is a Service Management \(SM\) application, which has its own set of states. Invalid states are reported as part of Process Selection.Security Incident Response Process Selection lists processes with invalid states for security incidents and response tasks.You can select the process definition to use for the appropriate states for your company security incidents and response tasks.Create a custom Process Definition script for the appropriate states for your company security incidents and response tasks.The Process Definition script include provides methods for defining a process definition.An administrator can correct the security incident or task to valid states, either manually or using a script. Available states vary based on the current state of the incident.Set up a security incident group and assign the appropriate roles and users to the group.Security incident calculator groups are used to group calculators.Security incident calculators allow you to calculate the severity of a security incident based on pre-defined formulas. You can define your own security incident calculators, as needed.Security incident calculators are used to update record values when pre-defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.The risk score is calculated as an arithmetic mean that represents the risk based on the priority of a security incident, the type of security incident \(Denial of Service, Spear Phishing, or Malicious code activity\), and the number of sources that triggered a failed reputation score on an indicator.The risk score weights used to calculate risk scores in security incidents can be removed or updated on an individual basis. They can also be removed or updated for all security incidents. The ability to remove them from security incidents is useful when changing weight values.You can define a Service Level Agreement \(SLA\) for Security Incident Response.You can repair SLA records to ensure that SLA timing and duration information is accurate.A runbook is an association between a published knowledge article and a specific task. While you are performing the task, a knowledge article in the runbook automatically opens, providing information pertinent to the task.When your employees receive emails that appear to be phishing attacks, they can report them to you using a phishing email address. The suspicious email is validated using rules defined by your organization.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 30
breadcrumb: [Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Setup Assistant reference

The Setup Assistant walks you through the steps you need to perform to set up the Security Incident Response base system. This section provides additional information on the complicated steps for which you may require more explanation.

## Create a Security Incident Response process definition

You can create a process definition to define the way security incidents transition from one state to the next. Process definitions give service desks and end users help tracking the problem throughout its life cycle.

### Before you begin

Role required: sn\_si.admin

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Administration** &gt; **Process Definition**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the record which describes the process encoded in the script include file. The name is displayed as a choice in the **Process Definition Selector** list.|
    |Script include|The name \(including the `sn_si`. prefix\) of the script include containing the definition of the process. The script must be in the Security Incident \(`sn_si`\) application scope. See [Create a custom Security Incident Response process definition script include](setup-assistant-reference.md#) for more information. If this field does not contain a valid script include name, the default ProcessDefinition\_NIST\_Stateful definition is used.|
    |Description|Helpful information about the script include.|
    |Order|Determines the position in the process definition list.|
    |Active|When checked, it makes this process definition selectable from the **Process Definition Selector** page.|

4.  Click **Submit.**


**Related topics**  


[Security Incident Response Process Selection](setup-assistant-reference.md#)

[Understanding Security Incident Response process definition](setup-assistant-reference.md#)

### Understanding Security Incident Response process definition

Security Incident Response Process Definition replaces state flows and provides end users and service desks with the status of a problem. A process definition helps track the problem through its life cycle. Security Incident Response is a Service Management \(SM\) application, which has its own set of states. Invalid states are reported as part of Process Selection.

#### Security Incident Response Process Definition

The default process definition \(NIST Stateful\) defines the following incident states:

**Note:** Available states vary based on the current state of the incident.

|State|Description|
|-----|-----------|
|Draft|The request initiator adds information about the security incident, but it isn’t yet ready to be worked on.|
|Analysis|The incident has been assigned and the issue is being analyzed.|
|Contain|The issue has been identified and the security staff is working to contain it and perform damage control. These actions can include taking servers offline, disconnecting equipment from the internet, and verifying that backups exist.|
|Eradicate|The issue has been contained and the security staff is taking steps to fix the issue.|
|Recover|The issue is resolved and the operational readiness of the affected systems is being verified.|
|Review|The security incident is complete and all systems are back to normal function, however, a post incident review is still needed.|
|Closed|The incident is complete but before a security incident can be closed, you must fill out the information on the **Closure Information** tab.|

#### Security Incident task process definitions

The following process definitions are used for security incident tasks.

|State|Description|
|-----|-----------|
|Ready|The task is ready to be worked on after it’s assigned to an agent.|
|Assigned|The task is assigned to an agent.|
|Work In Progress|The assigned agent is working on the task.|
|Complete|The task is complete.|
|Canceled|The task was canceled.|

NIST supports the following two models:

-   **NIST Stateful**

    This process definition enables analysts to move from one state to another in a sequential order without skipping any step. For example, if the Analyst starts with the **Draft** state, then the sequential order of this process definition is **Draft**&gt;**Analysis**&gt;**Contain**&gt;**Eradicate**&gt;**Recover**. So, the NIST Stateful process definition is unidirectional and enables analysts only to progress only to the forward states.

    Here’s another example, if the Analyst starts with the Analysis state, then the sequential order of this process definition is **Analysis**&gt;**Contain**&gt;**Eradicate**&gt;**Recover**.

-   **NIST Open**

    This process definition enables analysts to move from one state to another, either forward or backward. For example, if the Analyst starts with the **Analysis** state, then the order of the process definition can either be **Analysis**&gt;**Contain**&gt;**Eradicate**&gt;**Recover** or **Analysis**&gt;**Draft**. So, the NIST Open process definition is bidirectional and enables analysts to move to the forward or backward states depending on their requirements.


#### Security Incident Response Process Selection

Security Incident Response Process Selection lists processes with invalid states for security incidents and response tasks.

An administrator can correct the incident or task to valid states either manually or by using a script. An empty related list \(no incidents; no tasks\) indicates that every active task is in a valid state. Available states vary based on the current state of the incident. For more information, see [Correct an invalid security incident or task state with process definition](setup-assistant-reference.md#).

##### Select a Security Incident Response process definition

You can select the process definition to use for the appropriate states for your company security incidents and response tasks.

###### Before you begin

Role required: admin and sn\_si.admin

###### About this task

###### Procedure

1.  Navigate to **All** &gt; **Security Incident Response** &gt; **Administration** &gt; **Process Selection**.

2.  Click the search icon to list the available process definitions.

    ![Process definition selector](../image/ProcessorSelector.png)

3.  Select a process definition.

4.  Click **Update**.


#### Create a custom Security Incident Response process definition script include

Create a custom Process Definition script for the appropriate states for your company security incidents and response tasks.

##### Before you begin

Role required: sn\_si.admin

##### About this task

The sn\_si.ProcessDefinition main script include controls process definitions. **Process Definition** determines which definition is in use \(using **Process Selection**\). It calls the appropriate script include file to determine the initial states and transitions for both security incidents and response tasks.

##### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Click **New.**

3.  Fill in the fields, as appropriate.

<table id="table_qfl_nwk_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this script include.

</td></tr><tr><td>

API Name

</td><td>

Created based on the name of the script include.

</td></tr><tr><td>

Client callable

</td><td>

Makes the script include available to client scripts, list and report filters, reference qualifiers, or, if specified, as part of the URL.

</td></tr><tr><td>

Application

</td><td>

Security Incident

</td></tr><tr><td>

Accessible from

</td><td>

Choose **This application scope only** .

</td></tr><tr><td>

Active

</td><td>

When checked, it makes this script include selectable from the **Process Definition** page.

</td></tr><tr><td>

Description

</td><td>

Helpful information about the script include.

</td></tr><tr><td>

Script

</td><td>

Defines the server-side script to run when called from other scripts.The script must define a single JavaScript class or a global function. The class or function name must match the Name field.

For information on script contents, see [Process Definition script include](setup-assistant-reference.md#).

</td></tr></tbody>
</table>    ![Process Definition script include form](../image/ProcessDefinition-ScriptInclude.png)

4.  Click **Submit.**


**Related topics**  


[Process Definition script include](setup-assistant-reference.md#)

##### Process Definition script include

The Process Definition script include provides methods for defining a process definition.

Implement the constants, attributes, arrays, and method calls described here to customize a process definition script include.

###### Where to use

Use this script include to create a process definition.

###### Script include body

The script include body is composed of three sections:

-   Constants: Initial state definitions
-   Security Incident and Response Task: Process definition arrays
-   Method calls: Retrieving information

###### Constants

Constants are used to define the initial states of security incidents and response tasks.

The use of constants is optional but encouraged for readability. For example:

```
INITIAL_INCIDENT_STATE: 10,
INITIAL_TASK_STATE: 1,

```

Which are later used by the following methods:

```

getInitialIncidentState: function() {
return this.INITIAL_INCIDENT_STATE;
},
getInitialTaskState: function() {
return this.INITIAL_TASK_STATE;
},
```

The next set of constants defines the states for both security incidents and response tasks.

Each array also contains the definition of which states are available when the incident or task is in a specific state.

For example:

```
TASK_STATES: [{state:1, label:"Draft", choice:[1, 10]},
 {state:10, label:"Ready", choice:[10, 16]},
 {state:16, label:"Assigned", choice:[16, 18]},
 {state:18, label:"Work in Progress", choice:[18, 3]},
 {state:3, label:"Close Complete", choice:[]},
 {state:7, label:"Cancelled", choice:[]},
 ],
```

The example is an array of objects. Each object defines a state and possible transition states.

The order of the state's object determines the desired order for the flow.

When the task is in the 'Draft' state \(value 1\), possible states are: 1 \(Draft, which is no change\) and 10 \(Ready, the next step in the process\).

There is no limit on the number of transitions out of a state. The 'Close Complete' and 'Canceled' state are final states and therefore have no possible state transitions.

The order of the attributes in the object is not important. If it makes the definition clearer, put the label first.

###### Attributes

Required attributes in a state definition object are:

-   state: numerical value of the state
-   label: human readable text associated with the state
-   choice: an array of state values the state can transition to \(determines the content of the state dropdown\)

Optional attributes are:

-   mandatory: list of field IDs that become mandatory in this state
-   readonly: list of field IDs that become read-only in this state
-   visible: list of field IDs that become visible in this state
-   notmandatory: list of field IDs that become non-mandatory in this state
-   notvisible: list of field IDs that would no longer be visible in this state

**Note:**

If optional attributes are used, it is the author's responsibility to ensure that fields are made visible/invisible, mandatory/non-mandatory, visible/hidden, or readonly appropriately between states.

For example, hiding a field in one state does not make it visible in another state later unless the 'visible' attribute is used.

###### Process flow definition arrays

To define the information displayed in the process flow formatter \(the bar at the top of the Security Incident and Response task forms\), the system requires information on what to display for each state.

For example:

```
TASK_PF: [{label:"Draft", condition:"state=1^EQ", description:"<p>Security Incident Response Task is in draft</p>"},
 {label:"Ready", condition:"state=10^EQ", description:"<p>Security Incident Response Task is ready to be assigned</p>"},
 {label:"Assigned", condition:"state=16^EQ", description:"<p>Security Incident Response Task is assigned</p>"},
 {label:"Work in Progress", condition:"state=18^EQ", description:"<p>Work has started on this Security Incident Response Task</p>"},
 {label:"Closed", condition:"state=3^ORstate=4^ORstate=7^EQ", description:"<p>Security Incident Response Task is complete</p>"},
],
```

The TASK\_PF array is a collection of labels, conditions, and descriptions used to determine the text displayed in the process formatter bar \(including order and activity\).

In the example, the text 'Ready' is the second item displayed. It is highlighted when the task satisfied the condition 'state=10^EQ'.

When the pointer hovers over the text, the description 'Security Incident Response Task is ready to be assigned' is displayed.

**Note:**

States can be combined to a single formatter state.

In the example, both the 'Close Complete' and the 'Canceled' states show up as 'Closed' in the top bar.

###### Method calls

The following methods must be present in the script include as they are used by sn\_si.ProcessDefinition:

|Return type|Method summary|Description|
|-----------|--------------|-----------|
|String|getInitialIncidentState: function\(\)|return the initial incident state numerical value|
|String|getInitialTaskState: function\(\):|return the initial task state numerical value|
|Array of string|getIncidentStates: function\(\):|return the incident state's array|
|Array of string|getTaskStates: function\(\):|return the task state's array|
|Array of objects|getIncidentProcessFlows: function\(\):|return the incident process flow definition array|
|Array of objects|getTaskProcessFlows: function\(\):|return the task process flow definition array|

The next set of methods are called whenever an incident or a task is updated and allows actions to be taken on specific change transitions.

|Return type|Method summary|Description|
|-----------|--------------|-----------|
|void|performIncidentStateChange: function\(current, previous\)|In the examples, this method is used to set SM-related values and ensure that an incident advances out of 'Draft' once someone is assigned to it.|
|void|performTaskStateChange: function\(current, previous\)|In the example, this method is used to update timestamps \(on assignment and closing\) and advance the task from 'Ready' to 'Assigned' once the assigned\_to field is filled.|

The same actions performed by these two methods can be accomplished using a business rule. By defining them in the script include, switching process definitions is made easier.

#### Correct an invalid security incident or task state with process definition

An administrator can correct the security incident or task to valid states, either manually or using a script. Available states vary based on the current state of the incident.

##### Before you begin

Role required: admin

##### About this task

After you have switched process definitions, the new definition may not support some of the old states. To correct the orphan incident or task states, you can [change your process definition](setup-assistant-reference.md#), [edit your script include](setup-assistant-reference.md#), or manually open each incident or task to update the state. Generally, updating the state \(which can be done in bulk\) is the easiest solution.

To change states in bulk, do the following:

##### Procedure

1.  Navigate to **All** &gt; **Process Selection**.

2.  Highlight the **State** field for the incidents or tasks you want to change.

3.  Double-click the **State** field in the first record, select the new **State,** and click the green check mark \(![Green check mark](../../vulnerability-response/image/GreenCheckMarkIcon.png)\) to complete the change.

    ![Corrected definition example](../image/CorrectedDefinition.png)

4.  Click **Update**.


## Create a security incident group

Set up a security incident group and assign the appropriate roles and users to the group.

### Before you begin

Roles required:

-   If you have the user\_admin role, you can create security incident assignment groups.
-   If you have the sn\_si.admin role, you can create and edit security incident assignment groups.

### About this task

Users in a group inherit the roles of the group, so you do not have to assign roles to each user separately.

It is a good practice to create as many groups as needed in your organization. It is also a good practice to create one group for administrators and assign the admin role to this group only.

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups** or **Security Incident** &gt; **Setup** &gt; **Groups**.

2.  Click **New**.

3.  On the form, fill in the fields.

    **Note:**

    For more information, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

4.  Make sure that you select the **security incident** type for this group.

    1.  If the **Type** field is not visible, configure the form to add it.

    2.  Click the lock icon beside the **Type** field.

    3.  Click the reference lookup icon \(![lookup icon](../image/SearchIcon.png)\)

    4.  Search for and select the **security incident** type.

5.  Right-click the form header and select **Save**.

6.  In the **Roles** related list, add the roles that each member of this group receives.

    For example, if you are making a group for Security Incident Response team members, add sn\_si.analyst. If you are making a group for Security Incident Response administrators, add sn\_si.admin.

7.  In the **Group Members** related list, add users to this group.

8.  Click **Update**.


## Create a security incident calculator group

Security incident calculator groups are used to group calculators.

### Before you begin

Role required: sn\_si.admin

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Setup** &gt; **Security Incident Calculator Groups**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the security incident calculator.|
    |Application|The application that contains this record.|
    |Order|The order in which the security incident calculator is run. A calculator with an order entry of 100 runs before a calculator with an order entry of 200.|
    |Description|A description of this calculator group.|
    |Created by|Enter the name of the user who created|

4.  Click **Submit**.


### Create a security incident calculator

Security incident calculators allow you to calculate the severity of a security incident based on pre-defined formulas. You can define your own security incident calculators, as needed.

#### Before you begin

Role required: sn\_si.admin

#### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Setup** &gt; **Security Incident Calculator Groups**.

2.  Click the name of the group for which you want to create a calculator, or you can [create a calculator group](setup-assistant-reference.md#).

3.  Click **New**.

4.  Fill in the fields on the form, as appropriate.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the security incident calculator.

</td></tr><tr><td>

Calculator Group

</td><td>

Name of the group to which this calculator belongs. **Note:** Creating or changing the calculator group becomes available after you have entered a **Name** and **Table**.

</td></tr><tr><td>

Table

</td><td>

Select the table to be used for this calculator.

 When you add calculators to tables other than Vulnerability \[sn\_vul\_vulnerability\] and Vulnerable Item \[sn\_vul\_vulnerable\_item\], you must add business rules and UI Actions to those tables. To see examples:

-   Navigate to **System Definition** &gt; **Business Rules**, and locate the **Calculate Severity** business rule on the Vulnerable Item \[sn\_vul\_vulnerable\_item\] table.
-   Navigate to **System UI** &gt; **UI Actions**, and locate the **Calculate Severity** UI action on the Vulnerable Item \[sn\_vul\_vulnerable\_item\] table.
 Also, the vulnerability admin role must be granted full read, write \(or save\_as\_template\) capabilities on any table used by a calculator to properly see the values to apply to the template.

</td></tr><tr><td>

Application

</td><td>

The scoped application to which the calculator belongs.

</td></tr><tr><td>

Order

</td><td>

The order in which the security incident calculator runs. A calculator with an order entry of 100 runs before a calculator with an order entry of 200.

</td></tr><tr><td>

Active

</td><td>

Turn the calculator on or off.

</td></tr><tr><td>

Description

</td><td>

A description of this calculator.

</td></tr></tbody>
</table>5.  Right-click the form header and select **Save**.

    The **Conditions** and **Values to Apply** tabs appear.

6.  Fill in the fields in the **Conditions** tab, as appropriate.

<table id="table_xl5_43j_tw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use filter group

</td><td>

Select this check box to use a predefined filter group or [create a new filter group](../../security-operations-common/task/create-filter-group.md) to define the calculator criteria.

</td></tr><tr><td>

Filter group

</td><td>

Select the filter group to use for defining a calculator. This field appears only if you selected the **Use filter groups** check box.

</td></tr><tr><td>

Use advanced condition

</td><td>

Select this check box to indicate that a script condition is used to determine when this calculator is applied. When you select the check box, an **Advanced condition** scripting field appears.If you selected the **Use filter group** check box, this field is hidden.

 **Note:** Before you define advanced conditions and write scripts for determining when the security incident calculators are applied, return to the Security Incident Calculators list. Explore the calculator records shipped with the base system.

</td></tr><tr><td>

Condition

</td><td>

Defines basic filter conditions for determining whether the calculator is used. If you selected either of the **Use filter group** or **Use advanced conditions** check boxes, this field is hidden.

</td></tr></tbody>
</table>7.  Click the **Values to Apply** tab and fill in the fields on the form, as appropriate.

    You have the choice of creating a script for defining the values to apply to the calculation or defining a template based on fields in the selected table.

<table id="table_p2z_4jj_tw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use script values

</td><td>

Select this check box to define field values with a script.

</td></tr><tr><td>

Script values

</td><td>

Defines what values to apply the calculations to.This field appears only if you selected the **Use script values** check box.

</td></tr><tr><td>

Template

</td><td>

Right-click the form header and select **Save**. Select the fields and values you want to use for the calculator.

</td></tr></tbody>
</table>8.  When you have completed all entries, click **Submit**.


### Understanding security incident calculators

Security incident calculators are used to update record values when pre-defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.

The Security Incident Response base system includes the following security incident calculator groups and calculators. Within each group, the first calculator that matches the conditions is run.

<table id="table_wmy_bbn_2s"><thead><tr><th>

Security Incident Calculator Group Name

</th><th>

Calculators included in group

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Impact

</td><td>

Aggregate from Severity Calculators

</td><td>

This calculator delegates to the Security Criticality Calculator that determines criticality by weighing the values of other fields.

</td></tr><tr><td rowspan="6">

Severity

</td><td>

Business Impacted

</td><td>

This severity calculator defines its selection criteria using a simple condition builder.

</td></tr><tr><td>

Critical service affected

</td><td>

This severity calculator defines its selection criteria using an advanced condition. If the configuration item in the security incident is associated with a highly critical business service, the **Risk score**, **Business Impact**, and **Priority** fields are elevated as defined by the calculator.

</td></tr><tr><td>

Critical service changes

</td><td>

This severity calculator defines its selection criteria using an advanced condition. If the security incident meets the conditions, a script runs to define what levels the fields are elevated to. If the configuration item in the security incident is associated with a most critical or somewhat critical business service, the **Risk score**, **Business Impact**, and **Priority** fields are elevated as defined by the calculator.

</td></tr><tr><td>

Multi-Attack Vectors

</td><td>

This severity calculator defines its selection criteria using a simple condition builder. If the configuration item in the security incident is associated with web, email, and impersonation attack vectors, the **Risk score**, **Business Impact**, and **Priority** fields are elevated as defined by the calculator.

</td></tr><tr><td>

Set priority with category and services

</td><td>

This severity calculator defines its selection criteria using an advanced condition builder.The security incident priority is set to **1 - Critical** when the following conditions are met:

-   The security incident has associated affected services and one of them is critical.
-   The security incident category is one of the following:
    -   Denial of Service
    -   Spear Phishing
    -   Malicious code activity

**Note:** This calculator is available in the base system when you have the Starter Security Operation pricing tier.

</td></tr><tr><td>

Set priority with observables

</td><td>

This severity calculator defines its selection criteria using an advanced condition builder.The security incident priority is set to**1 - Critical** when the following conditions are met:

-   The security incident has associated affected services and one of them is critical.
-   The security incident category is one of the following:
    -   Denial of Service
    -   Spear Phishing
    -   Malicious code activity
-   One of the associated observables or indicators has a sighting count that exceeds two sightings with active indicators \(that is, the observables or indicators are confirmed as being bad from multiple sources\).

**Note:** This calculator is available in the base system when you have the Advanced Security Operation pricing tier and you activate the Threat Feeds plugin.

</td></tr><tr><td rowspan="2">

User criticality

</td><td>

Get user criticality

</td><td>

This severity calculator defines its selection criteria using a simple condition builder. This severity calculator causes user business criticality to change to **1 - Critical** when the **Department** field is changed to **Finance**.

</td></tr><tr><td>

Get user group criticality

</td><td>

This severity calculator defines its selection criteria using an advanced condition builder. This severity calculator provides example of a calculator that runs on data in a related list.

</td></tr></tbody>
</table>#### Severity calculators

When you create a security incident, the **Risk score**, **Business Impact**, and **Priority** fields contain default values. When you save the incident, a business rule automatically validates the information in the security incident against conditions defined in each of your active severity calculators. They are validated one security calculator at a time, in the order defined by the **Order** field in each calculator. If information in the security incident matches the conditions defined in one of the calculators, the severity field values are updated accordingly to the rules set up in the calculator.

For example, assume that you create a security incident for an affected CI, and the CI is highly critical. When the security incident is saved, the CI information is compared to the conditions defined in the severity calculators. When the security incident is validated against the **Critical service affected** severity calculator, the severity fields are automatically updated, and a message appears at the top of the security incident.

You can use these severity calculators as is or you can edit them to more closely meet the needs of your business. For example, if you want to identify web and email threats that are specific to the Finance business unit, you can change the conditions of the **Multi Attack Vectors** calculator:

-   \[Attack Vector\] \[contains\] \[Web\]
-   \[Attack Vector\] \[contains\] \[Email\]
-   \[Business Unit\] \[contains\] \[Finance\]

You can also update the severity values in an existing security incident at any time by opening the record and clicking the **Calculate Severity** related link.

#### Security incident risk score calculators

The **Set priority with category and services** and **Set priority with observables** calculators are used to calculate a risk score for a security incident.

#### User criticality calculators

The two calculators in the **User criticality** group \(**Get user criticality** and **Get user group criticality**\) provide examples of how you can drive criticality based on criteria defined in a user record or based on the group to which a user belongs.

They can be edited as needed, or new user criticality calculators can be created.

The **Get user criticality** calculator causes user business criticality to change to **1 - Critical** when the **Department** field is changed to **Finance**.

The **Get user group criticality** calculator causes user business criticality to change to **1 - Critical** when the user is added to the **Database** group.

**Note:** **Get user group criticality** is an example of a calculator that runs on data in a related list. If you want to add more groups to initiate a criticality change, add a comma-separated list of group sys\_ids in the first line of the script. Example: `var CRITICAL_GROUPS = [group1_sys_id, group2_sys_id, group3_sys_id]`.

#### Security incident risk score calculations

The risk score is calculated as an arithmetic mean that represents the risk based on the priority of a security incident, the type of security incident \(Denial of Service, Spear Phishing, or Malicious code activity\), and the number of sources that triggered a failed reputation score on an indicator.

The risk score aids in prioritizing security incident work for the analysts.

**Important:** If you want to use the new Risk Score Calculator, refer to [Define the new Risk Score Calculator Rules](../../secops-analyst-workspace/task/define-risk-score-calculator-rules-sir.md).

The **Set priority with category and services** and **Set priority with observables** [security incident calculators](setup-assistant-reference.md#) are used to calculate a risk score for a security incident. Additionally, the following business rules trigger automatic calculation of risk scores:

-   Calculate Severity
-   Update risk score
-   Update SI risk score

**Note:** The risk calculator available in the base system depends on your Security Operations pricing tier.

When you look at a list of security incidents in the base system, notice the **Risk score** column.

![Security Incidents and risk scores](../image/si-risk-score.png "Security Incidents")

The risk score is calculated using weights defined in **Risk score configuration**.

![Risk score weights](../image/risk-score-weights.png "Risk score configuration")

For example, if a security incident has a **Business impact** set to **2-High** and a **Priority** set to **3-Moderate**, the respective weights in the Risk Score Weights table are looked up and calculated thus:

**Security Incident Business Impact** with a value of 2 = a weight of 60.

**Security Incident Priority** with a value of 3 = a weight of 40.

\(60 + 40\)/2 = a risk score of 50.

The position of the security incident in the security incident list is then re-ordered based on its updated risk score.

If, in the example above, the **Business impact** or **Priority** of the security incident are changed, the risk score is recalculated, and the changes are reflected in the work notes.

![Work notes after risk score calculation](../image/work-notes.png "Work notes")

The work notes are updated when the following fields are changed \(causing the risk score to be updated\):

-   **Business impact** on the Security Incident form
-   **Priority** on the Security Incident form
-   **Severity** on the Security Incident form \(hidden by default\)
-   **Business impact** on the **Affected Users** related list
-   **Business impact** on the **Affected Services** related list
-   **Business impact** on vulnerabilities on the **Vulnerable items** related list

Additionally, the work notes are updated in the following situations:

-   When an association between affected users and a security incident is created or modified
-   When an association between affected services and a security incident is created or modified
-   When an association between vulnerable items and a security incident is created or modified

Work notes are also updated whenever **Update All Risk Scores** and **Clear All Risk Scores** on the [Risk Score Weights](setup-assistant-reference.md#) form are clicked.

##### Maintain risk score weights

The risk score weights used to calculate risk scores in security incidents can be removed or updated on an individual basis. They can also be removed or updated for all security incidents. The ability to remove them from security incidents is useful when changing weight values.

###### Before you begin

Role required: sn\_sec\_cmn.admin

**Note:** Users with the sn\_si.read role can view the risk score configuration in Security Incident Response.

###### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Setup** &gt; **Risk Score configuration**.

    **Note:** Users with the sn\_si.read role can view the risk score configuration by navigating to **Security Incident** &gt; **Alerts &amp; Events** &gt; **Risk Score Configuration**.

2.  To add a new risk score weight, click **New** and enter information in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|Select the type of risk score you are defining.|
    |Value|Specify the value associated with the selected type. If multiple values are available for the type, you may want to define multiple risk score weight records. Example: Security Incident Priority with a value of 1, Security Incident Priority with a value of 2, and so forth.|
    |Weight|The weight associated with the selected type/value pair. Valid entries are between 0 through 100, with 0 being the lowest weight and 100 the highest.|

3.  Click **Submit**.

4.  Perform any of these steps, as needed.

    -   To clear a risk score weight record, open it from the list and click **Delete**.
    -   To clear all risk score weight records, click **Clear All Risk Scores**.
    -   To update all risk score weight records, click **Update All Risk Scores**.

## Create a Security Incident Response SLA

You can define a Service Level Agreement \(SLA\) for Security Incident Response.

### Before you begin

Role required: sn\_si.admin

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Setup** &gt; **SLAs**.

2.  Click **New**.

    For field descriptions and detailed instructions, see [Create an SLA definition](https://www.servicenow.com/docs/access?context=t_CreateAnSLADefinition&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).


### Repair security incident SLAs

You can repair SLA records to ensure that SLA timing and duration information is accurate.

#### Before you begin

Role required: sn\_si.basic

#### Procedure

1.  If it is not already open, open the security incident you want to repair SLAs for.

2.  Click the form header context menu and select **Repair SLAs**:

    ![Repair SLAs from the form header menu](../image/HamburgerRepainSLAs.png)

3.  Click **OK** in the Warning confirmation box.

    For more information, see [Repair SLAs](https://www.servicenow.com/docs/access?context=c_RepairSLAs&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).


## Create a Security Incident Response runbook

A runbook is an association between a published knowledge article and a specific task. While you are performing the task, a knowledge article in the runbook automatically opens, providing information pertinent to the task.

### Before you begin

There must be existing knowledge articles in the Security Incident Response Runbook knowledge base. When you [create a security incident knowledge article](../task/t_CrtScrIncdtKnwArt.md), be sure to select **Security Incident Response Runbook** in the **Knowledge base** field. After you publish the article, you can select the **Create Runbook** button.

Role required: sn\_si.knowledge\_admin

### About this task

You can use runbooks during the security incident or response task creation processes, or you can associate the knowledge base articles in a runbook with tasks in the playbook.

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Manual Runbook** &gt; **Create New Runbook**.

2.  Fill in the fields, as appropriate.

<table id="table_qfl_nwk_cp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge article

</td><td>

Select a knowledge article to include in the runbook.

</td></tr><tr><td>

Active

</td><td>

Check the box to make the runbook available from the **Filter Navigator**.

</td></tr><tr><td>

Use filter group

</td><td>

Select this check box to use a predefined filter group or [create a new filter group](../../security-operations-common/task/create-filter-group.md) to define the runbook criteria.

</td></tr><tr><td>

Filter group

</td><td>

Select the filter group to use for defining a runbook. This field appears only if the **Use filter groups** check box is selected.

</td></tr><tr><td>

Table

</td><td>

Select either Security Incident \[sn\_si\_incident\] or Security Incident Response Task \[sn\_si\_task\].If you selected the **Use filter group** check box and selected a filter group, this field defaults to the table associated with the selected filter group.

</td></tr><tr><td>

Condition

</td><td>

Set the conditions that connect this runbook to the incident or task.If you selected the **Use filter group** check box and selected a filter group, the **Condition** fields are not displayed.

</td></tr></tbody>
</table>3.  Right-click the form header and select **Save**.

    The Knowledge Article Details tab and a series of buttons appear.

4.  To view the details of the runbook, click the **Knowledge Base Details** tab.

5.  To see the knowledge article as it would appear to the user, click **View Article**.

6.  To [edit the details of the knowledge article](https://www.servicenow.com/docs/access?context=create-knowledge-article&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US), click **Edit Article**.


## Create rules to validate user-reported phishing attacks

When your employees receive emails that appear to be phishing attacks, they can report them to you using a phishing email address. The suspicious email is validated using rules defined by your organization.

### Before you begin

Before email matching rules can be used to identify potential phishing attacks, define an email address to which emails forwarded from your employees would be sent for processing. You have the following options for defining this email address \(assuming your company email domain is acme.com\):

-   Define an email address such as **acme+phishing@service-now.com**. The **+phishing** tag is supported by SMTP to enable filtering and your instance can receive emails sent to it.
-   Define an email address, such as **phishing@acme.com** \(your Exchange mailbox\), which in turn forwards it to **acme+phishing@service-now.com** \(your instance mailbox defined through a mail forwarding rule\).

Role required: sn\_sec\_cmn.write

### About this task

When an employee encounters a suspicious email, they should forward it as an attachment to your phishing email address. If the attached email matches a rule defining a threat, a security incident is created.

### Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Email Processing** &gt; **User Reported Phishing**.

2.  Click **New**.

3.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name for this email matching rule. For example, User Reported Phishing.|
    |Conditions|Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) to validate whether an email sent to your company phishing email address is a phishing attack. See the following example.|

4.  Click **Submit**.


### Example

This example shows a matching rule for handling user-reported phishing.

![Email matching rule](../image/cj-sir-email-match-example.png "Example of Email matching rule")

