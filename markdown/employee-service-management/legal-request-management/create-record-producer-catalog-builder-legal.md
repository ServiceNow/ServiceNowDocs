---
title: Create or modify a record producer for legal services through Catalog Builder
description: Create or modify a record producer using a catalog template to define an intake form for a legal service. Employees can use these intake forms on the Legal Service Portal to submit a legal request or legal matter.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing record producers for legal services, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create or modify a record producer for legal services through Catalog Builder

Create or modify a record producer using a catalog template to define an intake form for a legal service. Employees can use these intake forms on the Legal Service Portal to submit a legal request or legal matter.

## Before you begin

Role required: sn\_lg\_ops.request\_config or sn\_lg\_matter.matter\_config

## About this task

Use the following base system catalog item templates installed with Legal Request Management to create a record producer for legal services:

-   Legal request intake form template: For creating a record producer for legal requests
-   Legal matter intake form template: For creating a record producer for legal matters

For more information about catalog item templates and catalog items, see [Catalog Builder](https://www.servicenow.com/docs/access?context=catalog-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Open Catalog Builder from the application navigator or from an intake form.

<table id="choicetable_umx_jtg_cvb"><thead><tr><th align="left" id="d577329e97">

Option

</th><th align="left" id="d577329e100">

Steps

</th></tr></thead><tbody><tr><td id="d577329e106">

**From an Intake form**

</td><td>

1.  [Open an intake form](associate-categories-practice-area.md) that has a record producer selected.
2.  Click the **Edit in Catalog Builder** related link.


</td></tr><tr><td id="d577329e133">

**From the application navigator**

</td><td>

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Builder**.
2.  Create or modify a record producer.
    -   To create a record producer, on the **Dashboard** tab, click **Create a new catalog item**.
    -   To modify an existing record producer, click the **Catalog items** tab and open the record producer from the list.
3.  Review the steps involved in the creation process and click **Continue**.
4.  Select a template from the list, review the template preview, and click **Use this item template**.


</td></tr></tbody>
</table>2.  Based on how each step is defined in the template, specify the required information.

    For more information, see [Create a catalog item using a template](https://www.servicenow.com/docs/access?context=create-item-cat-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    In addition to entering other details, make sure to provide the following information for a record producer for a legal service:

<table id="table_u4m_hvg_cvb"><thead><tr><th>

Step

</th><th>

Field and default values from the template

</th></tr></thead><tbody><tr><td>

Destination

</td><td>

**Table**: -   For legal requests: Default is **Legal Request \[sn\_lg\_ops\_request\]**.

You can select a [practice area table for legal requests](../reference/legal-request-pa-tables.md) as required.

-   For legal matters: Default is **Legal Matter \[sn\_lg\_matter\_matter\]**.

You can select a [practice area table for legal matters](../../legal-matter-management/reference/legal-matter-pa-tables.md) as required.

</td></tr><tr><td>

Location

</td><td>

-   **Catalogs**: Default is **Legal Operations Catalog**.
-   **Categories**: Legal Request for legal requests and Legal Matter for legal matters.

You can select a different catalog and [category](add-catalog-categories.md) based on your requirements.

</td></tr><tr><td>

Access

</td><td>

-   **Available for**:

    -   For legal requests: Default is **Users with legal\_user role**.
    -   For legal matters: Default is **Legal Matter Catalog**.
Select users with specific roles who are granted access to the record producer.

-   **Not available for**: Select users with specific roles who are denied access to the record producer.
 **Note:** If you don’t specify a user criteria in any option, access is granted to everyone.

 For more information on creating a user criteria, see [Set up the user criteria](https://www.servicenow.com/docs/access?context=t_CreateAUserCriteriaRecord&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>3.  To save your changes in each step, click **Save**.

    All edits to the item attributes are automatically saved when you navigate to the next step.

4.  To preview the record producer, click **Preview**.

5.  In the **Review and Submit** step, review the record producer and click **Submit** to publish the record producer in the selected catalog.


**Parent Topic:**[Managing record producers for legal services](../concept/record-producers-legal-services.md)

