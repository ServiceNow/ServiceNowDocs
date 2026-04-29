---
title: Create interoperability mappings between assets and models
description: Create interoperability mappings between assets and models so that you can define their operational relationships at a granular level.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Expanded Model and Asset Classes, Enterprise Asset Management, IT Asset Management]
---

# Create interoperability mappings between assets and models

Create interoperability mappings between assets and models so that you can define their operational relationships at a granular level.

## Before you begin

Role required: admin

## About this task

**Important:** You can currently create interoperability mappings for industrial assets only.

## Procedure

1.  On the page header of your ServiceNow instance, select **All**.

2.  In the menu navigation filter, enter `cmdb_asset_ci_model_interoperability_configuration_list.do`.

    The Asset CI Model Interoperability Configuration \[cmdb\_asset\_ci\_model\_interoperability\_configuration\] table opens.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_opf_wd2_h3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Functional Location

</td><td>

Functional location, such as a test site, that the interoperability mapping applies to.

</td></tr><tr><td>

Configuration Item

</td><td>

Configuration item \(CI\) of the asset that you want to map to the specified model.**Note:** If you fill in this field, you do not need to fill in the **Asset** field. After you create the interoperability mapping, the **Asset** field automatically populates with the corresponding asset.

</td></tr><tr><td>

Interoperability Type

</td><td>

Operational relationship between the specified asset and model. Select one of the following options:-   **Compatible With::Compatible With**: Indicates that the specified asset and model are compatible with each other.
-   **Transforms::Transformed By**: Indicates that the specified asset can transform any asset under the specified model.
-   **Produces::Produced By**: Indicates that the specified asset can produce an asset under the specified model.
-   **Uses::Used By**: Indicates that the specified asset can use any asset under the specified model.
**Note:** If a desired interoperability type is not available, you can create a new interoperability type.

</td></tr><tr><td>

Asset

</td><td>

Asset that you want to map to the specified model.**Note:** If you fill in this field, you do not need to fill in the **Configuration Item** field. After you create the interoperability mapping, the **Configuration Item** field automatically populates with the corresponding CI.

</td></tr><tr><td>

Interoperable Model 2

</td><td>

Model that you want to map to the specified asset.

</td></tr><tr><td colspan="2">

Details

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the interoperability mapping is active.

</td></tr><tr><td>

Effective From

</td><td>

Date on which the interoperability mapping becomes effective.

</td></tr><tr><td>

Effective To

</td><td>

Date on which the interoperability mapping is no longer effective.

</td></tr></tbody>
</table>5.  Select **Submit**.


