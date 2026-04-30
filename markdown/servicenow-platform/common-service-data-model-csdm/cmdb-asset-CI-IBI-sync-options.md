---
title: How life-cycle values for Asset, CI, and IBI are synced
description: Your organization gains significant value from your ServiceNow AI Platform applications when you take advantage of the option to directly map legacy status values to CSDM life cycle stage and life cycle stage status values and auto-sync the values going forward.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# How life-cycle values for Asset, CI, and IBI are synced

Your organization gains significant value from your ServiceNow AI Platform applications when you take advantage of the option to directly map legacy status values to CSDM **life cycle stage** and **life cycle stage status** values and auto-sync the values going forward.

## How Asset, CI, and IBI life-cycle values are synced

Any item that is provided as a service or sold to your customer is tracked as an Install Base Item \(IBI\). The Model category table associates Asset, CI, and IBI for the item.

-   **Sync between asset and IBI**

    By default, the system syncs life-cycle values between asset and IBI using the CSDM **life cycle stage** and **life cycle stage status** life-cycle value pairs.

-   **Sync between asset and CI**

    When the CSDM \(csdm.lifecycle.migration.activated\) plugin is activated on your instance, sync between the asset and CI tables depends on the **csdm.lifecycle.sync.between.ci.and.asset.activated** system property setting:

    -   When the property is set to true, the system syncs the CSDM **life cycle stage** and **life cycle stage status** values directly. This option provides significant benefits to your organization.

        **Important:** The property is set to true when you select **Enable life cycle sync** on the Life cycle mappings list view.

    -   When the property is set to false \(default\), sync occurs through the legacy **status** and **substatus** values.

## Life-cycle sync when the system property is set to false \(the default setting\)

![Sync when the system property is false.](../image/csdm-lifecycle-sync-default.png)

When the CSDM \(csdm.lifecycle.migration.activated\) plugin is activated on your instance and the **csdm.lifecycle.sync.between.ci.and.asset.activated** system property is set to false:

-   **Sync of updates from asset to IBI and CI**

    Updates made to the **status** or **substatus** value of an asset are synced with the associated IBI and CI. For example, when the **State** value of the asset is updated to **In use**, sync happens as follows:

    -   The **life cycle stage** and **life cycle stage status** values of the asset are set to **Operational** and **In use**, these values are then synced with **life cycle stage** and **life cycle stage status** values of IBI asset.
    -   The **status** and **substatus** values of the CI change to **Installed** and **In use**.
-   **Sync of updates from IBI to asset and CI**

    Updates made to the **life cycle stage** and **life cycle stage status** values of an IBI asset are synced with the legacy **status** and **substatus** values of the asset through the CSDM values. The **status** and **substatus** values of the asset are then synced with the associated CI. For example, when the **life cycle stage** and **life cycle stage status** values of an IBI asset are updated to **Defective** and **In Stock**, sync happens as follows.

    1.  The **life cycle stage** and **life cycle stage status** values of the asset change to **In Stock** and **Defective**. These values are synced with the **status** and **substatus** values of the asset.
    2.  The **status** and **substatus** values of the asset are then synced with the associated CI.
-   **Sync of updates from CI to asset and IBI**

    Updates made to the **status** and **substatus** values of a CI are synced with the associated asset. The **status** and **substatus** values of the asset are then synced with the **life cycle stage** and **life cycle stage status** values of the IBI asset through the CSDM values. For example, when the **status** and **substatus** values of a CI are updated to **Retired** and **Donated**, the corresponding values of the asset change. The changes from the asset are synced with the IBI asset and the **life cycle stage** and **life cycle stage status** values change to **End of Life** and **Retired**.


## Life-cycle sync when the system property is set to true

![Sync when the system property is true or you select Enable life cycle sync on the Life cycle mappings list view.](../image/csdm-lifecycle-sync-activated.png)

When the CSDM \(csdm.lifecycle.migration.activated\) plugin is activated on your instance and the **csdm.lifecycle.sync.between.ci.and.asset.activated** system property is set to true \(or you select the select **Enable life cycle sync** on the Life cycle mapping table list page, as described in [Enabling CSDM life-cycle sync between legacy fields and related assets](../../configuration-management/concept/csdm-life-cycle-standard-values.md#)\):

-   **Sync of updates from asset to CI and IBI**

    Updates made to the legacy **status** and **substatus** values of the asset are synced between the asset and CI as follows:

    -   The **life cycle stage** and **life cycle stage status** values of the asset are updated with values mapped to the legacy **status** and **substatus** values of the asset.
    -   The **status** and **substatus** values of the asset are then directly synced with the **status** and **substatus** values of the associated CI.
    -   The **life cycle stage** and **life cycle stage status** values of the asset are then directly synced with the associated CI.
    However, sync of updates from asset to IBI is only through the CSDM life-cycle value pairs.

-   **Sync of updates from IBI to asset and CI**

    Updates made to the **life cycle stage** and **life cycle stage status** values of the IBI are synced as follows:

    -   The legacy **status** and **substatus** values of the asset are synced with the CSDM life-cycle value pairs.
    -   The **status** and **substatus** values of the asset are synced with the **status** and **substatus** values of the associated CI.
    -   The life-cycle value pairs of the asset are directly synced with the associated CI.
-   **Sync of updates from CI to asset and IBI**

    Updates made to the **life cycle stage** and **life cycle stage status** values of a CI are synced as follows:

    -   The **life cycle stage** and **life cycle stage status** values of the CI are directly synced with the associated asset.
    -   The **status** and **substatus** values of the asset are then updated with the values mapped to the CSDM values.
    -   The **status** and **substatus** values of the asset are then synced with the associated CI.
    -   The **status** and **substatus** values of IBI are synced with the asset through the CSDM life-cycle value pairs.

**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

**Related topics**  


[Asset and CI management](https://www.servicenow.com/docs/access?context=c_ManagingAssets&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)

