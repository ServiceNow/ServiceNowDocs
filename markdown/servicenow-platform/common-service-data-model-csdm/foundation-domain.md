---
title: Foundation domain in the CSDM model
description: Tables in the Foundation domain contain base data that is referenced from or to objects in the other CSDM domains. Before you can use ServiceNow products, you must populate foundational data.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Foundation domain in the CSDM model

Tables in the Foundation domain contain base data that is referenced from or to objects in the other CSDM domains. Before you can use ServiceNow products, you must populate foundational data.

The tables in the Foundation domain aren't used in CMDB relationships. Instead, the tables contain critical referential data. Typical users of the domain are process owners, data stewards, product owners, and contract managers.

![Foundation domain of the CSDM framework.](../image/domain-foundation-tables.png)

**Note:** For an introductory walk-through of the tables and attributes that you should populate for any domain, see the videos listed in [CSDM resources](../reference/csdm-resources.md).

## Foundation domain tables used during the service life cycle

Individual Foundation domain tables are accessed as needed during each phase of the service life cycle. Each topic that describes the life-cycle phase of a domain identifies the foundation tables that are active during that phase. See the following diagrams:

-   [Tables used during the Ideation &amp; Strategy phase of the service life cycle](ideation-strategy-domain.md#section-idea-strat-active-tables)
-   [Tables used during the Design &amp; Planning phase of the service life cycle](design-domain.md#section-design-plan-active-tables)
-   [Tables used during the Build &amp; Integration phase of the service life cycle](build-domain.md#section-build-integr-active-tables)
-   [Tables used during the Service Delivery phase of the service life cycle](manage-tech-servs-domain.md#section-service-deliv-active-tables)
-   [Tables used during the Service Consumption phase of the service life cycle](sell-consume-domain.md#section-service-consume-active-tables)

## Data managed by the chief strategist: Value stream

Value stream: A value stream is the set of actions that take place to add value to a customer from the initial request through realization of value by the customer. The value stream begins with the initial concept, moves through various stages of development and on through delivery and support. A value stream always begins and ends with a customer. The value stream is aligned with your organization's business processes.

## Data managed by the process owner: Business processes

A business process has a well-defined start and finish. Examples of business processes in the banking industry are the customer onboarding process and the credit check process. Each business process can have levels of criticality and impact. Business processes are stored in the cmdb\_ci\_business\_process table.

In a parent-child relationship, business processes can be identified by using the parent attribute as a reference to a parent business process.

The business process is a manually-maintained CI that can identify declared and determined criticality as well as impact to confidentiality, integrity, and availability. Business processes can be reviewed monthly, quarterly, semi-annually, or annually. In addition, the next review date can be recorded. For further information, see [Business process management](https://www.servicenow.com/docs/access?context=business-process-overview&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) and [Create a business process](https://www.servicenow.com/docs/access?context=create-a-business-process&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

## Data managed by the contract manager: Contracts

A contract is a binding agreement between two parties. In the ServiceNow AI Platform, contracts contain detailed information such as the contract number, start and end dates, active status, terms and conditions statements, documents, renewal information, and financial terms.

-   A contract is not a CI. Contracts use contract model types from the [Product Models](https://www.servicenow.com/docs/access?context=c_CreateAProductModel&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) module. Contracts are stored in the \[ast\_contract\] table.
-   Use the Contract Management application to manage and track contracts. See [Contract Management application](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).
-   In the Service Level Management application, contracts group together SLAs that relate to a single vendor or customer, as well as the CIs, locations, groups, users, and child contracts that are related to the contract. For more information, see [Define a service contract](https://www.servicenow.com/docs/access?context=define-a-service-contract&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).
-   Service contracts used by Vendor Management Workspace can support tangible/physical CIs as part of an SLA.
-   In the Customer Service Management product, service contracts define the type of support that customers receive. A contract can include an account and contact or a consumer and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs. See [Define a service contract in Customer Service Management](https://www.servicenow.com/docs/access?context=create-csm-service-contracts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

For more information, see [Definitions of life-cycle values for document and contract entities](../reference/csdm-lifecycle-df-document.md).

## Data managed by the product owner

-   **Products and product models**

    Products might be bundled to create a collection or group of products, for example a FlashBlade server \(hardware model\), or a 24/7 support service \(service model\). Additionally, you can identify the products reaching end-of-life as defined by third-party providers or internal product owners. You can also bundle other products as components to represent the set of products that your organization develops, sells, or uses.

    A product model is a specific version or configuration of a product used to manage and track applications on the ServiceNow AI Platform. The Product Model tables are not CIs. CIs reference Product Models using the **Model ID** attribute \(available on all CMDB tables\). For example, a Service Offering CI may reference a Service Offering Model, while a Windows Server may reference a Hardware Model.

    Product models identify the product owner, team, product status, compatibility with other products, reference to product catalog, and reference objects in the various stages of a product's life cycle.

    Product Models are recorded in the \[cmdb\_model\] table through the following extended tables, known as product model classes.

    -   Application Model \[cmdb\_application\_product\_model\] \(version-agnostic\)
    -   Software Model \[cmdb\_software\_product\_model\] \(version-specific\)
    -   Contract Model \[cmdb\_contract\_product\_model\]
    -   Facility Model \[cmdb\_facility\_product\_model\]
    -   Hardware Model \[cmdb\_hardware\_product\_model\] \(tangible/physical devices\)
    -   Consumable Model \[cmdb\_consumable\_product\_model\]
    -   Service Model \[cmdb\_service\_product\_model\]
    Application, service, and software class instance CIs aren't created through Discovery, so their **Model ID \[model\_id\]** values might not refer to product model records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. For recommendations, see [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

-   **Product features**

    In digital product release, a feature \(what you're developing toward\) exists in a particular version of software or service.

-   **Software bills of material \(SBOMs\)**

    An SBOM is the overall collection of components of a piece of software.

    Cyclone DX is supported.


## Data managed by the data steward

-   **CMDB groups**

    A CMDB group is a collection of CIs \(but is not, itself, a CI\). A group is based on the results of saved Query Builder queries, encoded queries, or manual entries. You can apply an action to all members of a group at one time.

    -   You can work with a CMDB group across the ServiceNow AI Platform.
    -   For the CSDM, the Dynamic CI Group references a CMDB group to provide a list of CIs based on a common criteria.
    -   CMDB groups are stored in the Group \[cmdb\_group\] table.
    -   The CMDB group can potentially replace the spreadsheets that you might be using to group your CIs.
    For more information, see [CMDB groups](../../configuration-management/concept/cmdb-groups.md#).

-   **Locations**

    Data that comes from multiple sources and federated integrations is difficult to maintain. The following attributes have been added to the location \[cmn\_location\] table to simplify management:

    -   **Source**: The origin of the location record.
    -   **Location type**: The position of the location record in the hierarchy of locations. You can use the following options to create a hierarchy of location data to suit your requirements: Region, County, State/Province, City, Site, Building/Structure, Floor, and Room.
    -   **Managed by group**: The group that governs or manages this location record.
    -   **Validation** \(duplicate and primary\): Flag duplicate records and manually filter locations that are not be displayed.
    -   **Life cycle stage** and **Life cycle stage status**.
-   **Life-cycle values**

    life-cycle value pairs track the life cycles for products, assets, contracts, CIs, locations, and other objects. Using the standard CSDM life-cycle values consistently helps you to effectively track objects through their transitions over time. Reporting can therefore accurately reflect the actual states of CIs: usage, availability, end of support, and so on.

    When you enable the CSDM framework, you can start using the **Life Cycle Stage** and **Life Cycle Stage Status** values to track an asset's life cycle. To use the fields, follow the procedure described in [Activate the CSDM plugin](../task/csdm-enable.md). The following processes can use the life-cycle value pairs:

    -   [Life cycle of product entities](csdm-lifecycle-product.md)
    -   [Life cycle of tangible/physical CIs](csdm-lifecycle-hardware.md)
    -   [Life cycle of intangible/logical entities](csdm-lifecycle-logical.md)
    -   [Life cycle of document and contract entities](csdm-lifecycle-document.md)
    -   [Life cycle of location entities](csdm-lifecycle-location.md)
    See the ServiceNow Community video: [CSDM V4 product and life cycle discussion](https://www.youtube.com/watch?v=TfRv1VTRsgM)


## Common data managed by the data steward

Common data is stored in the following tables:

-   Company: \[core\_company\]
-   Business unit: \[business\_unit\]
-   Department: \[cmn\_department\]
-   Location: \[cmn\_location\]
-   Groups \[sys\_user\_group\] and users \[sys\_user\]. When the full definition of a CI requires that you identify the contact groups that are associated with the CI, you can add that data in the **Teams** related list for the CI.

Common data elements are not configuration items. Common data is shared and used throughout the ServiceNow AI Platform. Common data includes organizational structure \(Company, Business Unit, Department\), locations, groups, and users. Many ServiceNow AI Platform products depend on common data to provide business value.

Planning your common data is essential to the effective implementation of ServiceNow AI Platform products and features. Consider the following issues:

-   Do you have a trusted source for the data?
-   Do you have multiple data sources?
-   How often does the data change?
-   Do you have the depth of data that the CIs require?
-   Who maintains the data?

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM data domains](csdm-conceptual-model.md)

