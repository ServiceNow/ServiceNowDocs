---
title: Software model fields
description: Software Model form and related list field descriptions.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 30
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Software model fields

Software Model form and related list field descriptions.

After you fill a software entitlement with the correct PPN, a software model is automatically created. The tabs on the Software Model form, such as Suite Components, Suite Parents, Software Product Lifecycles, Metric Attributes, Downgrade Rights, Product Lifecycles for all Versions, and so on, are populated automatically. However, you can manually add or update the software model details based on your requirements.

## Details tab

This list shows the details of a software model such as the status of the model, product details, licensing, conditions, and product catalog information.

<table id="table_isl_g4z_4hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the model. The system property **glide.cmdb\_model.display\_name.shorten** controls how software model display names are generated. Users with the admin role can configure this property. The default format is publisher + product + version + edition + platform + language.

 If the **Platform** or **Language** fields aren't set to **Anything**, the values are appended.

</td></tr><tr><td>

Status

</td><td>

The status of the model. The options are **In Production**, **Retired**, and **Sold**.

</td></tr><tr class="sub-head"><td colspan="2">

Product Details section

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software. You can use the lookup list provided.**Note:** Publisher is a reference to the company \[core\_company\] table. Only companies that you’re using internally are shown.

</td></tr><tr><td>

Product

</td><td>

Software product name. The same lookup list provided on the Software Discovery Models form. You can create a custom product from the lookup list, if desired.**Note:** If the relationship between the software publisher \[samp\_sw\_publisher\] and company \[core\_company\] tables isn’t correct, products for that publisher may not be shown.

 If the publisher and product don’t exist, you can [Add a custom software product in Software Asset Management classic](../task/t_AddACustomProduct.md).

</td></tr><tr><td>

Version condition

</td><td>

Condition qualifiers for the **Version** field.-   **starts with**
-   **is**
-   **is anything**

 The default is **is anything**.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.

</td></tr><tr><td>

Edition condition

</td><td>

Condition qualifiers for the **Edition** field.-   **starts with**
-   **is**
-   **is anything**

 The default is **is anything**.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software product to use when searching for the normalized discovery model.

</td></tr><tr><td>

Discovery map

</td><td>

A set of conditions that determine which software discovery models get mapped to the software models. Purchased rights are only applied to software discovery models that meet the condition. This matching is important for reconciliation. Discovery models with predefined suites are indicated in the **Suite defined** field. A value of **Yes** indicates that the discovery model is a suite parent.

 You can use the discovery maps provided, or you can choose to specify the condition information directly instead. A user with the sam\_admin role can choose to create a custom discovery map.

 When you select a discovery map, you may encounter a message: `Many underlying software models will be created. These might be part of suite components, downgrade rights or next version. Please validate on completion`. The message appears only if there are greater than or equal to 50 suite components for the software model and if any of the following conditions are met:

-   A software model doesn’t exist for any suite component
-   A software model doesn’t exist for any downgrade rights
-   A software model doesn’t exist for the next version

 **Note:** If you change the discovery map in an existing software model, a warning message appears. The warning message informs you that the downgrade rights on the software model and on the related entitlements also change. For example, if you change the discovery map on a software model from DMAP1 to DMAP2, and save the software model, then all the downgrade rights associated with DMAP1 are removed from the software model and the downgrade rights associated with DMAP2 are populated. However, if the value in the **Agreement type** field in the Software Entitlement form layout is **Generic**, the downgrade rights for that entitlement don't change.

 You can verify which discovery models get mapped to the software model by selecting the **Show Matching Discovery Models** related link in Software Asset Management classic. View the same results in the Software Asset Workspace, by navigating to **License operations** &gt; **Licensing** &gt; **Software models**. Select a software model and then select the **Matching Discovery Models** related list.

 If the **Publisher** and **Product** fields are empty, the values are automatically populated according to the discovery map.

</td></tr><tr><td>

Next version

</td><td>

Reference to another software model of the same manufacturer, which represents the next version of the product. The next version is defined on the discovery map and is part of the content service. The next version is populated on the software model in either of the two ways:

-   When you create a software model or update the discovery map on a software model, a business rule is triggered when you select **Save**. The next version is populated if the discovery map has a next version defined for it.
-   If the content service has the next version specified for the associated discovery map on an existing software model, the next version is populated when the schedule job **SAM- Create downgrades/upgrades for a software entitlement** runs.

**Note:** The next version is populated only after the **SAM- Create downgrades/upgrades for a software entitlement** scheduled job runs weekly.


 However, if you entered a value in the **Next version** field, that value isn’t overridden.

</td></tr><tr><td>

Product classification

</td><td>

The official United Nations Standard Products and Services Code \(UNSPSC\) classification.From this release, product classifications have been enhanced with a comprehensive set of UNSPSC codes available via the Content Service library. Updates to the UNSPSC codes will also be available via the weekly Content Service library update.

</td></tr><tr class="sub-head"><td colspan="2">

Software Licensing section

</td></tr><tr><td>

Product type

</td><td>

Product type values include: **Child**, **Driver**, **Licensable**, **Not Licensable**, **Patch**, and **Unknown**.**Note:** The reconciliation process only considers software products that are licensable.

</td></tr><tr><td>

License under management

</td><td>

The option indicating that you want to manage licenses for the specified software. If you clear this option, your software model won't be included in your reconciliation results.This option is selected by default. It’s also selected for any software models that have been upgraded.

 If you upgrade and have software models with this option selected, you can do a bulk update and clear the **License Under Management** option from any software models you don’t want to include in your reconciliation results. When you run reconciliation again, only the software models with the option still selected will display in your results.

</td></tr><tr><td>

Owner

</td><td>

The person responsible for the model.

</td></tr><tr><td>

Unit of consumption

</td><td>

Unit of measure for the software units that can be consumed.

</td></tr><tr class="sub-head"><td colspan="2">

Conditions section

</td></tr><tr><td>

Condition name

</td><td>

Name of the condition that you want to define for the software model.

</td></tr><tr><td>

Software install condition

</td><td>

Condition to account for only specific software installations during reconciliation. Installs that do not meet the required software install conditions will be included in the reconciliation process. However, these installs are likely to be flagged as unlicensed unless there is another software model that meets the required software install conditions. For example, if you have purchased Microsoft Visual Studio and set up software installation conditions for using Visual Studio only to consume licenses in your non-production environment. You need to create separate software install conditions for each component model under Visual Studio.**Note:** If you clear the **License under management** option, the software installations that meet the specified software install conditions are excluded from reconciliation instead.

 In the Software Asset Management classic application, you can add multiple software install conditions to a single software model using the following options:

-   **Add Filter Condition**: Enables you to specify all the conditions that a software installation must meet to be included in reconciliation.
-   **Add "OR" Clause**: Enables you to specify any of the conditions that a software installation can meet to be included in reconciliation.

 In the Software Asset Workspace, you can add multiple software install conditions to a single software model using the following options:

-   **or**: Enables you to specify any of the conditions that a software installation can meet to be included in reconciliation.
-   **and**: Enables you to specify all the conditions that a software installation must meet to be included in reconciliation.
-   **+ New condition set**: Enables you to specify additional sets of conditions that a software installation can meet to be included in reconciliation.

</td></tr><tr><td>

Subscription condition**Note:** This field appears only on subscription-based software models, including hybrid software models that contain both software subscriptions and on-premise software installations.

</td><td>

Condition to account for only groups of subscriptions during reconciliation. Only the subscriptions that meet the specified subscription conditions are included in reconciliation. For example, you can set a subscription condition to reconcile subscriptions from only a specific geographic location or business department. **Note:** If you clear the **License under management** option, the subscriptions that meet the specified software conditions are excluded from reconciliation instead.

 In the Software Asset Management classic application, you can add multiple subscription conditions to a single software model using the following options:

-   **Add Filter Condition**: Enables you to specify all the conditions that a subscription must meet to be included in reconciliation.
-   **Add "OR" Clause**: Enables you to specify any of the conditions that a subscription can meet to be included in reconciliation.

 In the Software Asset Workspace, you can add multiple subscription conditions to a single software model using the following options:

-   **or**: Enables you to specify any of the conditions that a subscription can meet to be included in reconciliation.
-   **and**: Enables you to specify all the conditions that a subscription must meet to be included in reconciliation.
-   **+ New condition set**: Enables you to specify additional sets of conditions that a subscription can meet to be included in reconciliation.

 **Warning:** You can’t add subscription conditions to out-of-the-box software models. You must create a software model to define subscription conditions for the associated subscription software.

</td></tr><tr class="sub-head"><td>

General

</td><td>

 

</td></tr><tr><td>

Short description

</td><td>

A brief description of the model.

</td></tr><tr><td>

Platform

</td><td>

Platform of the software product to use when searching for the normalized discovery model.The default is **Anything** for Windows, macOS, UNIX.

</td></tr><tr><td>

Language

</td><td>

Language of the software product to use when searching for the normalized discovery model, which is populated after it has been normalized or added manually.The default is **Anything**.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

Allows to override the way assets are tracked for the model.

</td></tr><tr><td>

Asset tracking unit

</td><td>

Unit of measure for asset.

</td></tr><tr><td>

Cost

</td><td>

The cost of a single unit of the software.

</td></tr><tr><td>

Certified

</td><td>

Indicates if the product associated to this software model is approved or unapproved by TRM.

 When a enterprise architect adds a product to the TRM library, the product is flagged as either approved or unapproved. When a software model is created for an approved product, this check box is automatically selected.

 If you create a software model for an unapproved product, the software model is designated as restricted. During the reconciliation process, any software installations associated with unapproved products are identified as removal candidates.

 If you activate the Application Portfolio Management - TRM \(com.snc.apm\_trm\) plugin for software models that already exist, this check box may or may not be selected depending on whether the product is approved.

</td></tr><tr><td>

Restricted software

</td><td>

Option for restricting software.Restricted software identifies software that you shouldn’t install in your environment \(inappropriate software, or software with vulnerabilities, for example\).

 If the removal candidates don't exist, a scheduled job runs nightly that creates removal candidates for restricted software.

</td></tr><tr><td>

License all installs accessed by clients**Note:** This field appears only on software models that are associated with [client access records](../task/t_AddAClientAccessRec.md), except for Oracle DB Server software models.

</td><td>

Option to license the configuration items \(CIs\) that the software is installed on, based on conditions that you specify on the software model, such as software install conditions. If any of the associated client access records are unlicensed due to insufficient rights, all CIs remain unlicensed.If you disable this option, only the CIs that have been added to your client access records are licensed. See [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md) for detailed instructions on how to add CIs to your client access records.

 If you enable this option after you have already added CIs to your client access records, those CIs are deleted from your records and then subsequently licensed based on the conditions that you specify on the software model.

</td></tr><tr><td>

Database option**Note:** This field appears only on Oracle Database software models.

</td><td>

Oracle database option or management pack. Each option or pack requires a separate software model. The database option is an identifier for software models.

 This field is shown when creating software models that meet the following conditions:

-   The **Publisher** is **Oracle**.
-   The **Product** is **DB Server**.

</td></tr><tr><td>

Database option condition**Note:** This field appears only on Oracle Database software models that are associated with a database option or management pack, as specified in the **Database option** field.

</td><td>

Condition to account for only the subsets of Oracle Database options or management packs during reconciliation. Only the database options or management packs that meet the specified database option conditions are included in the reconciliation.**Note:** If you clear the **License under management** option, the database options or management packs that meet the specified database option conditions are excluded from reconciliation instead.

 In the Software Asset Management classic application, you can add multiple database option conditions to a single software model using the following options:

-   **Add Filter Condition**: Enables you to specify all the conditions that a database option or management pack must meet to be included in reconciliation.
-   **Add "OR" Clause**: Enables you to specify any of the conditions that a database option or management pack can meet to be included in the reconciliation.

 In the Software Asset Workspace, you can add multiple database option conditions to a single software model using the following options:

-   **or**: Enables you to specify any of the conditions that a database option or management pack can meet to be included in the reconciliation.
-   **and**: Enables you to specify all the conditions that a database option or management pack must meet to be included in reconciliation.
-   **+ New condition set**: Enables you to specify additional sets of conditions that a database option or management pack can meet to be included in reconciliation.

</td></tr><tr><td>

Apply to subscriptions

</td><td>

Option to apply this software model to only subscription-based software suites. If you don’t enable this option, you can apply this software model to only software suites with installed software.

</td></tr><tr><td>

Auto-generate client access for allocations. **Note:** This field appears only on Oracle Database Server software models.

 **Important:** To use this option, you must request the Data Collection for Oracle Global Licensing and Advisory Services application from the ServiceNow Store. See [Request Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)](../task/request-data-collection-oracle-glas-app.md) for more details on the Data Collection for Oracle Global Licensing and Advisory Services application.

</td><td>

Option to automatically generate and manage client access records for Oracle Database Server. If you enable this option, the Software Asset Management application generates and manages client access records based on your latest Oracle Database Server Named User Plus entitlements, the users, and devices that the associated rights are allocated to, and the Oracle database instances that are supported by these users and devices. The Software Asset Management application generates a separate client access record for each supported database instance. If you disable this option after the Software Asset Management application has automatically generated client access records for Oracle Database Server, those client access records are no longer managed and updated automatically. You must manage and update those client access records manually to keep them accurate and up to date.

 If you enable this option and already have existing client access records for Oracle Database Server, all automatically generated client access records are managed and updated automatically again. However, you must continue to manage and update all manually generated client access records.

</td></tr><tr class="sub-head"><td>

Product Catalog

</td><td>

 

</td></tr><tr><td>

Catalog Item

</td><td>

Information about the model as it appears in the product catalog and service catalog. Information only appears if the model has been published to the product catalog.

</td></tr><tr><td>

Description

</td><td>

Description of the software model as it appears in the product catalog.

</td></tr><tr><td>

Picture

</td><td>

Image of the software logo can be added. This logo appears in the service catalog if the software model is published.

</td></tr><tr class="sub-head"><td>

Activity

</td><td>

 

</td></tr><tr><td>

Work notes

</td><td>

Notes about the work order task that are visible to all users within your organization.

</td></tr></tbody>
</table>## Suite Components

This list shows the software suite component details. Software components are the suite children of a software suite parent. For more information, see [Software Asset Management software suites](../concept/software-suites.md).

<table id="table_nyv_lmc_xhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow automated content update

</td><td>

Option enabling ServiceNow to automatically send updated suite definitions to your instance through weekly content updates.

</td></tr><tr><td>

Suite child

</td><td>

The child product or products of the suite. For example, Microsoft Word and Microsoft Excel are child products of Microsoft Office.

</td></tr><tr><td>

Mandatory

</td><td>

Requirement of a suite component. A suite component can be **Optional**, **Always Mandatory**, or **Mandatory Group**.Set to **Always Mandatory** if the software must be installed to count the model as a suite.

</td></tr><tr><td>

Suite relationship assumed

</td><td>

Relationship that indicates that multiple software models exist for one or more of the suite components. Therefore, the relationship between suite parent and suite component was assumed. Review the created suite components to ensure the relationship is correct.

</td></tr><tr class="sub-head"><td>

Suite Content Usage

</td><td>

 

</td></tr><tr><td>

Inference Option: **Number** and **Percent**

</td><td>

**Number**: Specifies the number of components installed for the suite. Specify a number lesser than or equal to the number of components.

**Note:** For any new software models being created with suite components, the **Number** option is selected by default.

 **Percent**: Specifies what percentage of the components must be installed for the suite.

**Note:** For existing software models with suite components that were using the inference percent, the **Percent** option is selected by default. However, you can choose to use the **Number** option.

 If the system property **Use component licenses to optimize compliance when suite licenses run out** is set to true, Inference percent specifies a threshold to determine whether the suite or component licensing is optimal.

</td></tr><tr><td>

Allow automated content update

</td><td>

Option for enabling automatic content changes to software models.

</td></tr></tbody>
</table>## Suite Parents

This list shows the software suite parent details. For more information, see [Software Asset Management software suites](../concept/software-suites.md).

<table id="table_axt_czp_l3b"><thead><tr><th>

 

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suite parent

</td><td>

The parent suites to which the software is assigned. For example, the parent suite for several common Microsoft products is a version of Microsoft Office.

</td></tr><tr><td>

Suite child

</td><td>

 

</td></tr><tr><td>

Mandatory

</td><td>

Requirement of a suite component. A suite component can be **Optional**, **Always Mandatory**, or **Mandatory Group**.Set to **Always Mandatory** if the software must be installed to count the model as a suite.

</td></tr><tr><td>

Suite relationship assumed

</td><td>

Relationship that indicates that multiple software models exist for one or more of the suite components, therefore the relationship between suite parent and suite component was assumed. Review the created suite components to ensure the relationship is correct.

</td></tr></tbody>
</table>## Software Product Lifecycles

This list shows the lifecycle information of a software product version. For more information, see the Software Product Lifecycle report section in [Software models and Software entitlements](../concept/software-models-and-entitlements.md).

<table id="table_hqc_5nn_dbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher

</td><td>

Name of publisher.

</td></tr><tr><td>

Product

</td><td>

Name of the software product.

</td></tr><tr><td>

Version

</td><td>

Licensable version of the software

</td></tr><tr><td>

Edition

</td><td>

Edition of the software.

</td></tr><tr><td>

Full Version

</td><td>

The granular licensable version of the software.

</td></tr><tr><td>

Phase start date

</td><td>

Date the life-cycle phase starts.

</td></tr><tr><td>

Lifecycle type

</td><td>

The product life cycle type values include:-   **Internal**: The life cycle date is specific to the customer \(for example, based on their internal policy, based on a custom contract/agreement with the publisher\).
-   **Publisher**: The life cycle date comes from publisher sources and is not specific to a customer.

</td></tr><tr><td>

Risk

</td><td>

The risk level to an organization with regards to the lifecycle phase. For example, the risk for the end of support phase for a publisher maybe moderate or the end of life phase maybe high.

Risk type values include:-   **Very High**
-   **High**
-   **Moderate**
-   **Low**
-   **None**

</td></tr><tr><td>

Lifecycle phase

</td><td>

Lifecycle phase values include:-   **Pre Release**: Date the software was pre-released.
-   **General Availability**: Date the software became generally available to the market.
-   **Upgrade**

**Note:** Only shown when the **Lifecycle type** field is Internal.

-   **End of Support**: Date by which the software will not be enhanced by the publisher.

This value corresponds to the Mainstream Support end date for Microsoft according to its [Fixed Lifecycle Policy](https://learn.microsoft.com/en-us/lifecycle/policies/fixed).

-   **End of Extended Support**: Date by which the publisher will no longer provide any support or updates to the software.

This value corresponds to the Extended Support end date for Microsoft according to its [Fixed Lifecycle Policy](https://learn.microsoft.com/en-us/lifecycle/policies/fixed).

-   **End of Life**: Date by which the software will no longer be manufactured by the publisher.

**Note:** This value isn't applicable for Microsoft because it follows the fixed lifecycle policy providing mainstream support and extended support. For more information, see [Fixed Lifecycle Policy](https://learn.microsoft.com/en-us/lifecycle/policies/fixed).


</td></tr><tr><td>

Active

</td><td>

Indicates if the lifecycle is to be considered or not while evaluating the risk of the software.**Note:** By default, only active life cycles are displayed.

</td></tr><tr><td>

Source

</td><td>

Source of the lifecycle. If the record is created manually, it's set to **Internal**. If it's created automatically, the field is set to ServiceNow.

</td></tr><tr><td>

Description

</td><td>

Description of the software product lifecycle.

</td></tr></tbody>
</table>## Software Entitlements

This list shows the entitlement terms of your software license. For more information, see the Software entitlements section in [Software models and Software entitlements](../concept/software-models-and-entitlements.md).

<table id="table_erg_3b1_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Automatically generated name based on the software model display name.

</td></tr><tr><td>

License metric

</td><td>

License metric for the license group that the software license is counted against when reconciliation is run. The options for license metric change based on the Metric group field. For more information, see [Software license metrics](../concept/c_SAMLicenseMetrics.md).

</td></tr><tr><td>

Metric group

</td><td>

Metric group based on the Software Model field. Each metric group has a set of license metrics that are specific to the software publisher.

</td></tr><tr><td>

License type

</td><td>

The type determines whether the rights grant full access to the software or if they’re being upgraded from a previous version of the software.The following are the various license types:

-   Perpetual
-   Perpetual + Software Assurance
-   Software Assurance
-   Subscription
-   Step-up
-   Subscription Step-up

</td></tr><tr><td>

Active rights

</td><td>

Number of rights granted for this entitlement.

</td></tr><tr><td>

Purchased rights

</td><td>

Number of rights purchased for this entitlement.

</td></tr><tr><td>

Total cost

</td><td>

Total cost of the entitlement calculated from the unit cost.

</td></tr></tbody>
</table>## Override License Costs

This list shows the override license cost information for your software entitlements.

<table id="table_umm_ygl_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Model

</td><td>

The software model that the software entitlement belongs to.

</td></tr><tr><td>

Metric Group

</td><td>

The metric group the software entitlement belongs to.

</td></tr><tr><td>

License Metric

</td><td>

The license metric specified for the software entitlement.

</td></tr><tr><td>

License Cost

</td><td>

Cost of the license.

</td></tr><tr><td>

License &amp; Maintenance Cost

</td><td>

Cost of the license combined with cost of the maintenance license.

 Specify a license cost or a license and maintenance cost, to override the true-up cost during reconciliation. If no values are specified in the **License Cost** or **License &amp; Maintenance Cost** fields, the software entitlement cost is used for true-up cost calculations.

 **Note:** For SaaS licenses, only the license cost applies. The license &amp; maintenance cost does not apply.

</td></tr><tr><td class="sub-head" colspan="2">

The following fields appear when the value selected in the License Metric field is Employee.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the license cost is to be considered for true-up cost calculations.

</td></tr><tr><td>

Lower limit

</td><td>

The minimum number of employees that the licenses are required for.

</td></tr><tr><td>

Upper limit

</td><td>

The maximum number of employees that the licenses are required for.

</td></tr></tbody>
</table>## Software Model Results

This list shows the software model results associated with the license metric results.

<table id="table_fsf_cqk_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

Status of the software model. Possible values are Compliant and Not Compliant.Select the **Status** field to open the corresponding Software Model Results record, where you can view more in-depth information about the software model result. See [View software model results](../task/t_ViewSWModelResults.md) for detailed descriptions of each field on the Software Model Results form.

</td></tr><tr><td>

Agreement type

</td><td>

Agreement type is set on the software entitlement.-   Common: Generic, Enterprise License Agreement \(ELA\)
-   IBM: Generic, Enterprise License Agreement \(ELA\), International Program License Agreement \(IPLA\), IBM Customer Agreement \(ICA\), Unlimited Level Agreement \(ULA\)
-   Microsoft: Generic, Enterprise License Agreement \(ELA\)
-   Oracle: Generic, Unlimited Level Agreement \(ULA\)
-   VMware: Generic, Enterprise License Agreement \(ELA\), Enterprise Purchasing Program \(EPP\), Volume Purchasing Program \(VPP\)

 **Note:** If the agreement type is Enterprise Level Agreement or Unlimited Level Agreement, the **Status** is Compliant even if there are unlicensed installations or unlicensed subscriptions.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Number of unlicensed software installations that are not covered by any entitlements.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating unlicensed installations based on the lowest number of rights needed \(rights needed \* average price per right from entitlements\). The lowest cost from Purchase Rights remediation options.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of rights not being used. The sum of the Over Licensed amount from the True-up value costs.

</td></tr><tr><td>

Potential savings

</td><td>

 

</td></tr><tr><td>

Group

</td><td>

Group specified on which to run reconciliation. Values include None, Country, Department, Company, Region, and Cost Center.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup specified on which to run reconciliation. Values include None, Country, Department, Company, Region, and Cost Center.

</td></tr></tbody>
</table>## Metric Attributes

This list shows the metric attributes information of a software model.

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

Grouping for the software metric.If you have optional publisher packs installed that the software applies to, those options are shown. Otherwise, the metric group value is **Common**.

</td></tr><tr><td>

License metric

</td><td>

The license metric that the software license is counted against when reconciliation is run \(per user, per device, for example\).

</td></tr><tr><td>

Description

</td><td>

Attribute type description that is based on the license metric value.

</td></tr><tr><td>

Attribute

</td><td>

Attribute type for reconciling entitlement license metrics. For more information on each attribute type, see [Software model metric attributes](sw-metric-attributes.md).

</td></tr><tr><td>

Attribute value

</td><td>

Value of the attribute \(integer\).

</td></tr><tr><td>

Attribute value is unlimited

</td><td>

Option for setting the attribute as unlimited.

</td></tr></tbody>
</table>## Vendor Catalog Items

This list shows you the details of the software models associated with a vendor. For more information, see [Vendor catalog items](../../product-catalog/concept/c_ManageVendorCatalogItems.md).

|Field|Description|
|-----|-----------|
|Name|Name of the catalog item.|
|Product ID|Item identification number assigned by your organization.|
|Short Description|A brief description of the item.|
|Vendor Price|The price at which the item is available in the vendor catalog. If the vendor offers a discount, the vendor price reflects the discounted price.|
|Rank tier|Displays the overall ranking for this vendor's products and services.|

## Client Access

This list shows a client access record details of the users or devices that are accessing a particular version of your server software using a client access license \(CAL\).

<table id="table_kxy_z3q_l3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the client access record. Select a name to open the corresponding client access record, where you can view more in-depth information about the record, such as the users or devices that the associated client access licenses \(CALs\) are assigned to and the configuration items \(CIs\) that the associated server software is installed on. See [Add a software client access record in Software Asset Management classic](../task/t_AddAClientAccessRec.md) for more information on client access records in the Software Asset Management classic application. See [Create a software client access record in workspace](../task/create-clientaccess-workspace.md) for more information on client access records in the Software Asset Workspace.

</td></tr><tr><td>

Count

</td><td>

Number of unique users or devices that are granted access to the associated server.**Note:** If you are using a Citrix software model and User/Device CAL type, the **Count** field is based on the number of user/device licenses that are assigned to your users or shared devices.

</td></tr><tr><td>

Type

</td><td>

Type of CAL that is associated with the client access record.-   **User CAL**: Licenses each user that accesses the associated server, regardless of the number of devices that each user is using to access the server.

-   **Device CAL**: Licenses each device that accesses the specified server, regardless of the number of users that are using each device to access the server.

-   **User/Device CAL**: Licenses each user or device that accesses the associated server.

**Note:** If you are using a Citrix software model, the User/Device CAL type is based on the user/device licenses that are assigned to your users or shared devices.

-   **Reserved Hourly Average Sensor**: This metric counts the number of unique active endpoints per clock-hour and averages them over a rolling 28-day period. The count of Reserved Hourly Average Sensor Licenses resets at the start of each clock-hour.
-   **Sensor Subscription**: This metric calculates license usage by averaging endpoint counts over four consecutive weeks. Weekly endpoint counts are based on the total number of endpoints consumed in the previous seven days.

**Note:** The Reserved Hourly Average Sensor and Sensor Subscription license metrics are applicable only for CrowdStrike and are available with Yokohama Patch 1, Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) 15.0.8, and Software Asset Management \(sn\_itam\_samp\) 2.1.0 version onwards. If you are on any version for Yokohama below Patch 1, refer [KB1801232](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=ef634dac83935610cdbbc430feaad3d9).

</td></tr><tr><td>

Cost Center

</td><td>

Cost center of the users or devices that are granted access to the associated server.

</td></tr><tr><td>

Department

</td><td>

Business department of the users or devices that are granted access to the associated server.

</td></tr><tr><td>

Location

</td><td>

Geographic location of the users or devices that are granted access to the associated server.

</td></tr><tr><td>

Company

</td><td>

Company of the users or devices that are granted access to the associated server.

</td></tr></tbody>
</table>## Software Subscriptions

This list shows the available subscriptions for a software application.

<table id="table_z5t_zb1_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Software publisher and product for the subscription.

</td></tr><tr><td>

User principal name

</td><td>

The user's email address for the subscription.

</td></tr><tr><td>

Software model

</td><td>

The software model for the subscription.

</td></tr><tr><td>

Last activity

</td><td>

The last date when this subscription was last used.

</td></tr><tr><td>

Inactive days

</td><td>

The number of days for which a user's subscription has been inactive.This field is visible on the Software Subscriptions form when the **Last activity** field is not empty. Inactive days are calculated using the value in the **Last activity** field.

</td></tr><tr><td>

Subscription profile

</td><td>

Profile that is associated with the subscription identifier.

</td></tr></tbody>
</table>## Downgrade Rights

This list shows the downgrade rights information of a software model. For more information, see [Downgrade Rights](../concept/downgrade-rights.md).

<table id="table_mzw_bv2_fhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Parent software model

</td><td>

Parent \(or the topmost hierarchy\) of the software model.

</td></tr><tr><td>

Software model

</td><td>

Software model associated with the downgrade rights. Based on the parent software model that you select, the related software models appear in the list. For example, if you select Microsoft SQL Server 2012 Standard as the parent software model, only Microsoft -related software models appear in the list.

</td></tr><tr><td>

Source

</td><td>

Source of the downgrade rights. If the record is created manually, it's set to **Internal**. If it's created automatically, the field is set to ServiceNow.

</td></tr><tr><td>

Active

</td><td>

Option that indicates if the downgrade rights on the software model are active or not. If needed, you can deactivate the downgrade rights. Only the active downgrade rights appear in the field. To see all the downgrade rights, remove the Active condition from the filter. If you deactivate a downgrade right on a software model, the change is propagated to the related software entitlement downgrade rights, irrespective of the source of the downgrade right. You cannot deactivate the downgrade right on a software model and keep the downgrade right activated on the software entitlement.

 To deactivate a downgrade right, double-click the field to display the toggle button, select **false**, and then select the Save icon \(![Save icon](../image/save-icon.png)\).

-   **false**: deactivates the downgrade right on the software model and on the related software entitlements.
-   **true**: reactivates the downgrade right on the software model and on the related software entitlements.

</td></tr></tbody>
</table>## Matching Discovery Models

This list shows the discovery maps that match the software publisher and product fields of the software model.

<table id="table_xcy_2c1_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the discovery model. This value is generated automatically using the discovered publisher, discovered product, and discovered version.

</td></tr><tr><td>

Normalization status

</td><td>

Status of the normalization process:-   Normalized
-   Partially Normalized
-   Publisher Normalized
-   Match Not Found
-   Manually Normalized
-   New

</td></tr><tr><td>

Publisher

</td><td>

Normalized publisher of the software.

</td></tr><tr><td>

Product

</td><td>

Normalized product name of the software.

</td></tr><tr><td>

Version

</td><td>

Normalized version of the software product.

</td></tr><tr><td>

Edition

</td><td>

Normalized edition of the software.

</td></tr></tbody>
</table>## Product Lifecycles for all Versions

This list shows the life cycle for all versions of the software product.

<table id="table_d5y_533_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Publisher

</td><td>

Name of the publisher.

</td></tr><tr><td>

Product

</td><td>

Name of the software product.

</td></tr><tr><td>

Version

</td><td>

Licensable version of the software.

</td></tr><tr><td>

Full version

</td><td>

The granular licensable version of the software.

</td></tr><tr><td>

Edition

</td><td>

Edition of the software.

</td></tr><tr><td>

Lifecycle phase

</td><td>

Life-cycle phase values include:-   **Pre Release**: Date the software was pre-released.
-   **General Availability**: Date the software became generally available to the market.
-   **Upgrade**

**Note:** Only shown when the **Lifecycle type** field is Internal.

-   **End of Life**: Date by which the software will no longer be manufactured by the publisher.

**Note:** This value isn't applicable for Microsoft because it follows the fixed life-cycle policy providing mainstream support and extended support. For more information, see [Fixed Lifecycle Policy](https://learn.microsoft.com/en-us/lifecycle/policies/fixed).

-   **End of Support**: Date by which the software will not be enhanced by the publisher.

This value corresponds to the Mainstream Support end date for Microsoft according to its [Fixed Lifecycle Policy](https://learn.microsoft.com/en-us/lifecycle/policies/fixed).

-   **End of Extended Support**: Date by which the publisher will no longer provide any support or updates to the software.

This value corresponds to the Extended Support end date for Microsoft according to its [Fixed Lifecycle Policy](https://learn.microsoft.com/en-us/lifecycle/policies/fixed).


</td></tr><tr><td>

Lifecycle type

</td><td>

The product life cycle type values include:-   **Internal**: The life cycle date is specific to the customer \(for example, based on their internal policy, based on a custom contract/agreement with the publisher\).
-   **Publisher**: The life cycle date comes from publisher sources and is not specific to a customer.

</td></tr><tr><td>

Source

</td><td>

Source of the life cycle.-   If the record is created manually, this value set to Internal.
-   If the record is created automatically, the field is set to ServiceNow.

</td></tr><tr><td>

Description

</td><td>

Description of the software product life cycle.

</td></tr><tr><td>

Phase start date

</td><td>

Date the life-cycle phase starts.

</td></tr><tr><td>

Risk

</td><td>

The risk level to an organization with regards to the life-cycle phase. For example, the risk for the end of support phase for a publisher maybe moderate or the end of life phase maybe high.Risk type values include:

-   Very High
-   High
-   Moderate
-   Low
-   None

</td></tr><tr><td>

Active

</td><td>

Indicates if the life cycle is to be considered or not while evaluating the risk of the software.**Note:** By default, only active life cycles are displayed.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

