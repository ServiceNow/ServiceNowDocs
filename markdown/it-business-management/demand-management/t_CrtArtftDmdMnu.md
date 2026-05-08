---
title: Create an artifact from a demand
description: Create an artifact, such as a work item, from a demand so that you can track work on the demand.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create an artifact from a demand

Create an artifact, such as a work item, from a demand so that you can track work on the demand.

## Before you begin

A demand must have been created. For more information, see [Create a demand](t_CreatingDemands.md).

The category and type of a demand and the applications you have installed determine the artifact you can create from it. The available artifact types and the applications you must have installed to be able to create them are listed in the following table.

|Artifact|Required application|
|--------|--------------------|
|Enhancement, change, or defect|[Project Portfolio Suite](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)|
|Agile Development entities \(story or epic\)|[Agile Development 2.0](../../agile-development/reference/agile-landing-page.md)|
|Scaled Agile Framework \(SAFe\)SAFe entities \(story, feature, or epic\)|[Essential SAFe](../../agile-SAFe/concept/essential-overview.md) or [Portfolio SAFe](../../agile-SAFe/concept/portfolio-overview.md)|
|Enterprise Agile Planning \(EAP\) entities \(epic, feature, or capability\)|[Strategic Planning](../../alignment-planner-workspace/concept/alignment-planner-workspace-landing-page.md)|
|Improvement initiatives|Continual Improvement Management|

Role required: it\_demand\_manager

**Note:**

-   The sn\_apw\_advanced.eap\_user role is required to convert a demand to EAP entities.
-   The safe\_art\_user role is required to create a SAFe story.

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Open the demand for which you want to create an artifact.

3.  Verify that the values in the **Category** and **Type** fields are appropriate for the artifact you want to create.

    The options in the Type list change according to the category that you select. For more information, see [Demand form](../reference/demand-form.md).

    **Note:** The **Category** and **Type** fields are set to read only when an artifact is created from a demand. If you delete the created artifact, these fields become editable again.

4.  Select **Update**.

5.  Create the artifact by selecting the appropriate related link.

    Depending on the category and type of the demand, links related to the artifact you can create become available.

<table id="choicetable_plg_zcm_plb"><thead><tr><th align="left" id="d89676e293">

Related link

</th><th align="left" id="d89676e296">

Description

</th></tr></thead><tbody><tr><td id="d89676e302">

**Create Project**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Project**. Creates a project that is associated with this demand. The number of the project record is displayed in the **Project** field. For more information, see [Data migrated from a demand to a created project](../reference/data-copied-from-demand-to-project.md).

</td></tr><tr><td id="d89676e334">

**Create Enhancement**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Enhancement**. Creates an enhancement associated with this demand. Use enhancements to request improvements or new capabilities for existing features or services, for example, a request to add new UI elements. The number of the enhancement record is displayed in the **Enhancement** field.

</td></tr><tr><td id="d89676e358">

**Create Epic**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Epic**. Creates an Agile Development 2.0 epic that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Epic form.

</td></tr><tr><td id="d89676e389">

**Create Story**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Story**. Creates an Agile Development 2.0 story that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Story form.

</td></tr><tr><td id="d89676e423">

**Create EAP Epic**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Epic**. Creates an Enterprise Agile Planning \(EAP\) epic that is associated with this demand. A **Converted from** reference field is created in the EAP epic form.

</td></tr><tr><td id="d89676e464">

**Create EAP Feature**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Feature**. Creates an EAP feature that is associated with this demand. A **Converted from** reference field is created in the EAP feature form.

</td></tr><tr><td id="d89676e499">

**Create EAP Capability**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Capability**. Creates an EAP capability that is associated with this demand. A **Converted from** reference field is created in the EAP capability form.

</td></tr><tr><td id="d89676e532">

**Create SAFe Story**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to SAFe **Story**. Creates a Scaled Agile Framework \(SAFe\) story that is associated with this demand. A **Demand** reference field is created in the SAFe Story form.

</td></tr><tr><td id="d89676e563">

**Create SAFe Epic**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **SAFe Epic**. Creates an SAFe epic that is associated with this demand. A **Demand** reference field is created in the SAFe Epic form.

</td></tr><tr><td id="d89676e594">

**Create SAFe Feature**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **SAFe Feature**. Creates a SAFe feature that is associated with this demand. A **Demand** reference field is created in the SAFe Feature form.

</td></tr><tr><td id="d89676e626">

**Create Improvement Initiative**

</td><td>

This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Continual Improvement Management**. Creates an improvement initiative that is associated with this demand. Demand record to which the improvement initiative is linked is added to the **Source/Parent** field in the Details tab.**Note:** When the improvement is closed, the demand record is set to complete.

</td></tr><tr><td id="d89676e653">

**Create Change**

</td><td>

This link appears if the **Category** field is set to **Operational** and the **Type** field is set to **Change**. Creates a change that is associated with this demand. The number of the change record is displayed in the **Change** field.

</td></tr><tr><td id="d89676e677">

**Create Defect**

</td><td>

This link appears if the **Category** field is set to **Operational** and the **Type** field is set to **Defect**. Creates a defect that is associated with this demand. The number of the defect record is displayed in the **Defect** field.

</td></tr></tbody>
</table>
-   **[Create an Enterprise Agile Planning \(EAP\) entity from a demand](create-an-eap-entity-from-a-demand.md)**  
Create an Enterprise Agile Planning \(EAP\) entity, such as an epic, feature, or capability, from a demand so that you can start to work on these entities in Enterprise Agile Planning.

**Parent Topic:**[Create a demand](t_CreatingDemands.md)

