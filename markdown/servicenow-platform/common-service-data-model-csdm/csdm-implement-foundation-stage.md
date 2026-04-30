---
title: CSDM implementation stages — Foundation
description: In the Foundation stage of implementing the CSDM framework, you prepare the referential data that enables accurate reporting to support good business decisions. Use the base-system tables when you begin implementing the CSDM to derive the highest value from your ServiceNow products and the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM implementation stages — Foundation

In the Foundation stage of implementing the CSDM framework, you prepare the referential data that enables accurate reporting to support good business decisions. Use the base-system tables when you begin implementing the CSDM to derive the highest value from your ServiceNow products and the ServiceNow AI Platform.

## Benefits of preparing the data in the Foundation stage

The basis of any good data model is the foundational data that is referenced throughout the model.

-   The base-system tables act as the foundation for many ServiceNow products.
-   The tables help your company align with reporting requirements early to expedite the value you get from the CSDM. You can reduce or eliminate costly rework tasks needed to align with reporting requirements.

## Tables that you work on during the Foundation stage

![Tables that you work on during the Foundation stage.](../image/foundation-domain.png)

-   **Business Process table \[cmdb\_ci\_business\_process\]**

    A business process has a well-defined start and finish. Examples of business processes in the banking industry are the customer onboarding process and the credit check process. Each business process can have levels of criticality and impact. Business processes are stored in the cmdb\_ci\_business\_process table.

-   **Contract table \[ast\_contract\]**

    The Contract table identifies binding agreements between two parties. When you populate services provided by vendors into the CMDB, consider the role that contracts play when evaluating service level agreements \(SLAs\).

-   **Product model table \[model\_id\]**

    The Product model table \[model\_id\] identifies the unique types of products your organization develops or consumes. When you group assets and CIs by product model, you unify and relate CIs that are part of the same digital product and portfolios of products. Grouping assets and CIs by product model can help you plan projects, monitor costs, and rationalize your data. Discovery can populate hardware product models after they’re operational, but other types of product models require planning from product owners.

    Use the CSDM Product Model Assignment job to auto-generate a product model record \(application model, service model, or software model\) for each logical CI that is not yet associated with a product model. Product models are ideal for associating CIs that are parts of a single digital product. See [Auto-generate product models for logical CIs](../task/csdm-auto-create-prod-model-for-ci.md).

-   **CMDB Group table \[cmdb\_ci\_query\_based\_service\]**

    The CMDB Group table identifies a collection of CIs based on the results of saved Query Builder queries, encoded queries, or manual entries. CMDB groups are critical elements of Dynamic CI groups and the strategic management of CIs. Decide early how you want to report CI information and how you want to monitor CIs. These decisions affect how you create CMDB groups.

-   **Location table \[cmn\_location\]**

    The Location table uniquely identifies geographic locations. You can create a hierarchy of location data using the Parent attribute. The hierarchy might include entries that match your reporting requirements. For example, you could populate the location table as follows

    ![Location reporting.](../image/location-flow.png "Your organization's location attributes")

    To include more detail in reports, you could extend the Location table to include floors, rooms, and even datacenters. With hierarchy capabilities, trusted source data, and your requirements in hand, you can create locations that support your future reporting needs.

-   **Group table \[sys\_user\_group\]**

    The Group table identifies sets of users that share a common purpose. Groups may perform tasks such as approving change requests, resolving incidents, receiving email notifications, or performing work order tasks. Groups also use the referential data in the CMDB to identify how CIs are managed \(for example, the Managed by group\) and supported \(for example, the Support group\). Any business rules, assignment rules, system roles, or attributes that refer to a group automatically apply to all group members.

-   **User table \[sys\_user\]**

    The User table identifies the persons and applications that have access to your ServiceNow instance. You can organize users into groups that are associated with the Company, Business Unit, and Department tables.

-   **Organizational structure**

    Organization structure tables identify internal business structures and external customers, manufacturers, and vendors.

    -   **Company table \[core\_company\]**

        The Company table is populated with the legal entities of companies. Entities can be either internal \(your organization\) or external. You can use the Parent attribute to build a hierarchy. Consider the legal entities that you need for reporting when the CMDB is populated.

        -   Internal entries should focus on a hierarchy of legal entities rather than a hierarchy of business units within a legal entity.
        -   External entries are identified by a True or False flag. The Customer flag identifies your external customers.

            The Manufacturer flag identifies companies that create products that you consume. An internal organization might be a manufacturer.

        -   The Vendor flag identifies organizations that provide products that you purchase. An internal organization might be a vendor.
    -   **Business Unit table \[business\_unit\]**

        The hierarchy of your business is populated in the Business Unit table with a reference to the parent company. A business unit is a part of your organization that is responsible for specific operations, such as finance, human resources \(HR\), or IT. A hierarchy within a business unit is common. For large multinational organizations, you might have business units that identify independent regional operations and the specific operations within the region.

    -   **Department table \[cmn\_department\]**

        The Department table includes a finer level of detail about a business unit. The Department table gives you another way to categorize users, groups, assets, and CIs.

-   **Life cycle tables**

    CSDM life-cycle value pairs track the life cycles for products, assets, contracts, CIs, locations, and other objects. Using the standard values consistently helps you to track objects through their transitions over time. Reporting can therefore accurately reflect the actual states of CIs: usage, availability, end of support, and so on.

    The standard CSDM life-cycle value pair covers all phases of a product instance life cycle.

    -   A **life cycle stage** is one of the broad phases that a CI moves through, from inception or procurement to retirement and end of life.
    -   **life cycle stage status** is the particular status of a CI within its current life cycle stage.
    For example, a hardware CI in the **Operational** stage might change status over time from **In Use** to **In Maintenance** to **End of Support**. A different hardware CI might go from **In Use** to **End of Support** without ever having been in **In Maintenance** status.

    ![Allowed life-cycle values during the Operational stage of a hardware CI's life cycle](../image/csdm-op-stage-of-hw-ci.png)

    **Note:** The \[life\_cycle\_control\] table uses the type of CI \(hardware, document, logical and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

    To take full advantage of the CSDM life-cycle standards, you can map legacy status data to the life-cycle value pairs. See [Enabling CSDM life-cycle sync between legacy fields and related assets](../../configuration-management/concept/csdm-life-cycle-standard-values.md#).

    The following assets can use life-cycle value pairs:

    -   [Product life cycle](csdm-lifecycle-product.md)
    -   [Hardware life cycle](csdm-lifecycle-hardware.md)
    -   [Logical life cycle](csdm-lifecycle-logical.md)
    -   [Document life cycle](csdm-lifecycle-document.md)
    -   [Location life cycle](csdm-lifecycle-location.md)
    Watch the ServiceNow Community video: [CSDM V4 product and life cycle discussion](https://www.youtube.com/watch?v=TfRv1VTRsgM)


**Parent Topic:**[Implementing the CSDM framework in stages](csdm-implementation-stages.md)

