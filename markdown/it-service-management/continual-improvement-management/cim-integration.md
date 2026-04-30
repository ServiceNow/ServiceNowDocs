---
title: Improvement integration with other applications
description: You can create an improvement request from within multiple integrated applications. You can also create many application tasks from within an improvement initiative. Set the Continual Improvement Management attributes property to determine which field values get copied to integrated application tasks.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Improvement integration with other applications

You can create an improvement request from within multiple integrated applications. You can also create many application tasks from within an improvement initiative. Set the Continual Improvement Management attributes property to determine which field values get copied to integrated application tasks.

Set Continual Improvement Management properties for integration with other applications.

As part of Continual Improvement Management integration with other applications, improvement requests can be created from within other applications and, conversely, records for other applications can be created from within an improvement initiative \(or CIM task\).

Multiple tasks from outside integrated applications can be linked to a single improvement initiative \(or CIM task\), and multiple CIM tasks can be linked to a single integrated application task for maximum flexibility when creating improvements.

An improvement initiative can be created from these applications.

-   [Benchmarks](../../benchmarks/reference/r_Benchmarks.md)
-   [Coaching](../../coaching/concept/coaching-landing.md)
-   Configuration Management Database \(CMDB\)
-   [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)
-   [Governance, Risk, and Compliance \(GRC\)](https://www.servicenow.com/docs/access?context=r_WhatIsGRC&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)
-   [Incident Management](../../incident-management/concept/c_IncidentManagement.md)
-   [Problem Management](../../problem-management/concept/c_ProblemManagement.md)
-   [Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

As part of an improvement initiative, these records can be created.

-   Demand record
-   [Project](https://www.servicenow.com/docs/access?context=c_ProjectApplicationOverview&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) \(optional\)

As part of a CIM task, these records can be created:

-   [change](../../change-management/concept/c_ITILChangeManagement.md) record
-   [Coaching opportunity](../../coaching/task/create-coaching-opportunity.md)
-   [Create a knowledge article](https://www.servicenow.com/docs/access?context=create-knowledge-article&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Create a story](https://www.servicenow.com/docs/access?context=create-a-story&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)

## Integration property

You can set field values that get copied to the improvement request when the improvement request is created from within another application.

To access Continual Improvement Management properties, navigate to **Continual Improvement** &gt; **Administration** &gt; **Properties**.

**Note:** System admin role is required to set Continual Improvement Management properties.

<table id="table_yhb_vc5_bdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List of attributes \(comma-separated\) that will be copied from the originating improvement initiative.

 sn\_cim.initiative\_copy\_attributes

</td><td>

Specifies the field values that are copied from the originating improvement initiative to the application task record \(for example, demand, project, change record\) created from the improvement initiative.

-   Short description \(short\_description\)
-   Description \(description\)
-   Priority \(priority\)
-   CIM estimate \(cim\_estimate\)
-   Benefit \(benefit\)
-   Assigned to \(assigned\_to\)
-   Strategic objective \(strategic\_objective\)
-   Business process \(business\_process\)
-   Business service \(business\_service\)
-   Approver group \(approver\_group\)
-   Type \(type\)

</td></tr></tbody>
</table>## Create Improvement Initiative related link

-   Benchmarks

    When you create an improvement initiative from Benchmarks, the improvement is associated with the Benchmarks recommendation candidate, and the Benchmarks KPI is added to the improvement initiative.

<table id="table_crz_4ft_pdb"><thead><tr><th>

Benchmarks recommendation candidate

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

-   **Create Improvement Initiative** related link is added.
-   **Create Improvement Initiative** related link is replaced by the **CIM number** related link once an improvement initiative is created.


</td><td>

Benchmarks recommendation KPI is added to the **Improvement KPI** field on the Goals tab.

</td></tr></tbody>
</table>-   Coaching

    When you create an improvement initiative from Coaching, the Improvement Initiatives related list is added to the coaching opportunity, and the coaching opportunity details are added to the improvement initiative.

<table id="table_btk_ncx_sfb"><thead><tr><th>

Coaching opportunity

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

-   **Create Improvement Initiative** related link is added.
-   Improvement Initiatives related list is added that contains the improvement initiative \(CIM\) record.


</td><td>

Coaching opportunity record to which the improvement initiative is linked is added to the **Source/Parent** field in the Details tab.

</td></tr></tbody>
</table>-   Configuration Management Database \(CMDB\)

    When you create an improvement initiative from CMDB, the Improvement Initiatives related list is added to the task, and the Remediate Duplicate Task details are added to the improvement initiative.

<table id="table_bmr_tcx_sfb"><thead><tr><th>

Remediate Duplicate Tasks record

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

-   **Create Improvement Initiative** related link is added.
-   Improvement Initiatives related list is added that contains the improvement initiative \(CIM\) record.


</td><td>

Remediate Duplicate Tasks record to which the improvement initiative is linked is added to the **Source/Parent** field in the Details tab.

</td></tr></tbody>
</table>-   Demand Management

    When you create an improvement initiative from Demand Management, the improvement initiative is associated with the demand record, and the demand details are added to the improvement initiative.

<table id="table_i1c_dgt_pdb"><thead><tr><th>

Demand record

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

-   **Create Improvement Initiative** related link is added.
-   Improvement initiative \(CIM\) record is set in the **Improvement** field.


</td><td>

Demand record to which the improvement initiative is linked is added to the **Source/Parent** field in the Details tab.**Note:** When the improvement is closed, the demand record is set to complete.

</td></tr></tbody>
</table>-   Governance, Risk, and Compliance \(GRC\)

    When you create an improvement initiative from GRC, the improvement initiatives related list is added to the issue, and the issue details are added to the improvement initiative.

<table id="table_oh2_g2x_sfb"><thead><tr><th>

Issue record

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

-   **Create Improvement Initiative** related link is added.
-   Improvement Initiatives related list is added that contains the improvement initiative \(CIM\) record.


</td><td>

Issue record to which the improvement initiative is linked is added to the **Source/Parent** field on the Details tab.

</td></tr></tbody>
</table>-   Incident Management

    When you create an improvement initiative from Incident Management, the improvement initiative is associated with the incident record, and the incident details are added to the improvement initiative.

<table id="table_jxq_ggt_pdb"><thead><tr><th>

Incident record

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

**Create Improvement Initiative** related link is added.**Note:** You must customize the Incident form to show the Improvement Initiatives related list that contains the improvement initiative \(CIM\) record.

</td><td>

Incident \(INC\) record is added to the **Source/Parent** field on the Details tab.

</td></tr></tbody>
</table>-   Problem Management

    When you create an improvement initiative from Problem Management, the improvement is associated with the problem record, and the problem details are added to the improvement initiative.

<table id="table_jsk_jgt_pdb"><thead><tr><th>

Problem record

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

**Create Improvement Initiative** related link is added. **Note:** You must customize the Problem form to show the Improvement Initiatives related list that contains the improvement initiative \(CIM\) record.

</td><td>

Problem \(PRB\) record is added to the **Source/Parent** field on the Details tab.

</td></tr></tbody>
</table>    |Problem record state|Improvement initiative state|
    |--------------------|----------------------------|
    |Open|New|
    |Pending change|In Progress|
    |Closed/Resolved|Closed|

-   Survey Management and Assessments

    When you create an improvement initiative from Survey Management, the improvement is associated with the Survey, and the survey details are added to the improvement initiative. \(Assessment Metric Type \[Survey view\] record\)

<table id="table_zx3_pgt_pdb"><thead><tr><th>

Survey definition record

</th><th>

Improvement initiative

</th></tr></thead><tbody><tr><td>

-   **Create Improvement Initiative** related link is added.
-   Improvement Initiatives related list is added that contains the improvement initiative \(CIM\) record.


</td><td>

Survey definition \(Assessment Metric Type \[Survey view\]\) record is added to the **Source/Parent** field on the Details tab.

</td></tr></tbody>
</table>
## Related links in improvement initiatives

-   **Create Demand**

    When you create a demand record from an improvement initiative, the demand record is associated with the improvement initiative, and the Demands related list is added to the improvement initiative.

<table id="table_dlm_1ht_pdb"><thead><tr><th>

Improvement initiative

</th><th>

Demand record

</th></tr></thead><tbody><tr><td>

-   **Create Demand** related link is added.
-   Demands related list is added that contains the demand \(DMND\) record.


</td><td>

-   **Continual Improvement Management** is set in the **Type** field.
-   Improvement initiative \(CIM\) record is set in the **Improvement** field.


</td></tr></tbody>
</table>-   **Create Project**

    When you create a project record from an improvement initiative, the Projects related list is added to the improvement initiative.

<table id="table_ryk_dht_pdb"><thead><tr><th>

Improvement initiative

</th><th>

Project record

</th></tr></thead><tbody><tr><td>

-   **Create Project** related link is added.
-   Projects related list is added that contains the project \(PRJ\) record.


</td><td>

No change.

</td></tr></tbody>
</table>-   **Create PA Indicator** related link

    [Create a Performance Analytics automated indicator](https://www.servicenow.com/docs/access?context=t_CrtIndctrIndctrWzrd&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

-   **Show Benchmarks** related link

    Shows the [benchmarks](../../benchmarks/concept/c_BenchDashboard.md) for the KPI specified in the Improvement Initiative form **Improvement KPI** field using the [Benchmarks](../../benchmarks/reference/r_Benchmarks.md) application.


## Related links in improvement initiative CIM tasks

**Note:** Related links in CIM tasks are shown only when a CIM task is in Open, Work in Progress, or On Hold state.

-   **Create Change**

    When you create a change \(CHG\) record from an improvement initiative CIM task, the change record is added to the Change Requests related list in the CIM task.

    |Improvement initiative CIM task|Change record|
    |-------------------------------|-------------|
    |Change \(CHG\) record is added to the Change Requests related list.|No change.|

    |Improvement initiative CIM task state|Change record state|
    |-------------------------------------|-------------------|
    |New|New|
    |In Progress|Implement|
    |Closed|Closed|

-   **Create Coaching Opportunity**

    When you create a coaching opportunity from an improvement initiative CIM task, the coaching opportunity record is added to the Coaching Opportunities related list in the CIM task.

    |Improvement initiative CIM task|Coaching opportunity record|
    |-------------------------------|---------------------------|
    |Coaching opportunity \(COP\) record is added to the Coaching Opportunities related list.|No change.|

-   **Create Knowledge**

    When you create a Knowledge Management knowledge base article \(KB\) record from an improvement initiative CIM task, the KB article record is added to the Knowledge Articles related list in the CIM task.

    |Improvement initiative CIM task|Knowledge base article record|
    |-------------------------------|-----------------------------|
    |Knowledge article record is added to the Knowledge Articles related list.|No change.|

-   **Create Story**

    When you create an Agile Management story record from an improvement initiative CIM task, the story record is added to the Stories related list in the CIM task.

    |Improvement initiative CIM task|Story record|
    |-------------------------------|------------|
    |The story \(STRY\) record is added to the Stories related list.|No change.|


## Integration with other applications

|Application|Application record|Create improvement initiative|Create application record from improvement initiative|
|-----------|------------------|-----------------------------|-----------------------------------------------------|
|GRC|
|Audit Management|Issue record|X|--|
|Strategic Portfolio Management|
|Agile Development|Story record|--|X|
|Demand Management|Demand record|X|X|
|Project Management|Project record|--|X|
|IT Operations Management|
|CMDB|Remediate Duplicate Task record|X|--|
|IT Service Management|
|Benchmarks|Benchmarks recommendation|X|--|
|Change Management|Change record|--|X|
|Major Incident Management|Post incident review workbench|X|--|
|Problem Management|Problem record|X|--|
|Platform Capabilities|
|Knowledge Management|Knowledge base article|--|X|
|Survey Management|Survey|X|--|
|Service Management|
|Coaching|Coaching opportunity|X|X|

## Extension point

You can use the Continual Improvement Management integration extension point to define an application to be integrated.

Extend `sn_cim.CIMIntegrationAPI` extension point to integrate Continual Improvement Management with other applications.

-   **[Create improvement initiatives from integrated applications](../task/create-improvmt-from-apps.md)**  
Create improvement initiatives from applications integrated with Continual Improvement Management to enable planning, implementation, monitoring, and impact assessment of improvements in a centralized framework.
-   **[Create application records from improvement initiatives](../task/create-app-records.md)**  
Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.
-   **[Configure CIM integration property](../task/configure-cim-int-property.md)**  
Configure the CIM sn\_cim.initiative\_copy\_attributes integration property to define field values to be copied from an improvement initiative to application records that you create from the initiative.

**Parent Topic:**[Continual Improvement Management overview](../concept/get-started-cim.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

