---
title: Enterprise Asset Management data model
description: The Enterprise Asset Management data model provides a structured framework for representing, tracking, and managing physical assets and their relationships throughout their life cycles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/eam-data-model.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 5
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Enterprise Asset Management data model

The Enterprise Asset Management data model provides a structured framework for representing, tracking, and managing physical assets and their relationships throughout their life cycles.

## Enterprise Asset Management data model overview

The Enterprise Asset Management data model defines how asset-related data is created, classified, synchronized, and governed. It is not a single table or diagram. Instead, it is a connected set of entities and relationships that act as guardrails for how asset-related data flows from initial definition through procurement, operation, maintenance, and retirement.

## Enterprise models and assets

The Enterprise Asset Management data model uses enterprise models and assets to separate standardized asset definitions from real-world physical objects.

-   An enterprise model defines an enterprise asset type. Each enterprise model contains a set of asset specifications, attributes, and structural compositions, including information about whether its associated assets are standalone or multi-component.
-   An enterprise asset represents a real-world physical object that is purchased, received, deployed, and tracked throughout its operational life. Every enterprise asset is created from an enterprise model.

## Core components of the Enterprise Asset Management data model

The Enterprise Asset Management data model is built around three core structural components: enterprise model classes, enterprise asset classes, and Configuration Management Database \(CMDB\) CI classes.

-   **Enterprise model classes**

    Enterprise model classes are tables that store enterprise model records. Records are organized by model type, such as the facility model or medical model. Each enterprise model class defines a set of attributes that are common to all enterprise model records stored within the given table. Extended enterprise model classes inherit attributes from their parent model classes, enabling consistent data standardization across related model types.

    For more information on enterprise model classes, see [Enterprise model and asset classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes.md).

-   **Enterprise asset classes**

    Enterprise asset classes are tables that store enterprise asset records. Records are organized by asset type, such as industrial assets or medical assets. Enterprise asset classes categorize assets based on their function or usage, helping you define maintenance strategies, compliance rules, and life-cycle workflows for different asset types.

    For more information on enterprise asset classes, see [Enterprise model and asset classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes.md).

-   **CMDB CI classes**

    CMDB CI classes are tables that store configuration item \(CI\) records. Each CMDB CI class maps to corresponding enterprise model and asset classes through model categories, creating a unified view of assets across the Enterprise Asset Management application and the CMDB.

    For more information on the CMDB and CMDB CI classes, see [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ITILConfigurationManagement.md).


These core components link to each other through enterprise model categories. Each enterprise model category maps an appropriate enterprise model class, enterprise asset class, and CMDB CI class together for a given enterprise asset type. The associated models, assets, and CIs can then work together across various workflows throughout the asset life cycle, including procurement and maintenance. For more information on model categories, see [Model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/model-hierarchy.md).

\[Omitted image "model-asset-ci-relationship.png"\] Alt text: Overview of how enterprise models, enterprise assets, and CIs link to each other.

## Enterprise Asset Management system architecture

The system architecture of the Enterprise Asset Management application is comprised of components that extend beyond the core data model components. Together, these components support the end-to-end asset management process, from procurement to disposal.

\[Omitted image "eam-system-architecture.png"\] Alt text: Enterprise Asset Management system architecture.

<table id="table_fxm_2hm_hjc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model management

</td><td>

Supported model management features and capabilities: -   Standardized asset definitions
-   Enterprise Asset Management Content Library
-   Enterprise model classifications

</td></tr><tr><td>

Discovery

</td><td>

Supported discovery features and capabilities:-   Service Graph Connectors
-   CI discovery aligned with enterprise model categories

</td></tr><tr><td>

Asset management

</td><td>

Supported asset management features and capabilities:-   Asset creation
-   Categorization of assets by asset type
-   Linear asset management
-   Bi-directional asset and CI synchronization
-   Financial data tracking

</td></tr><tr><td>

Functional modules

</td><td>

Supported functional modules in which you can perform tasks and complete workflows:-   Life-cycle workflows
-   Analytics
-   Inventory management
-   Work management
-   Procurement management
-   Contract management
-   Location hierarchies and indoor maps

</td></tr><tr><td>

Capabilities

</td><td>

Supported capabilities within each functional module. Examples include asset onboarding and stockroom management.

 For the complete list of capabilities within each module, refer to the previous [Enterprise Asset Management system architecture diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md).

</td></tr></tbody>
</table>-   **[Enterprise model and asset classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes.md)**  
The Enterprise Asset Management application supports enterprise model and asset classes that extend base classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, and dependent relationships.
-   **[Model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/model-hierarchy.md)**  
Model categories define the relationships between enterprise model classes, enterprise asset classes, and Configuration Management Database \(CMDB\) CI classes in Enterprise Asset Management. Model categories connect every enterprise asset to the correct model class, asset class, and CI class.
-   **[Model classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/classification-codes.md)**  
Use model classification to organize and categorize enterprise models and their associated assets in a structured, consistent way across the ServiceNow platform.
-   **[Model types in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-model-types.md)**  
Every enterprise model in the Enterprise Asset Management application is assigned a model type that determines its structural nature. Each enterprise model can represent standalone enterprise assets, quantity-tracked consumable assets, or complex assemblies that are comprised of multiple components.
-   **[Asset groups in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/asset-groups-eam.md)**  
Asset groups in the Enterprise Asset Management application provide a systematic approach to organizing assets based on their functional relationships and their physical placement within an organization. They can help improve data integrity and support maintenance planning, life-cycle tracking, reporting, and access control.
-   **[Linear assets in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/using-linear-assets.md)**  
Expand your asset management portfolio by creating and managing linear assets.

**Parent Topic:**[IT Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/it-asset-management.md)

