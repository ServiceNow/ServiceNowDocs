---
title: Product Instance feature in Hardware Asset Management
description: You can consistently represent a product along all applications, processes, workflows, and user interactions through the Product Instance feature. Changes made to any of the product representations are synchronized automatically.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Product Instance feature in Hardware Asset Management

You can consistently represent a product along all applications, processes, workflows, and user interactions through the Product Instance feature. Changes made to any of the product representations are synchronized automatically.

The Product Instance feature enables you to have a common representation for any product tracked as an asset in IT Asset Management, an install base item \(IBI\) in Customer Service Management \(CSM\), and a configuration item in Configuration Management Database \(CMDB\). A Product Instance is associated with assets of a particular model category.

**Note:** Product Instance is currently enabled only for the Medical device model category.

## Product Instance Identifier \(PID\) configurations for a model category

Product Instance Identifier \(PID\) is a unique identifier for a Product Instance and links asset, CI, and IBI.

A PID is generated based on the following items defined in the Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table:

-   PID configurations
-   Order assigned to each configuration

**Note:** PID configurations out-of-the-box can't be edited and are read-only.

Note the following about PID generation:

-   If the fields specified in the parameters of PID configurations are empty, a PID isn't generated and the asset isn't created.
-   Assets that are in the On order or Pre-allocated state and don't have a serial number won’t have a PID generated.
-   The PID is recalculated and regenerated whenever changes are made to the fields specified in the PID configuration parameters, for example, updates to the serial number of an asset, CI, or IBI.

**Note:** The PID is stored in the product\_instance\_id field of the Asset \[alm\_asset\], Configuration Item \[cmdb\_CI\], and Install Base Item \[sn\_install\_base\_item\] table.

For the medical device model category, the default parameters of a PID configuration are based on the **Serial number**, **Parent**, and **Model Component ID** fields of the table. The PID configuration based on the item's serial number is given the highest priority when generating a PID. But when the serial number isn’t present, the parameters based on the Parent and Model Component ID fields are considered for generating the PID. If you specify an existing serial number, the PID that is generated would be a duplicate of an existing PID, so the asset isn’t created. If you have any customizations, such as using a different custom field instead of the Serial Number as a unique identifier, you should deactivate the Serial Number PID configuration and create a new PID configuration for that custom field.

**Note:** To enable PID recalculation for child assets when updates are made to the parent asset, set the system property **sn\_itam\_enable\_pid\_recalculation\_for\_child\_asset** to true. The default value is false.

## PID synchronization between an asset, CI, and IBI

Synchronization of PID between an asset, CI, and IBI happens in the following circumstances:

-   Any of the fields of the PID is updated on an asset, CI, or IBI
-   An asset, CI, or IBI is with values specified in the fields of the PID configuration parameters.

-   **Create or update assets**

    When you create an asset by specifying a value for a field included in the PID configuration parameter, based on the PID configuration of the associated model category, the following actions occur:

    1.  A PID is generated for the asset based on the field value that you specified.
    2.  The asset is created.
    3.  The PID of the asset is synchronized with the associated CI.
    When you update the field included in the PID configuration parameter of an asset, the PID is recalculated and regenerated based on the new field value. The updated PID of the asset is then synchronized with its associated CI.

-   **Create or update a CI**

    When you create a CI, a PID is generated only when the asset is created for that CI. The PID of the asset is then synchronized with the CI.

    When you update a field included in the PID configuration parameter on a CI, the following actions occur:

    1.  The field value is copied from CI to the asset.
    2.  The PID is recalculated and regenerated for the asset.
    3.  The PID of the asset is synchronized with the associated CI.
-   **Create or update an IBI**

    When you create an IBI by specifying a field included in the PID configuration parameter, an asset and the associated CI are created. The PID is generated on the install base item and is synchronized with the asset and its associated CI.

    A PID is regenerated and synchronized when any updates are made to the fields of the IBI that are part of the PID configuration parameters.


