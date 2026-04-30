---
title: Prescriptive cost models for business services and business capabilities - Legacy
description: Use the preconfigured business services and business capabilities cost models with their prescribed metrics for weight allocation. Understand the system requirements that each model supports, the allocation methods, and the datasets required to use them effectively.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [The Cost Models tab - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Prescriptive cost models for business services and business capabilities - Legacy

Use the preconfigured business services and business capabilities cost models with their prescribed metrics for weight allocation. Understand the system requirements that each model supports, the allocation methods, and the datasets required to use them effectively.

**Important:**

This feature is available only when you own an ITBM Analyst license.

## Level 2 Costing — Business Services cost model

![Level 2 Costing — Business Services cost model](../image/L2-BusinessServices.png "Level 2 Costing — Business Services cost model")

The cost model provides:

-   Cost of Enabling the Business: The expenses of the IT to ensure that the business is aligned to transformational initiatives.
-   Cost to support each Business Service in business terms: The cost to provide business services.

The cost model is recommended:

-   At phase II or if you have previously invested in Financial Management.
-   For showback in terms of core business functions or alignment to business capabilities.
-   To provide insight into operational cost drivers.

Specifications of the Level 2 Costing — Business Services cost model:

![Model complexity of Level 2 — Service portfolio and IT shared services aligned.](../image/L2-BusinessServicesModelComplexity.png "Model complexity of Level 2 Costing — Business Services cost model")

-   The cost bucket layer ties to the ITFM Bucket table \[itfm\_bucket\]. Cost buckets are model specific.
-   IT Shared Service segment accounts \(the second layer in this model\) are sourced from the IT Shared Service table \[itfm\_shared\_service\].
-   Business Service segment accounts \(the third layer in this model\) are sourced from the Service table \[cmdb\_ci\_service\].
-   The Business Unit layer ties to the Platform Business Unit table \[business\_unit\].

## Level 3 Costing — Business Capabilities cost model

![Level 3 Costing — Business Capabilities cost model](../image/L3-BusinessCapabilities.png "Level 3 Costing — Business Capabilities cost model")

The cost model provides:

-   Cost of Enabling the Business: The expenses of the IT to ensure that the business is aligned to transformational initiatives.
-   Cost to support each Business Capability in business terms: The cost of innovation.

The cost model is recommended:

-   At phase II or if you have previously invested in Financial Management.
-   For showback in terms of core business functions or alignment to business capabilities.

Specifications of the Level 3 Costing — Business Capabilities cost model:

![Model complexity of Level 3 — business capability, application portfolio, and IT process services aligned](../image/L3-BusinessCapabilitiesComplexity.png "Model complexity of Level 3 Costing — Business Capabilities cost model")

-   The specifications are similar to that of the Level 2 Costing — Business Services cost model, aligned to business application. However, there is an extra layer for business capabilities. The accounts in this segment are sourced from the Business Capability \[cmdb\_ci\_business\_capability\] table, which is a flat list.
-   There is a prescribed scripted metric that aligns the actual capability associated with an application with the high-level business capability in the table.

## Rollup methods

Use the following allocation methods to move the cost from the cost buckets to the upper layers of the model \(IT Shared Services, Allocations, or Business Units\).

|Rollup methods|Description|
|--------------|-----------|
|None|Does not allocate out to the next layer.|
|Equal|Equally splits the cost to each item it is related to.|
|Manual|Allocated by estimated or pre-calculated fixed percentages.|
|Weighted|Allocated based on actual usage. For example, allocate to BU based on change request volume, incident volume, or CI count or by a property of the object being allocated to, which is headcount.|

The prescribed metrics support the **Weighted** rollup method, and source data directly from applications within the ServiceNow platform. For example:

-   IT organizational structure: Business unit or department level.
-   PPM or Time Card: Labor efforts charged to projects.
-   CMDB: CI inventory with relationships, usage, and owner alignment.
-   Asset Management: Asset inventory \(end user and infrastructure\) aligned to asset owners.
-   IT Service Management: Volume related to Incident, Problem, and Change.
-   IT Operations Management: Relationships and alignment to hardware and applications.
-   Enterprise Architecture \(formerly Application Portfolio Management\): Inventory of application hierarchy, associated business owner, and technology mapping.

## Prescribed metrics - IT Shared Services to Business Services

Following are the descriptions of each metric with an explanation of the weighting methodology and their related tables within the ServiceNow system.

**Note:** If the related tables have incomplete data or if there are gaps in the data, then the calculated weighting percentages are affected.

The preconfigured cost model begins with equal weighting to the next segment. Prescriptive metrics are available for more mature solutions.

-   **Allocate to Business Service based on CI count**

    The metric allocates shared service cost to business services based on the following weighting table:

    ![Allocate to Business Service based on CI count.](../image/PrescribedMetricSStoBS.png "Allocate to Business Service based on CI count")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all CIs and their relationship to their parent CI such as dependency, use, runs on, and contained by.
    -   The Service \[cmdb\_ci\_service\] table provides a list of all business services that are the parent CIs.
    -   The prescribed metric performs a count of CIs per parent and weights the cost to the business services accordingly.

        The weight table enforces lifespan on the following metric.

        -   Filters: Child.Class is not Business Service and Type is Depends on::Used by.
        -   Duration start: Actual start.
        -   Duration end: Actual end.
-   **Allocate to Business Service based on compute power**

    The metric allocates shared service cost to business services based on the following weighting table:

    ![Allocate to Business Service based on compute power.](../image/PrescribedMetricSStoBS.png "Allocate to Business Service based on compute power")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all CIs and their relationship to their parent CI such as dependency, use, runs on, and contained by.
    -   The Service \[cmdb\_ci\_service\] table provides a list of all business services, which are the parent CIs.
    -   The prescribed metric performs a count of CIs per server \(Child.Class\) and weights the cost to the \(parent\) business services accordingly.

        The weight table enforces lifespan on the following metric:

        -   Filters: Child.Class is Server and Type is Depends on::Used by.
        -   Duration start: Actual start.
        -   Duration end: Actual end.
-   **Allocate to Business Service based on database count**

    The metric allocates shared service cost to business services based on the following weighting table:

    ![Allocate to Business Service based on database count.](../image/PrescribedMetricSStoBS.png "Allocate to Business Service based on database count")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all CIs and their relationship to their parent CI such as dependency, use, runs on, and contained by.
    -   The Service \[cmdb\_ci\_service\] table provides a list of all business services, which are the parent CIs.
    -   The prescribed metric performs a count of CIs per database \(Child.Class\) and weights the cost to the \(parent\) business services accordingly.

        The weight table enforces lifespan on the following metric:

        -   Filters: Child.Class is Database and Type is Depends on::Used by.
        -   Duration start: Actual start.
        -   Duration end: Actual end.
-   **Allocate to Business Service based on change request volume**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Service based on change request volume.](../image/PrescribedMetricSStoBU.png "Allocate to Business Service based on change request volume")

    -   The Change Request \[change\_request\] table provides a list of all change requests and who requested it including the related business service.
    -   The Service \[cmdb\_ci\_service\] table provides a list of all business services.
    -   The prescribed metric performs a count of change requests per business service and weights the costs accordingly.

        The weight table enforces lifespan on the following metric:

        -   Duration start: Actual start.
        -   Duration end: Actual end.
        -   Enforce lifespan selected on the weight table.
-   **Allocate to Business Services based on incident volume**

    The metric allocates shared service cost to business unit based on the following weighting table:

    ![Allocate to Business Services based on incident volume.](../image/PrescribedMetricSStoBUonIV.png "Allocate to Business Services based on incident volume")

    -   The Incident \[incident.list\] table provides a list of all incidents, their related callers, and the related business service.
    -   The Service \[cmdb\_ci\_service\] table provides a list of all business services.
    -   The prescribed metric performs a count of incidents per business service \(opened and closed within the period\) and weights the costs accordingly.
        -   Duration start: Opened.
        -   Duration end: Resolved.
        -   Enforce lifespan selected on the weight table.

## Prescribed metrics - IT Shared Services to Business Applications

-   **Allocate to Applications using active user count**

    The metric allocates shared service cost to applications based on the following weighted metric:

    ![Allocate to Applications using active user count.](../image/PrescribedMetricSStoBAonUC.png "Allocate to Applications using active user count")

    -   The Business Application \[cmdb\_ci\_business\_app\] table provides a list of all business applications.
    -   The prescribed metric performs a sum of active users and weights the costs accordingly to the receiving applications by **Sys ID**.
-   **Allocate to Applications using database count**

    The metric allocates shared service cost to applications based on the following weighted metric:

    ![Allocate to applications using database count.](../image/PrescribedMetricSStoBAonDBCount.png "Allocate to Applications using database count")

    -   The CI Relationship \[cmdb\_rel\_ci\] table provides a list of all CIs and their relationship to their parent CI such as dependency, use, runs on, and contained by.
    -   The Business Application \[cmdb\_ci\_business\_app\] table provides a list of all business applications, which are the parent CIs.
    -   The prescribed metric performs a count of CIs per database \(Child.Class\) and weights the cost to the \(parent\) business application accordingly.
        -   Filters: Child.Class is Database and Type is Depends on::Used by.
        -   Duration start: Actual start.
        -   Duration end: Actual end.

## Prescribed metrics - Business Applications to Business Capabilities

Following is the scripted metric to allocate to business capabilities:

```
// Create a Scripted metric if you have complex logic to derive the weights for an Allocate to Segment.
//
// This Return Object is json:
// 1) key: The sys_id of the Allocate To segment's transaction table
// 2) value: the weight for the
//
// The API is called for each fiscal period and stored in weight Maps table which is in turn used in allocation.
// 'inputObject'  is available in the script to have access to fiscal period and from Account id.
// The  from account id is applicable only for "Allocate From" is part of metric setup where each entity in Allocate From table have their own weight distribution
// An 'inputObject' is injected during the evaluation of the script.
// It is an object of 2 key value pairs for fiscal period and allocate from accountId.
function getTopCapability(capabilityId){
  var now_GR = new GlideRecord('cmdb_ci_business_capability');
  gr.get(capabilityId);
   if(gr.isValidRecord())
    return getParentCapabilityRecur(now_GR);
 }
 function getParentCapabilityRecur(capabilityGr){
   if(JSUtil.nil(capabilityGr.parent))
    return capabilityGr;
  else
    return getParentCapabilityRecur(capabilityGr.parent.getRefRecord());
}
getScriptedWeightedMetric();
function getScriptedWeightedMetric(){
var appId = inputObject.from_id; // where inputObject.from_id is one of the Business Applications Id from Allocate From segment(Business Applications)
var relGr= new GlideRecord('cmdb_rel_ci');
relGr.addEncodedQuery('parent.sys_class_name=cmdb_ci_business_capability^child.sys_class_name=cmdb_ci_business_app');
relGr.addQuery('child',appId);
relGr.query();
var retObj={};
 while(relGr.next()){
   retObj[getTopCapability(relGr.parent).getUniqueValue()] = 1;
 }
 return retObj;
}

```

-   The Business Capability \[cmdb\_ci\_business\_capability\] table provides a list of all business capabilities and is part of Enterprise Architecture \(formerly Application Portfolio Management\).
-   The script, in essence, flattens the business capability list.

    **Note:** Everything should be related to its Level 0 Business Capability for Financial Modeling although applications within Enterprise Architecture \(formerly Application Portfolio Management\) may be assigned to lower-level capabilities.

    ![Scripted metric logic from APM to FM.](../image/PrescribedMetricBAtoBCScripted.png "Scripted metric logic from APM to FM")


**Parent Topic:**[The Cost Models tab - Legacy](c_TheCostModelsTab.md)

**Related topics**  


[Prescriptive cost models for shared services and business applications - Legacy](preconfigured-prescriptive-cost-models.md)

[View settings for each cost model - Legacy](../task/t_ViewSettingsForEachCostModel.md)

[Delete a cost model - Legacy](../task/t_DeleteACostModel.md)

[Compare cost models - Legacy](../task/t_CompareCostModels.md)

[Clone a cost model - Legacy](../task/t_CloneACostModel.md)

[Create breakdown relationship - Legacy](../task/t_CreateBreakdownRelationship.md)

