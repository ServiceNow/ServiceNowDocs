---
title: Set up Entity Based Access properties
description: Enable or disable the Entity Based Access properties to control access to the objects that are associated with an entity.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Set up Entity Based Access properties

Enable or disable the Entity Based Access properties to control access to the objects that are associated with an entity.

## Before you begin

Role required: sn\_grc\_ent\_access.admin

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Properties**.

    The properties in the following table are displayed.

    |Property|Options|Description|
    |--------|-------|-----------|
    |Entity-based access on record types related to entity \[sn\_grc\_ent\_access.enable\_entity\_based\_accesss\]|Enable|Option for Entity Based Access. By default, entity-based access is turned off. Entity-based access administrators are responsible for activating these properties for users.|
    |Enable data filters on record types consuming entity-based access \[sn\_grc\_ent\_access.enable\_datafilters\_for\_eba\]|Yes or No|Option for enabling data filters on record types. By default, entity-based access is Yes. Enabling this property filters the records based on the entity-based access configuration.|

2.  Select **Save**.

    Based on your selected settings, the entity-based access properties are configured in your system.

3.  Navigate to the record that you want to set up entity-based access for.

4.  On the **Access settings** tab, select **Entity based access restriction**.

    The **Entity based access restriction** field is available only on the Issue form. For all other records, you must configure a bulk access update to enable an entity-based access restriction.

    ![Access settings for entity-based access restriction on the Issue form.](../image/eba-issue-form.png)


## Result

You have completed configuring entity-based access properties in your system.

**Parent Topic:**[Configuring Entity Based Access](../concept/setting-up-entity-based-access.md)

