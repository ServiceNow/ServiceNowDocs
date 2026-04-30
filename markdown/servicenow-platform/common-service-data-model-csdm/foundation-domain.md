---
title: Foundation domain in the CSDM framework
description: The Foundation domain involves tables that contain base data that is referenced from or to objects in the other CSDM domains. Foundation data is required before you can use ServiceNow products or add data to the CMDB.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [CSDM data domains, Explore, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Foundation domain in the CSDM framework

The Foundation domain involves tables that contain base data that is referenced from or to objects in the other CSDM domains. Foundation data is required before you can use ServiceNow products or add data to the CMDB.

The tables in the Foundation domain aren't used in Configuration Management Database \(CMDB\) relationships. Instead, the tables contain critical referential data. Typical users of the domain are process owners, data stewards, product owners, and contract managers.

![Foundation domain.](../image/foundation-domain.png)

## Business process

A business process has a well-defined start and finish. Examples of business processes in the banking industry are the customer onboarding process and the credit check process. Each business process can have levels of criticality and impact. Business processes are stored in the cmdb\_ci\_business\_process table.

In a parent-child relationship, business processes can be identified by using the parent attribute as a reference to a parent business process.

The business process is a manually-maintained CI that can identify declared and determined criticality as well as impact to confidentiality, integrity, and availability. Business processes can be reviewed monthly, quarterly, semi-annually, or annually. In addition, the next review date can be recorded. For further information, see [Business process management](https://www.servicenow.com/docs/access?context=business-process-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) and [Create a business process](https://www.servicenow.com/docs/access?context=create-a-business-process&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

## Contracts

A contract is a binding agreement between two parties. In the ServiceNow AI Platform, contracts contain detailed information such as the contract number, start and end dates, active status, terms and conditions statements, documents, renewal information, and financial terms.

-   A contract is not a CI. Contracts use contract model types from the [Product Models](https://www.servicenow.com/docs/access?context=c_CreateAProductModel&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) module. Contracts are stored in the \[ast\_contract\] table.
-   Use the Contract Management application to manage and track contracts. See [Contract Management application](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).
-   In the Service Level Management application, contracts group together SLAs that relate to a single vendor or customer, as well as the CIs, locations, groups, users, and child contracts that are related to the contract. For more information, see [Define a service contract](https://www.servicenow.com/docs/access?context=define-a-service-contract&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).
-   Service contracts used by Vendor Management Workspace can support hardware CIs as part of an SLA.
-   In the Customer Service Management product, service contracts define the type of support that customers receive. A contract can include an account and contact or a consumer and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs. See [Define a service contract in Customer Service Management](https://www.servicenow.com/docs/access?context=create-csm-service-contracts&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

## Products and product models

A product model is a specific version or configuration of a product used to manage and track applications on the ServiceNow AI Platform. Product models identify the product owner, team, product status, compatibility with other products, reference to product catalog, and reference objects in the various stages of a product's life cycle. For more information, see [Product catalog](https://www.servicenow.com/docs/access?context=c_ProductCatalog&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

Additionally, you can identify the products reaching end-of-life as defined by third party providers or internal product owners. You can also bundle other products as components to represent the set of products that your organization develops, sells, or uses.

Product models are extended into seven base types: application model \(version agnostic\), software model \(version specific\),contract model, facility model, hardware model, consumable model, service model. Products might be bundled to create a collection or group of products, for example a FlashBlade server \(hardware model\), or a 24/7 support service \(service model\).

![Technical product model table hierarchy.](../image/product-model-technical.png)

Product models are stored in the \[cmdb\_model\] table or the extended tables aligned to the seven base types. The product model tables are not CIs. Configuration items can use the **Model ID** attribute to reference product models. For example, a service offering CI might reference a particular service model that other service offerings of the same type also reference.

Application, service, and software class instance CIs aren't created through Discovery, so their **Model ID \[model\_id\]** values might not refer to product model records. To help you to migrate to a product-centric management paradigm, each instance of a logical CI should be associated with a product model. See [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

## CMDB group

A CMDB group is a collection of CIs \(but is not, itself, a CI\). A group is based on the results of saved Query Builder queries, encoded queries, or manual entries. You can apply an action to all members of a group at one time.

You can work with a CMDB group across the ServiceNow AI Platform.

![CMDB group.](../image/cmdb-group-found-domain.png)

-   For the CSDM, the Dynamic CI Group references a CMDB group to provide a list of CIs based on a common criteria.
-   CMDB groups are stored in the table \[cmdb\_group\].
-   The CMDB group can potentially replace the spreadsheets that you might be using to group your CIs.

For additional information, see [CMDB groups](../../../Chunk1292530847.md#).

## Life-cycle value pairs

life-cycle value pairs track the life cycles for products, assets, contracts, CIs, locations, and other objects. Using the standard CSDM life-cycle values consistently helps you to effectively track objects through their transitions over time. Reporting can therefore accurately reflect the actual states of CIs: usage, availability, end of support, and so on.

See the ServiceNow Community video: [CSDM V4 product and life cycle discussion](https://www.youtube.com/watch?v=TfRv1VTRsgM)

The standard CSDM life-cycle value pair covers all phases of a product instance life cycle.

-   A **life cycle stage** is one of the broad phases that a CI moves through, from inception or procurement to operation and then to end of life.
-   **life cycle stage status** is the particular status of a CI within its current life cycle stage.

For example, a hardware CI in the **Operational** stage might change stage status over time from **In Use** to **In Maintenance** to **End of Support**. A different hardware CI might go from **In Use** to **End of Support** without ever having been in **In Maintenance** status.

![Allowed life-cycle values during the Operational stage of a hardware CI's life cycle](../image/csdm-op-stage-of-hw-ci.png)

When you enable the CSDM framework, you can start using the **Life Cycle Stage** and **Life Cycle Stage Status** values to track an asset's life cycle. To use the fields, follow the procedure described in [Activate the CSDM plugin](../task/csdm-enable.md). The following processes can use the life-cycle value pairs:

-   [Product life cycle](csdm-lifecycle-product.md)
-   [Hardware life cycle](csdm-lifecycle-hardware.md)
-   [Logical life cycle](csdm-lifecycle-logical.md)
-   [Document life cycle](csdm-lifecycle-document.md)
-   [Location life cycle](csdm-lifecycle-location.md)

## Legacy status values are auto-updated

The following legacy statuses are automatically mapped to the **Life Cycle Stage** and **Life Cycle Stage Status** fields when you follow the procedure described in [Activate the CSDM plugin](../task/csdm-enable.md).

**Important:** Legacy field values are not deleted after you map them to **Life Cycle Stage** and **Life Cycle Stage Status** values.

-   Product Model Status
-   Asset State
-   Asset Substate
-   Contract Status
-   CI Install Status
-   CI Operational Status
-   CI Hardware Status
-   CI Hardware Substatus

## Map existing status values to CSDM life-cycle value pairs

Use the Life Cycle Mapping module \(**CSDM** &gt; **Life Cycle Mapping**\) to specify how your existing life-cycle values should be converted to CSDM life-cycle value pairs. The mapping ensures ServiceNow AI Platform products "see" legacy CIs in your environment. In this example, the existing **Pending Install** value of the **Install Status** attribute for hardware CIs will always map to **Deploy/Test** life-cycle value pairs in the CMDB. See [Map legacy status values to CSDM life-cycle values](../../configuration-management/concept/csdm-life-cycle-standard-values.md#) and [Activate align and sync for CSDM life-cycle values](../../configuration-management/concept/csdm-life-cycle-standard-values.md#).

![Assign CSDM life-cycle values to existing legacy values.](../image/csdm-lifecycle-mapping-form.png)

## Common data

Common data elements are not configuration items. Common data is shared and used throughout the ServiceNow AI Platform. Common data includes organizational structure \(Company, Business Unit, Department\), locations, groups, and users. Many ServiceNow AI Platform products depend on common data to provide business value.

Planning your common data is essential to the effective implementation of ServiceNow AI Platform products and features. Consider the following issues:

-   Do you have a trusted source for the data?
-   Do you have multiple data sources?
-   How often does the data change?
-   Do you have the depth of data that the CIs require?
-   Who maintains the data?

Common data is stored in the following tables:

-   Company: \[core\_company\]
-   Business unit: \[business\_unit\]
-   Department: \[cmn\_department\]
-   Location: \[cmn\_location\]
-   Groups: \[sys\_user\_group\]
-   Users: \[sys\_user\]

## Location management

Data that comes from multiple sources and federated integrations is difficult to maintain. The following attributes have been added to the location \(cmn\_location\) table to simplify management:

-   **Source**: The origin of the location record.
-   **Location type**: The position of the location record in the hierarchy of locations. You can use the following options to create a hierarchy of location data to suit your requirements: Region, County, State/Province, City, Site, Building/Structure, Floor, and Room.
-   **Managed by group**: The group that governs or manages this location record.
-   **Validation** \(duplicate and primary\): Flag duplicate records and manually filter locations that are not be displayed.
-   **Life cycle stage** and **Life cycle stage status**: See [Life-cycle value pairs](foundation-domain.md#section-life-cycle-states).

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[Common Service Data Model — conceptual model](csdm-conceptual-model.md)

