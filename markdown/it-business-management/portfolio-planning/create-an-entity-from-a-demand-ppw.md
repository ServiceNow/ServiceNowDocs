---
title: Create an entity from a demand
description: Create an entity, such as a work item, from a demand so that you can track work on the demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/create-an-entity-from-a-demand-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Create an entity from a demand

Create an entity, such as a work item, from a demand so that you can track work on the demand.

## Before you begin

A demand must have been created. For more information, see [Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/create-a-demand-ppw.md).

The category and type of a demand and the applications you have installed determine the entity you can create from it. The following table lists the available entity types and the applications you must have installed to create them.

|Entity|Required application|
|------|--------------------|
|Enhancement, change, or defect|[Project Portfolio Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/ppm-collaboration/c_ProjectPortfolioSuite.md)|
|Agile Development entities \(story or epic\)|[Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/agile-landing-page.md)|
|Enterprise Agile Planning \(EAP\) entities \(epic, feature, or capability\)|[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/alignment-planner-workspace-landing-page.md)|

Role required: it\_demand\_manager

**Note:** The sn\_apw\_advanced.eap\_user role is required to convert a demand to EAP entities.

## About this task

To create an entity, you can also use the **Confirm details and convert to selected entity** Playbook activity. For more information, see [Use Playbook in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/use-playbooks-in-ppw.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select **Details** from the navigation menu.

5.  Verify that the values in the **Category** and **Type** fields are appropriate for the entity you want to create.

    The options in the Type list change according to the category that you select. For more information, see [Demand form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/demand-form-ppw.md).

    **Note:** The **Category** and **Type** fields are set to read only when an entity is created from a demand. If you delete the created entity, these fields are set to editable again.

6.  Select **Save**.

7.  Select the More Actions option.

8.  Select the appropriate option to create an entity.

    \[Omitted image "demand-create-entity.png"\] Alt text: Create Project selected in the More Actions menu.

    Options vary depending on the category and type of the demand.

    |Option|Description|
    |------|-----------|
    |**Create Project**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Project**. Creates a project that is associated with this demand. The number of the project record is displayed in the **Project** field. For more information, see [Data migrated from a demand to a created project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/data-migrated-from-demand-project-dw.md).|
    |**Create Enhancement**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Enhancement**. Creates an enhancement associated with this demand. Use enhancements to request improvements or new capabilities for existing features or services, for example, a request to add new UI elements. The number of the enhancement record is displayed in the **Enhancement** field.|
    |**Create Epic**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Epic**. Creates an Agile Development 2.0 epic that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Epic form.|
    |**Create Story**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Story**. Creates an Agile Development 2.0 story that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Story form.|
    |**Create EAP Epic**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Epic**. Creates an Enterprise Agile Planning \(EAP\) epic that is associated with this demand. A **Converted from** reference field is created in the EAP epic form.|
    |**Create EAP Feature**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Feature**. Creates an EAP feature that is associated with this demand. A **Converted from** reference field is created in the EAP feature form.|
    |**Create EAP Capability**|This option appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Capability**. Creates an EAP capability that is associated with this demand. A **Converted from** reference field is created in the EAP capability form.|
    |**Create Change**|This option appears if the **Category** field is set to **Operational** and the **Type** field is set to **Change**. Creates a change that is associated with this demand. The number of the change record is displayed in the **Change** field.|
    |**Create Defect**|This option appears if the **Category** field is set to **Operational** and the **Type** field is set to **Defect**. Creates a defect that is associated with this demand. The number of the defect record is displayed in the **Defect** field.|

    **Note:** For EAP entities, select the team that you want the EAP entity to be assigned to, in the **Team** field in the **EAP Details** section in the demand form. This field is set to read-only once the entity is created.


