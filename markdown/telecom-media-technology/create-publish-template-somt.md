---
title: Create and publish a template
description: Create and publish a template so that you can define the 5G network services for your organization.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-16"
reading_time_minutes: 2
breadcrumb: [Retiring or archiving versioned specifications and product offerings, Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Create and publish a template

Create and publish a template so that you can define the 5G network services for your organization.

## Before you begin

Role required:

-   sn\_prd\_pm.product\_catalog\_admin
-   sn\_prd\_pm.product\_catalog\_manager \(Read-only access\)

## Procedure

1.  Open CSM Configurable Workspace.

2.  Navigate to **List** &gt; **Templates** &gt; **All**.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_lm4_zxw_lxb"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated number of the template.

</td></tr><tr><td>

Name

</td><td>

Name of the template.

</td></tr><tr><td>

Description

</td><td>

Description of the template.

</td></tr><tr><td>

State

</td><td>

State of the template.-   **Draft**

The template is created, but not yet published in the catalog to be used in the product or service specifications.

-   **Published**

The template is published in the catalog and in use in the product or service specifications.

-   **Retired**

The template is retired and you can't make any changes to the retired template.

-   **Archived**

The template is archived. You can archive only a retired template.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  Navigate to the **Template Characteristics** tab, select **New**, and fill in the fields on the form.

    |Fields|Descriptions|
    |------|------------|
    |Number|Number of the automatically filled-in template.|
    |Characteristic|Characteristic of the network service that you're defining.|
    |Template|Template name that is automatically selected.|
    |Mandatory|Mandatory characteristics that are confirmed by the system when this option is selected.|

7.  Select **Save**.

8.  Select the **Template Characteristic Options** tab, select **New**, and fill in the fields on the form.

    |Fields|Descriptions|
    |------|------------|
    |Number|Number of the automatically filled-in template characteristic.|
    |Template characteristic|Template characteristic that you have defined.|
    |Characteristic option|List of the characteristic options defined in the Template Characteristic table.|

9.  Publish, save, or copy the draft template.

<table id="choicetable_q3p_bpt_txb"><thead><tr><th align="left" id="d22023e380">

Action

</th><th align="left" id="d22023e383">

Description

</th></tr></thead><tbody><tr><td id="d22023e389">

**Publish**

</td><td>

Publish the draft template so that you can use it in a service specification.**Note:**

A dialog box appears with the following message: Changes to templates are not allowed once published. Are you sure you want to publish?

Do one of the following actions:

-   To skip publishing this template, select **Cancel**.
-   To publish this template, select **OK**.
When you publish it, its state changes from Draft to Published.

</td></tr><tr><td id="d22023e418">

**Save**

</td><td>

Update the template with the new data that you added.

</td></tr><tr><td id="d22023e429">

**Copy**

</td><td>

Copy the data in this template so that you can create a template from it.

</td></tr></tbody>
</table>
## What to do next

Create and publish the service specifications and associate them with the templates. For more information, see [Create and publish service specifications](create-service-specification.md).

