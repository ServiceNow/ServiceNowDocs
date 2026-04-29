---
title: CSDM life-cycle terms
description: Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM life-cycle terms

Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.

## Terms related to life cycle

-   **CI**

    Configuration item: Record in the CMDB CI \[cmdb\_ci\] table.

-   **life-cycle value pair**

    A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. The pair of values fully describe the life-cycle state of the product instance.

    The standard CSDM life-cycle value pair covers all phases of a product instance life cycle.

    -   A **life cycle stage** is one of the broad phases that a CI moves through, for example from inception or procurement to operation and then perhaps to end of life.
    -   **life cycle stage status** is the particular status of a CI within its current life cycle stage.
    For example, a tangible/physical CI in the **Operational** stage might change stage status over time from **In Use** to **In Maintenance** to **End of Support**. A different tangible/physical CI might go from **In Use** to **End of Support** without ever having been in **In Maintenance** status.

    ![Allowed life-cycle values during the Operational stage of a tangible/physical CI life cycle](../../csdm-implementation/image/csdm-op-stage-of-hw-ci.png)

-   **CI legacy values**

    Value types that were in place before CSDM life-cycle values were implemented:

    -   install status
    -   operational status
    -   hardware status
    -   hardware substatus
-   **asset**

    Production asset: Record in the asset \[alm\_asset\] table.

-   **install base item \(IBI\)**

    Install-Base-Item: Record in the install base item \[sn\_install\_base\_item\] table. Any item that is provided as a service or sold to your customer is tracked as an Install Base Item \(IBI\). The Model category table associates Asset, CI, and IBI for the item.

-   **product instance**

    A product instance \(PI\) is comprised of an operational asset \(asset\), an install-base-item \(IBI\), and a configuration item \(CI\). A PI is a logical grouping of the \[Asset/CI/IBI\] that represents instances of products \(goods and services\) throughout their life cycles in ServiceNow applications and workflows. Possible formulations:

    -   Asset+CI+IBI
    -   Asset+CI
    -   Asset+IBI

## Life cycle mapping table

The base system includes the life cycle mapping \[life\_cycle\_mapping\] table. The table is prepopulated with mappings between widely used legacy status values and the equivalent CSDM *life cycle stage* and *life cycle stage status* values. Each record in the table \(called a mapping rule\) specifies how to map a legacy status value, based on its table, to the best-fit CSDM life-cycle value pair.

The table typically contains multiple record entries per class, each entry that maps a specific legacy status to a life-cycle value pair. When there are multiple record entries for a class, the entries are prioritized by importance and likelihood for containing meaningful values for the mapping process. The highest priority rule is used when multiple candidate rules apply.

![Mapping rule that specifies the mapping between a legacy status value and the equivalent CSDM life cycle stage and life cycle stage status values.](../../csdm-implementation/image/csdm-lifecycle-mapping-form-annota.png)

See [Map legacy status values to CSDM life-cycle values](../concept/csdm-life-cycle-standard-values.md#) and [How life-cycle values for Asset, CI, and IBI are synchronized](../../csdm-implementation/reference/cmdb-asset-CI-IBI-sync-options.md).

## Life Cycle Stage inheritance for Business Application records

Business Application records define a restricted set of Life Cycle Stage values that are intended to reflect application planning and usage, such as Ideation, Design, Operational, and End of Life. These life cycle definitions are configured using the life\_cycle\_control table specifically for the cmdb\_ci\_business\_application class. When you view or edit a Business Application record, however, additional Life Cycle Stage values such as Deploy and Inventory might also appear. These stages are not defined directly for Business Application, but are inherited from parent CI classes \(for example, cmdb\_ci\) through the aggregation-based inheritance model that is used by life\_cycle\_control. In this model, life cycle definitions from the current CI class are combined with life cycle definitions from all parent classes in the CMDB class hierarchy. Child classes therefore extend parent life cycle definitions rather than overriding them. As a result, Business Application records can display Life Cycle Stage values that are applicable to infrastructure or hardware CIs but might not be semantically meaningful for applications. This behavior is expected and working as designed.

In contrast, in sys\_choice inheritance definitions in child tables override the values in parent tables.

**Parent Topic:**[CSDM reference](../../csdm-implementation/concept/csdm-content-frame-reference.md)

