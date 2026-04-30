---
title: Hardware Model Normalization
description: Asset Management Hardware Model Normalization enables you to normalize the details, such as manufacturer, product, model, and device type, of your hardware and consumable models. Data from the models is compared against the data in the Hardware Model Normalization Content Service.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Hardware Model Normalization

Asset Management Hardware Model Normalization enables you to normalize the details, such as manufacturer, product, model, and device type, of your hardware and consumable models. Data from the models is compared against the data in the Hardware Model Normalization Content Service.

The Hardware Model Normalization \(com.sn\_hwnorm\) plugin is activated when you activate the Hardware Asset Management \[sn\_hamp\] plugin.

For more information about the process of normalizing hardware and consumable models, see [Normalize hardware and consumable models](../task/normalize-hardware-consumable-models.md).

**Note:** This documentation is for Hardware Model Normalization. For additional information on Asset Management, see the [Asset Management documentation](https://www.servicenow.com/docs/access?context=c_AssetManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

## Scheduled jobs

To standardize your hardware and consumable models, the asset data must be normalized. You can manually update the model records with the normalization content, or you can compare your data against the Hardware Asset Management Content Service.

The **HAM- Hardware Normalization** scheduled job runs daily. This job doesn’t add, remove, or merge models, nor does it modify the original fields like Model Name, Manufacturer, or Model Number. It only updates the normalization-related fields for existing models, such as Normalized Product, Normalized Manufacturer, Normalized Model, and so on.

Content from the Hardware Model Normalization Content Service is pulled into the ServiceNow AI Platform. Use the Asset Job Log \(asset\_job\_log\) table to review the status of the scheduled job.

The normalization status of models can be reverted by selecting **Revert Normalization** on the model. Any normalization that occurred on the model gets reverted and the rule gets deactivated. When the scheduled job runs, the models are processed with the active rules and the status is updated. For more information about reverting normalization, see [Revert normalization of hardware and consumable models](../task/revert-norm-ham.md).

**Note:** The Domain Asset Process Settings table \(alm\_domain\_asset\_process\_setting\) stores configurations for asset processes, including the normalization of hardware models. By default, normalization is performed only for models within the TOP/Default domain. However, if you have the asset or domain\_admin role, you can enable normalization for hardware models in any domain. To enable normalization for a specific domain, follow these steps:

1.  Navigate to the Domain Asset Process Settings table \(alm\_domain\_asset\_process\_setting\).
2.  Locate the specific domain for which you want to enable normalization of models.
3.  Set the **Run asset process** field to **true**.

When the scheduled job runs the next time, the hardware models of that domain are normalized.

**Important:** By default, hardware models that belong to a model category associated with an opted-out HAM resource category are excluded from HAM workflows. Therefore, such hardware models don’t go through Hardware Model Normalization. However, when the OT Asset Management application is activated on your ServiceNow instance, any hardware model of an opted-out HAM resource category with a minimum of one Operational Technology \(OT\) asset also goes through Hardware Model Normalization. The **OT entity** flag on the asset indicates whether it's an OT asset. For more information on OT assets, see [OT Asset Workspace](../../enterprise-asset-management/concept/ot-asset-ws-otam.md).

You can also revert the normalization status of the hardware models with OT assets.

The scheduled job generates hardware and consumable model reports. These reports identify the overall status of your models and provide a breakdown of the normalization status.

The following reports are included.

-   Hardware Product Overall Normalization Status
-   Consumable Product Overall Normalization Status
-   Hardware Model Normalization Status
-   Consumable Model Normalization Status

**Related topics**  


[Work with hardware normalization](Work-with-hardware-normalization.md)

