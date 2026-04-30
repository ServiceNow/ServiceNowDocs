---
title: CSDM life-cycle terms
description: Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [CSDM reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CSDM life-cycle terms

Most ServiceNow products and ServiceNow AI Platform applications align closely with the Common Service Data Model. This table defines terms as they are used across the ServiceNow AI Platform.

## Life cycle mapping table

The base system includes the life cycle mapping \[life\_cycle\_mapping\] table. The table is pre-populated with mappings between widely used legacy status values and the equivalent CSDM *life cycle stage* and *life cycle stage status* values. Each record in the table \(called a mapping rule\) specifies how to map a legacy status value, based on its table, to the best-fit CSDM life-cycle value pair.

The table typically contains multiple record entries per class, each entry that maps a specific legacy status to a life-cycle value pair. When there are multiple record entries for a class, the entries are prioritized by importance and likelihood for containing meaningful values for the mapping process. The highest priority rule is used when multiple candidate rules apply.

![Mapping rule that specifies the mapping between a legacy status value and the equivalent CSDM life cycle stage and life cycle stage status values.](../../csdm-implementation/image/csdm-lifecycle-mapping-form-annota.png)

See [Map legacy status values to CSDM life-cycle values](../concept/csdm-life-cycle-standard-values.md#) and [How life-cycle values for Asset, CI, and IBI are synced](../../csdm-implementation/reference/cmdb-asset-CI-IBI-sync-options.md).

## Terms related to life cycle

-   **CI**

    Configuration item: Record in the CMDB CI \[cmdb\_ci\] table.

-   **life-cycle value pair**

    A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. The pair of values fully describe the life-cycle state of the product instance.

    The standard CSDM life-cycle value pair covers all phases of a product instance life cycle.

    -   A **life cycle stage** is one of the broad phases that a CI moves through, from inception or procurement to retirement and end of life.
    -   **life cycle stage status** is the particular status of a CI within its current life cycle stage.
    For example, a hardware CI in the **Operational** stage might change status over time from **In Use** to **In Maintenance** to **End of Support**. A different hardware CI might go from **In Use** to **End of Support** without ever having been in **In Maintenance** status.

    ![Allowed life-cycle values during the Operational stage of a hardware CI's life cycle](../../csdm-implementation/image/csdm-op-stage-of-hw-ci.png)

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

**Parent Topic:**[CSDM reference](../../csdm-implementation/concept/csdm-content-frame-reference.md)

