---
title: Create an artifact from a demand
description: Create an artifact, such as a work item, from a demand so that you can track work on the demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/demand-management/t\_CrtArtftDmdMnu.html
release: zurich
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create an artifact from a demand

Create an artifact, such as a work item, from a demand so that you can track work on the demand.

## Before you begin

A demand must have been created. For more information, see [Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/t_CreatingDemands.md).

The category and type of a demand and the applications you have installed determine the artifact you can create from it. The available artifact types and the applications you must have installed to be able to create them are listed in the following table.

|Artifact|Required application|
|--------|--------------------|
|Enhancement, change, or defect|[Project Portfolio Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/ppm-collaboration/c_ProjectPortfolioSuite.md)|
|Agile Development entities \(story or epic\)|[Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/agile-development/agile-landing-page.md)|
|Scaled Agile Framework \(SAFe\)SAFe entities \(story, feature, or epic\)|[Essential SAFe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scaled-agile-framework-safe/essential-overview.md) or [Portfolio SAFe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scaled-agile-framework-safe/portfolio-overview.md)|
|Enterprise Agile Planning \(EAP\) entities \(epic, feature, or capability\)|[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/alignment-planner-workspace-landing-page.md)|

Role required: it\_demand\_manager

**Note:**

-   The sn\_apw\_advanced.eap\_user role is required to convert a demand to EAP entities.
-   The safe\_art\_user role is required to create a SAFe story.

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Open the demand for which you want to create an artifact.

3.  Verify that the values in the **Category** and **Type** fields are appropriate for the artifact you want to create.

    The options in the Type list change according to the category that you select. For more information, see [Demand form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/demand-form.md).

    **Note:** The **Category** and **Type** fields are set to read only when an artifact is created from a demand. If you delete the created artifact, these fields become editable again.

4.  Select **Update**.

5.  Create the artifact by selecting the appropriate related link.

    Depending on the category and type of the demand, links related to the artifact you can create become available.

    |Related link|Description|
    |------------|-----------|
    |**Create Project**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Project**. Creates a project that is associated with this demand. The number of the project record is displayed in the **Project** field. For more information, see [Data migrated from a demand to a created project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/data-copied-from-demand-to-project.md).|
    |**Create Enhancement**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Enhancement**. Creates an enhancement associated with this demand. Use enhancements to request improvements or new capabilities for existing features or services, for example, a request to add new UI elements. The number of the enhancement record is displayed in the **Enhancement** field.|
    |**Create Epic**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Epic**. Creates an Agile Development 2.0 epic that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Epic form.|
    |**Create Story**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **Story**. Creates an Agile Development 2.0 story that is associated with this demand. A **Demand** reference field is created in the Agile Development 2.0 Story form.|
    |**Create EAP Epic**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Epic**. Creates an Enterprise Agile Planning \(EAP\) epic that is associated with this demand. A **Converted from** reference field is created in the EAP epic form.|
    |**Create EAP Feature**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Feature**. Creates an EAP feature that is associated with this demand. A **Converted from** reference field is created in the EAP feature form.|
    |**Create EAP Capability**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **EAP Capability**. Creates an EAP capability that is associated with this demand. A **Converted from** reference field is created in the EAP capability form.|
    |**Create SAFe Story**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to SAFe **Story**. Creates a Scaled Agile Framework \(SAFe\) story that is associated with this demand. A **Demand** reference field is created in the SAFe Story form.|
    |**Create SAFe Epic**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **SAFe Epic**. Creates a SAFe epic that is associated with this demand. A **Demand** reference field is created in the SAFe Epic form.|
    |**Create SAFe Feature**|This link appears if the **Category** field is set to **Strategic** and the **Type** field is set to **SAFe Feature**. Creates a SAFe feature that is associated with this demand. A **Demand** reference field is created in the SAFe Feature form.|
    |**Create Change**|This link appears if the **Category** field is set to **Operational** and the **Type** field is set to **Change**. Creates a change that is associated with this demand. The number of the change record is displayed in the **Change** field.|
    |**Create Defect**|This link appears if the **Category** field is set to **Operational** and the **Type** field is set to **Defect**. Creates a defect that is associated with this demand. The number of the defect record is displayed in the **Defect** field.|


-   **[Create an Enterprise Agile Planning \(EAP\) entity from a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/create-an-eap-entity-from-a-demand.md)**  
Create an Enterprise Agile Planning \(EAP\) entity, such as an epic, feature, or capability, from a demand so that you can start to work on these entities in Enterprise Agile Planning.

**Parent Topic:**[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/t_CreatingDemands.md)

