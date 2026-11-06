---
title: Hardware Model Normalization
description: Hardware Model Normalization standardizes the manufacturer, product, model, and device type, of your hardware and consumable models. The system compares the details on each model against the Hardware Model Normalization Content Service and fills in the standard values it finds.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/hardware-asset-management/hardware-normalization.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [Explore, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Hardware Model Normalization

Hardware Model Normalization standardizes the manufacturer, product, model, and device type, of your hardware and consumable models. The system compares the details on each model against the Hardware Model Normalization Content Service and fills in the standard values it finds.

## Benefits of normalization

Normalization helps you:

-   Use the same manufacturer, product, and model names across assets and reports.
-   View manufacturer lifecycle phases on a model: Availability, End of sale, End of support, End of extended support, and End of life.
-   See consistent display names for models and for the assets that use them.

**Note:** Normalization doesn't add, remove, or merge models. It also doesn’t change the Name, Manufacturer, or Model number that you entered. If two models normalize to the same standard model, both records remain.

For more details, see [Normalize hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md).

## How normalization works

The system searches the Content Service for the combination of Manufacturer, Name, and Model number from your model. If the Content Service finds a match, the system fills the normalized fields on your model and sets the normalization status. The status depends on how many normalized fields the system fills. The system matches the three values as one combination and doesn’t compare them field by field.

Normalization requires the model number of the device. You can enter the model number in the **Name** field or the **Model number** field.

-   **How model normalization starts**

    Normalization starts when:

    -   You create a model, or you change its Manufacturer, Name, or Model number.
    -   You select **Normalize** on a model. This option isn't available for models that are Normalized or Manually Normalized.
    -   The HAM - Hardware Normalization job runs. It runs daily.
    **Note:** Normalization runs only for models whose resource categories are opted in.

-   **When new content arrives**

    Content Service data is published weekly. Each instance downloads the new data on a day that varies by instance, so new data can take up to a week to reach your instance. The next daily run of the **HAM - Hardware Normalization** job then applies it. This is why a model might not show new normalized values right away.

-   **Which models are normalized**

    Normalization applies to hardware and consumable models. A model qualifies only when its model category is associated with a HAM resource category that you opted in to. If you haven’t opted in to the resource category, normalization doesn’t run, and the model stays in the **New** status. For opt-in details, see [Opt-in or opt-out of HAM license resource categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/optin-optout-ham-license-resource-categories.md).

    By default, normalization runs only for models that belong to leaf domains, which are domains that have no child domains.

    **Note:**

    By default, HAM workflows exclude hardware models whose model category is associated with an opted-out HAM resource category. These models don’t go through normalization. An exception applies when the OT Asset Management application is activated on your instance. In that case, such a model is also normalized if it has at least one Operational Technology \(OT\) asset. The OT asset can have any install status except Retired or Missing. The **OT entity** flag on an asset shows whether it’s an OT asset.

    Normalization doesn’t run for retired or missing OT assets. For more information, see [OT Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/enterprise-asset-management/ot-asset-ws-otam.md).


## Normalization status

Each hardware and consumable model has one of these statuses. The status shows how much standard information the system filled in from the Content Service.

<table id="table_ymg_t3q_clc"><thead><tr><th>

Status

</th><th>

Description

</th><th>

What to do next

</th></tr></thead><tbody><tr><td>

**New**

</td><td>

The model hasn't been processed yet. A model also stays **New** when its resource category isn't opted in to HAM.

</td><td>

Wait for the next daily run of the HAM - Hardware Normalization job, or select **Normalize** on the model to start normalization immediately. If the status stays New, confirm that the resource category of the model is opted in.

</td></tr><tr><td>

**Normalized**

</td><td>

The Content Service matches the combination of Manufacturer, Name, and Model number on the model. The system fills the normalized Manufacturer, Product, Device type, and Model fields.

</td><td>

No action needed.

</td></tr><tr><td>

**Partially Normalized**

</td><td>

The Content Service fills the normalized Manufacturer, Product, and Device type fields but doesn’t fill the normalized Model field.

</td><td>

Review the Name and Model number fields for errors or missing values. Then select **Normalize** on the model to run normalization again.

</td></tr><tr><td>

**Manufacturer Normalized**

</td><td>

The system uses the manufacturer mapping in the Content Service to fill the normalized Manufacturer field. It doesn’t fill the other normalized fields.

</td><td>

Review the model details, Then select **Normalize** on the model to run normalization again.

</td></tr><tr><td>

**Match Not Found**

</td><td>

The Content Service has no match. This typically occurs for:-   Custom or proprietary hardware
-   New hardware that isn’t in the Content Service data yet
-   Legacy hardware

</td><td>

Enter the normalized Manufacturer, Product, and Model values manually. After you save, the status changes to Manually Normalized.

</td></tr><tr><td>

**Manually Normalized**

</td><td>

You edit any of the normalized fields, such as Manufacturer, Product, Device type, or Model.

</td><td>

No action is required. The system keeps your values, and you can’t revert a Manually Normalized model to its previous status.

</td></tr></tbody>
</table>## What happens after normalization

Fields that normalization updates:

-   Normalized manufacturer: Shows the manufacturer that the system fills from the Content Service during normalization, or the value you enter manually.
-   Normalized product: Shows the hardware product that the system fills from the Content Service during normalization, or the value you enter manually.
-   Normalized model: Shows the model that the system fills from the Content Service during normalization, or the value you enter manually.
-   Normalized device type: Shows the device type that the system fills from the Content Service during normalization, or the value you enter manually.
-   Normalization status: Shows the normalization state of the model, such as New, Normalized, or Manually Normalized.
-   Normalization status summary: Indicates whether the model is normalized or not normalized.
-   Display name: Shows the normalized Manufacturer and the normalized Model combined, for a model that has a normalized model.

-   **Other results**
    -   Asset display names: The display name of an asset includes the display name of its model. After normalization, the system recalculates the display names of the assets that use the model.

        The system recalculates asset display names only when the**sn\_hamp.update\_assets\_norm\_model\_name** system property is set to **true**. The default is true for new HAM installations and false for upgraded instances. On upgraded instances, asset display names don’t update after normalization until you set the property to true. To change the property, see Administrator settings.

    -   Lifecycle records: The system adds lifecycle records from the Content Service to models that have a normalized model. Other models have no lifecycle records from the Content Service.
    -   Reports: Normalization reports in the Hardware Asset Workspace show the results.

## Lifecycle records for normalized models

-   When the system adds lifecycle records: Manufacturers publish lifecycle dates for specific models, not for whole product lines. When your hardware or consumable model matches a specific model in the Content Service, the system copies the lifecycle records to your model automatically. This applies to models with the status Normalized, or Manually Normalized with a normalized model. A model that matches no specific model, such as a Partially Normalized or Manufacturer Normalized model, doesn’t get lifecycle records.
-   Where the information comes from: ServiceNow maintains a library of lifecycle definitions for manufacturer models. Each definition gives the dates for one phase: Availability, End of sale, End of support, End of extended support, or End of life. When a model matches, the system copies the active definitions for the matching content model to your model as lifecycle records. The Source field on each record shows ServiceNow.
-   Approximated lifecycles: If a manufacturer doesn’t publish lifecycle dates for a model, the Content Service can include approximated lifecycle records instead. These records are tagged as approximated. The **sn\_hamp.approximate\_dates\_in\_hw\_lifecycle** system property controls whether the system uses them.
-   Reverting normalization: If a model no longer matches the Content Service, for example after you revert normalization, the system deactivates the lifecycle records it added from that match. It doesn’t delete them. If the model later matches a different content rule, the system adds lifecycle records for the new match.
-   Opted-out models: When you opt out a resource category, the system deactivates the Content Service lifecycle records for its models and reverts their normalization.
-   Determining the current phase: A model can have several lifecycle records. The Calculate active lifecycle phase for models step of the HAM - Daily Job marks one record as current:
    1.  The system considers only active records whose start and end dates include today. If more than one record qualifies, the record with the latest start date is current.
    2.  If records share the same start date, the system compares their phases. The default order is Availability, End of sale, End of support, End of extended support, and End of life. Administrators can change the order with the **sn\_hamp.model\_lifecycle\_phase\_order** system property.
    3.  If records still tie, the system compares their sources in this order: internal, ServiceNow, calculated, and other.

-   **Keeping lifecycle records in sync**

    The system keeps lifecycle records current after normalization, so models that were normalized earlier still receive updated lifecycle records. Three scheduled tasks do this:

    1.  The weekly Download Hardware Content schedules download lifecycle content from the Content Service.
    2.  The weekly HAM - Hardware Lifecycles job applies the changed lifecycle content to models.
    3.  The daily HAM - Daily Job recalculates the current phase of each model.

## Normalization reports

The Hardware Asset Workspace includes these reports for model normalization:

-   Normalization Metrics: The number of normalized and not normalized models. This report is available in the Model management view of the Hardware Asset Workspace.
-   Model Normalization Scorecard: The percentage of models that are normalized. This report is available n the Hardware asset overview of the Hardware Asset Workspace.

## Actions you can take

-   **Normalize manually**

    Normalization runs automatically in most cases. You can also normalize a model yourself in these situations:

    -   To complete a Partially Normalized model.
    -   To add values for custom or proprietary hardware that the Content Service doesn’t include.
    -   To correct values that the system filled in.
    When you edit the normalized fields, the status changes to Manually Normalized. For the steps, see [Normalize hardware and consumable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/normalize-hardware-consumable-models.md).

-   **Revert normalization**

    Revert normalization to undo the normalization of a Normalized, Partially Normalized, or Manufacturer Normalized model. You can’t revert a **Manually Normalized** model. When you revert a model:

    -   The system clears the normalized fields and changes the status to **Match Not Found**.
    -   For a Normalized or Partially Normalized model, the system deactivates the content rule that normalized it. The system also reverts the other models that the rule normalized, except Manually Normalized models.
    -   The system doesn’t normalize the model again immediately. The next daily run of the normalization job processes it, or you can select **Normalize** on the model. A different active rule can then normalize the model.

## Administrator settings

**Note:** This section is for administrators and implementers.

-   **Domain configuration**

    By default, normalization runs only for models in the leaf domains. If you have the asset and domain\_admin role, you can enable normalization for hardware models in any domain.

    1.  Navigate to the Domain Asset Process Settings \[alm\_domain\_asset\_process\_setting\] table.
    2.  Find the domain for which you want to enable normalization of models.
    3.  Set the Run asset process field to true.
    The next time the scheduled job runs, it normalizes the hardware models of that domain.


**Parent Topic:**[Exploring Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/exploring-ham.md)

**Related topics**  


[Configure Hardware Model Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/Work-with-hardware-normalization.md)

