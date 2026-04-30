---
title: Software Asset Management Content Service
description: Opt in to the Software Asset Management Content Service to share unnormalized software installation data from your organization with ServiceNow to improve the normalization process.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Software Asset Management Content Service

Opt in to the Software Asset Management Content Service to share unnormalized software installation data from your organization with ServiceNow® to improve the normalization process.

The Software Asset Management Content Service is an IT Asset Management \(ITAM\) shared service that provides users with continual software recognition improvements. By sharing unnormalized software installation data with ServiceNow, you receive automatic content updates based on your unique software installation footprint. For more information on content updates, see [Content updates for Software Asset Management](sam-content-updates.md).

The Software Asset Management Content Service transfers data between your organization and ServiceNow through a Content Data Service \(CDS\) instance. In commercial deployments, data is transferred through a CDS instance that is deployed in a commercial data center. In National Security Cloud \(NSC\) Department of Defense \(DOD\) Impact Level 5 \(IL5\) deployments, data is transferred through a CDS instance that is deployed in an NSC DOD IL5 data center.

**Note:** Data for your NSC DOD IL5 deployments can be transferred only from ServiceNow to your organization. It cannot be transferred from your organization to ServiceNow. Since you cannot share any unnormalized software installation data with ServiceNow, you must manually create a software content request for any software product that you want to add to the Software Asset Management Content Library. After the software product is added to the Content Library, the Software Asset Management application can begin normalizing the corresponding software installations that are discovered in your NSC DOD IL5 deployments. See [Create IT Asset Management content request](../task/create-itam-content-request.md) for instructions on how to create a software content request.

No personally identifiable information is shared with ServiceNow. However, please note the exception for custom software products, as described in the Software Asset Management Content Service asset data types table below.

Data that is shared using the Software Asset Management Content Service remains secure and is properly disposed of after review, following the same ServiceNow privacy policies, procedures, tools, and techniques that are used to secure ServiceNow instances. The selection of data types that are shared with ServiceNow is configurable by your organization. In addition, data is never packaged and shipped to other ServiceNow customers.

This new content improves your normalization hit ratios, which enable you to manage your software assets better. By default, you aren’t opted in to the Content Service. For information on how to opt-in, see [Enable sharing information with Software Asset Management content service](../task/t_EnableSAMContentService.md).

If you want to exclude any software discovery models, custom software products, or custom publisher part numbers from being shared with ServiceNow, select the **Exclude from content service** check box on the Software Discovery Model, Custom Software Product, or Custom Part Number form.

The normalization process acts only on active publishers, products, and rules. Obsolete rules aren’t used. You can deactivate any Normalization Library content version at any time.

Data sharing for Software Discovery Models, Software Model Lifecycles, Part Numbers and Discovery Maps, Processor Names, and Product License Exception Rules is automatically enabled after opting in. If you don't want to share a type of asset data, select the toggle button next to the type of data on the Content Service Setup page and then select **Save**.

<table id="table_wvr_3x3_b1b"><thead><tr><th>

Software asset data

</th><th>

Definition

</th><th>

Details transferred

</th></tr></thead><tbody><tr><td>

Software Discovery Models

</td><td>

Model created to classify and reduce duplication of software installs when new installs are identified. Only Software Discovery Models with the following statuses are transferred:

-   Match not found
-   Publisher normalized
-   Partially normalized
-   Manually normalized
-   Normalized

**Note:** Only the Discovery models whose status is Normalized and Version is empty are transferred.


**Note:** To improve the accuracy of machine learning predictions, software discovery models normalized by machine learning are transferred.

</td><td>

-   Discovered publisher
-   Discovered product
-   Discovered version
-   Normalized publisher
-   Normalized product
-   Normalized version
-   Edition
-   Language
-   Platform
-   Rule table
-   Rule ID
-   ML model version
-   ML normalization status
-   ML prediction values

 **Note:** You can override the ML model used for prediction by specifying alternate values in the property `com.snc.samp.ml.overrride_ml_model_version`. The admin and sam\_admin have read access to this property but only the admin has both read and write access.

</td></tr><tr><td>

Software Product Lifecycles

</td><td>

The externally defined or publisher-defined life cycle of the software product. Only software product life cycles that aren’t created by ServiceNow and have a life-cycle type that is not internal are transferred.

</td><td>

-   Publisher
-   Product
-   Licensable version
-   Edition
-   Full version
-   Lifecycle phase
-   Phase start date
-   Lifecycle source

</td></tr><tr><td>

Part Numbers and Discovery Maps

</td><td>

Custom part numbers and custom discovery maps that are manually created to represent the publisher part number and the corresponding version and edition of the software product.

</td><td>

-   Publisher part number
-   License type
-   Publisher
-   Product
-   Discovery map
-   Version condition
-   Version
-   Edition condition
-   Edition
-   Platform
-   Platform condition
-   Language
-   Language condition
-   Database Option

</td></tr><tr><td>

Processor Names

</td><td>

Processor identified on a configuration item \(CI\). Only processors mapped to the default processor factor are transferred.

</td><td>

-   CPU type
-   Core count
-   Speed

</td></tr><tr><td>

File signatures

</td><td>

Signature that identifies software packages discovered on CIs. Software packages are discovered based on the attributes of the file, such as file name or file size. Only file signatures that are manually normalized are transferred.

</td><td>

-   File name
-   File size
-   Publisher
-   Product
-   Version
-   Edition
-   Platform
-   Language

</td></tr><tr><td>

Software Spend Transactions**Note:** Displays only if Software Spend Detection is installed.

Data sharing for Software Spend Transactions is inactive by default.

</td><td>

Software Spend Transaction records that were imported for Software Spend Detection.Only the vendor name, transaction description, general ledger account, and prediction results are transferred.

</td><td>

-   Vendor name
-   Description
-   GL account
-   Is software
-   Publisher ID
-   Product ID

</td></tr><tr><td>

Unrecognized Subscription Identifier

</td><td>

Subscription identifiers that software models aren’t associated with in the ServiceNow content.

</td><td>

-   Subscription identifier
-   Software model
-   Number of subscriptions

</td></tr><tr><td>

Common Platform Enumeration \(CPE\) normalization rule

</td><td>

Publisher, product, version, and edition, as well as their corresponding values of the software product in the Software Asset Management Content Library.

</td><td>

-   Publisher
-   Product
-   Version
-   Full Version
-   Edition
-   Language

</td></tr><tr><td>

Product License Exception Rules

</td><td>

Product, edition condition, edition, and product type, as well as their corresponding values of the software product in the Software Asset Management Content Library. The exception rules table provides an option to tag certain product editions as non-licensable​.

**Note:** If a product is labeled as non-licensable, and you want to tag an edition of that product as licensable, then you should submit a request with the Content Service team.

</td><td>

-   Product
-   Edition condition
-   Edition
-   Product type
-   Active

 **Note:** This record enables you to add your own exception rules using the Custom Product License Exception Rules \[samp\_custom\_lic\_exception\_rules\] table. This table is available to you and has reverse push capabilities. This functionality enables you to create an exception rule for a case where the product is licensable but certain editions of the product are non-licensable.

</td></tr><tr><td>

Custom Software Products

</td><td>

Custom software products that were manually added to your ServiceNow instance.

 You can add a custom software product for any publicly-available software product that does not already exist in the Software Asset Management Content Library. See [Add custom software products in workspace](../task/add-custom-software-products-workspace.md) for detailed instructions.

</td><td>

-   Publisher
-   Product
-   Product type
-   Product classification
-   Subscription software

 **Warning:** In addition to transferring these details, the Software Asset Management application transfers the instance name and customer name.

</td></tr><tr><td>

Extracted Entitlements from Software Contracts using Machine Learning

</td><td>

Software entitlement details are extracted from software contracts using machine learning. This helps in improving our machine learning model to predict product, publisher, and edition values. Additionally, it also enhances our mapping capabilities by adding more entries to the mapping table.

</td><td>

-   Publisher part number
-   Product description
-   Publisher
-   Product
-   Version
-   Edition
-   Named user type
-   Database option
-   License type
-   License metric
-   Subscription period
-   Agreement type

</td></tr></tbody>
</table>## Opting out

You can opt out at any time from the Content Service Setup page.

When you opt out, your company no longer contributes to the improvement of the normalization process. You still receive content updates, but the updates may be less applicable because they aren't informed by your company's unique software installation footprint that exists within your environment and CMDB.

Your company can rejoin the Software Asset Management Content Service at any time.

-   **[Content updates for Software Asset Management](sam-content-updates.md)**  
The Software Asset Management Content Service provides content updates to your instance twice every week that you can use to normalize your data.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[Normalization and Content Service dashboard](sam-normalization-dash.md)

[Enable sharing information with Software Asset Management content service](../task/t_EnableSAMContentService.md)

