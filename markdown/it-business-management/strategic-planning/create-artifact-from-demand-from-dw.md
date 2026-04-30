---
title: Create an entity from a demand
description: Create an entity, such as a work item, from a demand so that you can track work on the demand.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-01-19"
reading_time_minutes: 5
breadcrumb: [Manage demands, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create an entity from a demand

Create an entity, such as a work item, from a demand so that you can track work on the demand.

## Before you begin

A demand must have been created. For more information, see [Create a demand](create-demand-from-dw.md).

The category and type of a demand and the applications you have installed determine the entity you can create from it. The available entity types and the applications you must have installed to be able to create them are listed in the following table.

|Entity|Required application|
|------|--------------------|
|Enhancement, change, or defect|[Project Portfolio Suite](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)|
|Agile Development entities \(story or epic\)|[Agile Development 2.0](../../agile-development/reference/agile-landing-page.md)|
|Enterprise Agile Planning \(EAP\) entities \(epic, feature, or capability\)|[Strategic Planning](../../alignment-planner-workspace/concept/alignment-planner-workspace-landing-page.md)|

Role required: it\_demand\_manager

**Note:** The sn\_apw\_advanced.eap\_user role is required to convert a demand to EAP entities.

## Procedure

1.  Open a demand from the home page of Next Experience for Demand Management.

    For more information, see [Access demands](access-demand-workspace.md).

2.  Verify that the values in the **Category** and **Type** fields are appropriate for the entity you want to create.

    The options in the Type list change according to the category that you select. For more information, see [Demand form](../reference/demand-form-dw.md).

    **Note:** The **Category** and **Type** fields are set to read only when an entity is created from a demand. If you delete the created entity, these fields become editable again.

3.  Select **Save**.

4.  Create the entity by selecting the appropriate option from the More Actions option.![Example of Create Project in the More Actions option.](../images/demand-create-entity.png)

    Depending on the category and type of the demand, options related to the entity you can create become available.

    |Option|Description|
    |------|-----------|
    |**Create Project**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Project**. Creates a project that is associated with this demand. The number of the project record is displayed in the **Project** field. For more information, see [Data migrated from a demand to a created project](../reference/data-migrated-from-demand-to-project-dw.md).|
    |**Create Enhancement**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Enhancement**. Creates an enhancement associated with this demand. Use enhancements to request improvements or new capabilities for existing features or services, for example, a request to add new UI elements. The number of the enhancement record is displayed in the **Enhancement** field.|
    |**Create Epic**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Epic**. Creates an Agile Development 2.0 epic that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Epic form.|
    |**Create Story**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Story**. Creates an Agile Development 2.0 story that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Story form.|
    |**Create EAP Epic**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Epic**. Creates an Enterprise Agile Planning \(EAP\) epic that is associated with this demand. A **Converted from** reference field is created in the EAP epic form.|
    |**Create EAP Feature**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Feature**. Creates an EAP feature that is associated with this demand. A **Converted from** reference field is created in the EAP feature form.|
    |**Create EAP Capability**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Capability**. Creates an EAP capability that is associated with this demand. A **Converted from** reference field is created in the EAP capability form.|
    |**Create Change**|This option appears if the **Category** field is set to **Operational** and the **Type** field is set to **Change**. Creates a change that is associated with this demand. The number of the change record is displayed in the **Change** field.|
    |**Create Defect**|This option appears if the **Category** field is set to **Operational** and the **Type** field is set to **Defect**. Creates a defect that is associated with this demand. The number of the defect record is displayed in the **Defect** field.|

    **Note:**

    -   For EAP entities, select the team that you want the EAP entity to be assigned to, in the **Team** field in the **EAP Details** section in the demand form. This field becomes read-only once the entity is created.
    -   Alternatively, you can create an entity using the **Confirm details and convert to selected entity** playbook activity. For more information, see [Use Playbooks](use-playbooks-in-dw.md).

**Related topics**  


[Use Playbooks](use-playbooks-in-dw.md)

[Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md)

