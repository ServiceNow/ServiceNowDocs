---
title: Create a Software Asset Management Foundation plugin software model in classic
description: Software models are used to connect purchased software rights with discovered software installations. Additionally, software models can be used to manage suites of software as well as to publish requestable software to the Service Catalog.
locale: en-US
release: yokohama
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Configuring Software Asset Management Foundation plugin classic, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create a Software Asset Management Foundation plugin software model in classic

Software models are used to connect purchased software rights with discovered software installations. Additionally, software models can be used to manage suites of software as well as to publish requestable software to the Service Catalog.

## Before you begin

Role required: sam\_user or model\_manager

## About this task

Manage software available and tie software installations \(software being used\) with entitlements \(software owned\) using software models. Create software models for all software to be monitored.

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but cannot administer all aspects of software models.

Predefined suites are used so suite components are automatically created for known suite parent software models. Discovery maps indicate whether a suite is defined for the product.

You can also track a software model lifecycle phase for use with the [Technology Portfolio Management](https://www.servicenow.com/docs/access?context=technology-portfolio-management&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

## Procedure

1.  Navigate to **Software Asset** &gt; **Licensing** &gt; **Software Models** and create a new record \(see table for field descriptions\).

<table id="table_nr2_nd1_y4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

\[Read-only\] Name of the model. The system property **glide.cmdb\_model.display\_name.shorten** controls how software model display names are generated. System administrators can configure this property. Default format is publisher + product + version + edition.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software. You can use the lookup list provided.**Note:** Publisher is a reference to the company \[core\_company\]. Only companies you are using internally are shown.

 If the publisher and product do not exist, you can [Add a Software Asset Management Foundation plugin custom license metric](add-custom-license-metric-samf.md).

</td></tr><tr><td>

Product

</td><td>

Software product name. The same lookup list provided on the Software Discovery Models form.**Note:** If the relationship between the software publisher \[samp\_sw\_publisher\] and company \[core\_company\] is not correct, products for that publisher may not be shown.

</td></tr><tr><td>

Product classification

</td><td>

The official UNSPSC classification of the product.

</td></tr><tr><td>

Product type

</td><td>

-   Child: A subcomponent of main software \(not licensable\).
-   Driver: A software product that controls a device.
-   Licensable: A software product that is licensable.
-   Not Licensable: A software product that is not licensable.
-   Patch: A software product designed to update, fix, or improve an existing computer program.
-   Unknown: Not discovered.


</td></tr><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Short description

</td><td>

A brief description of the model.

</td></tr><tr><td>

Cost

</td><td>

The cost of a single unit of the software.

</td></tr><tr><td>

Next version

</td><td>

Reference to another software model of the same manufacturer which represents the next version of the product.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

</td></tr><tr><td>

Status

</td><td>

The current status of the model. Options are **In Production**, **Retired**, and **Sold**.

</td></tr><tr><td>

Certified

</td><td>

Check box for indicating the software model has been approved for use.

</td></tr><tr><td class="sub-head" colspan="2">

Discovery Mapping

</td></tr><tr><td>

Version condition

</td><td>

Condition qualifier for the **Version** field.-   starts with
-   is
-   is anything
 Default is **is anything**.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.Required if version condition value is **starts with** or **is**.

</td></tr><tr><td>

Edition condition

</td><td>

Condition qualifier for the **Edition** field.-   starts with
-   is
-   is anything
 Default is **is anything**.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software product to use when searching for the normalized discovery model.Required if edition condition value is **starts with** or **is**.

</td></tr><tr><td>

Platform

</td><td>

Platform of the software product to use when searching for the normalized discovery model.Default is **--Anything--** for Windows, Mac, Unix.

</td></tr><tr><td>

Language

</td><td>

Language of the software product to use when searching for the normalized discovery model, which is populated once it has been normalized or added manually.Default is **--Anything--**.

</td></tr><tr><td>

Software installation condition

</td><td>

Only software installations that meet this software discovery map condition are counted during reconciliation.If needed, specify a subset of software installations that should be counted during reconciliation.

</td></tr><tr><td class="sub-head" colspan="2">

Product Catalog

</td></tr><tr><td>

Catalog Item

</td><td>

The information about the model as it appears in the product catalog and service catalog. Information only appears if the model has been published to the product catalog.

</td></tr><tr><td>

Description

</td><td>

Description of the software model as it appears in the product catalog.

</td></tr><tr><td>

Picture

</td><td>

An image of the software logo can be added. This logo appears in the Service Catalog if the software model is published.

</td></tr></tbody>
</table>    The Suite Components and Suite Parents related lists consist of parent and child configuration.

2.  To publish the software model to the product catalog, under **Related Links**, click **Publish to Software Catalog** and select a category for the software model.

    The values set in the Product Catalog related list are published.

3.  To show the list of discovery models that match the software publisher and product fields of the software model, under **Related Links**, click **Show Matching Discovery Models**.

    The Discovery Models list is opened in a new browser tab for your reference.

4.  To perform additional configuration, select the new software model record in the Software Models list.

    1.  In the Software Model Lifecycles related list, create a new record \(see table for field descriptions\).

<table id="table_hqc_5nn_dbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software model

</td><td>

\[Read-only\] Name of software model.

</td></tr><tr><td>

Lifecycle type

</td><td>

-   Internal
-   Publisher


</td></tr><tr><td>

Lifecycle phase

</td><td>

-   Pre Release
-   General Availability

Date the software became generally available to the market.

-   Upgrade

Only shown when the **Lifecycle type** field is Internal.

-   End of Life

Date the software was no longer supported by the publisher.

-   End of Support
-   End of Extended Support


</td></tr><tr><td>

Source

</td><td>

\[Read-only\] Internal \(for new records created manually\), or ServiceNow \(when created automatically\).

</td></tr><tr><td>

Description

</td><td>

Description of the software model lifecycle.

</td></tr><tr><td>

Phase start date

</td><td>

Date the lifecycle phase starts.

</td></tr><tr><td>

Phase end date

</td><td>

Date the lifecycle phase ends.

</td></tr><tr><td>

Risk

</td><td>

-   Very High
-   High
-   Moderate
-   Low
-   None


</td></tr></tbody>
</table>    2.  [Create a Software Asset Management Foundation plugin entitlement in classic](t_AddASoftwareEntitlementSAMF.md).

    3.  [View Software Asset Management Foundation plugin software model results in classic](t_ViewSWModelResultsSAMF.md).

        The latest software model results are shown in the Software Model Results related list.

    4.  In the Metric Attributes related list, click a metric attribute to set the attribute value field \(see table for field descriptions\).

        The Metric Attributes related list contains metric values set in [software entitlements](t_AddASoftwareEntitlementSAMF.md) and is used for reconciliation \(metric group, license metric, and software model combination\).

<table id="table_zql_nkm_11b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software model

</td><td>

Software model associated with the metric attributes.

</td></tr><tr><td>

Metric group

</td><td>

Grouping for the software metric \(Common\).

</td></tr><tr><td>

License metric

</td><td>

The license metric that the software license is counted against when reconciliation is run \(per user, per device, for example\).

</td></tr><tr><td>

Description

</td><td>

Attribute type description that is based on license metric value.

</td></tr><tr><td>

Attribute

</td><td>

Attribute type for reconciling entitlements license metric.-   Maximum active OSEs per server
-   Maximum installs per OSE
-   Maximum installs per right: For Per User, Per Device, Per Named User, and Per Named Device.
-   Maximum processors per right
-   Minimum users per processor
-   Minimum cores per processor
-   Minimum cores per server


</td></tr><tr><td>

Attribute value

</td><td>

Value of the attribute \(integer\).

</td></tr><tr><td>

Attribute value is unlimited

</td><td>

Check box for setting the attribute as unlimited.

</td></tr></tbody>
</table>    5.  [Create a vendor catalog item](../../product-catalog/task/t_CreateAVendorCatalogItem.md).


**Parent Topic:**[Configuring Software Asset Management Foundation plugin classic](../concept/samf-plugin-configuration.md)

