---
title: Quick start tests for Software Asset Management
description: Validate that Software Asset Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Quick start tests for Software Asset Management

Validate that Software Asset Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Software Asset Management quick start tests require activating the Software Asset Management Professional plugin \(com.snc.samp\). Some quick start tests require activating the following additional plugins.

-   Software Asset Management - Spend Detection \(com.sn\_sam\_spend\)
-   Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\)
-   Software Asset Management Professional for SAP \(com.sn\_samp\_sap\)
-   Software Asset Management Professional for Oracle \(com.snc.samp.oracle\)
-   Software Asset Management - SaaS License Management Integrations \(sn\_sam\_saas\_int\)

<table id="atf-tests-sam"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

SAM - Mapping Custom PPN/DMAP to newly published PPN and Content

</td><td>

Validates the replacement of a custom publisher part number \(PPN\) with a new Software Asset Management Content Service PPN.

</td><td>

San Diego

</td></tr><tr><td>

SAM - Oracle PaaS BYOL

</td><td>

-   Validates the addition of the new Serverless Hardware \[cmdb\_ci\_serverless\_hardware\] table, which stores information about PaaS devices.
-   Validates the license compliance of Oracle Database servers in Amazon Web Services \(AWS\) PaaS environments.

 **Note:** Requires the Software Asset Management Professional for Oracle \(com.snc.samp.oracle\) plugin and the CMDB CI Class Models store application.

</td><td>

Rome

</td></tr><tr><td>

SAM - Software Product Lifecycles records on Software Model

</td><td>

Validates that the Software Lifecycle tab on the Software Model form is showing records.**Note:** Requires demo data and the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Quebec

</td></tr><tr><td>

SAM - BYOL

</td><td>

-   Validates the purchase date on the Software Entitlement form
-   Validates the addition of newly added column legacy\_license on the License Metric Results \[samp\_license\_metric\_result\] and License Position Report \[samp\_license\_position\_report\] tables
-   Validates the addition of newly added columns, cloud\_license\_type and cloud\_license \_type\_source in the Software Installations \[cmdb\_sam\_sw\_install\] table

**Note:** Requires the Software Asset Management Professional for Micorosft \(com.snc.samp.microsoft\) plugin.

</td><td>

Quebec

</td></tr><tr><td>

SAM - Validate CIS Suites

</td><td>

Validates reconciliation of Core Infrastructure Server \(CIS\) suites along with downgrade rights.**Note:** Requires demo data and the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - PerCoreForMSCluster

</td><td>

Verifies the reconciliation functionality for Microsoft per core with cluster.**Note:** Requires the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Validate upgrade/downgrade during Reconciliation for Microsoft publisher

</td><td>

Validates upgrade and downgrade rights during reconciliation for Microsoft products.**Note:** Requires demo data and the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Generate demand to consolidate SaaS applications

</td><td>

Validates generation and submission of a demand on SaaS applications.**Note:** Requires the Software Asset Management - Spend Detection \(com.sn\_sam\_spend\) plugin and the PPM standard \(com.snc.financial\_planning\_pmo\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Software Model and Software Entitlement checks for SAP Engines

</td><td>

Verifies that the Software Model and Software Entitlement forms change when the product is an SAP engine.**Note:** Requires the Software Asset Management Professional for SAP \(com.sn\_samp\_sap\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Downgrade Rights on Software Model

</td><td>

Validates that the downgrade rights pushed from the content service are correctly populated on the Downgrade Rights related list on the software model form.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Multi-core pack validation on Software Entitlement

</td><td>

Validates the functionality of new fields for a multi-core pack on software entitlements.**Note:** Requires the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Downgrade Rights on Software Entitlement

</td><td>

Validates that the downgrade rights pushed from the content service are correctly populated on the Downgrade Rights related list on the software entitlement form.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Software Spend Transaction

</td><td>

Validates the creation of a Software Spend Transaction.**Note:** Requires the Software Asset Management - Spend Detection \(com.sn\_sam\_spend\) plugin.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Software Model and Software Entitlement

</td><td>

Tests that a user can create a software model and software entitlement and validates those records.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Installation and Discovery Model

</td><td>

Tests that a user can create a software installation and discovery model and validates those records.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Entitlement Creation Using Custom PPN

</td><td>

Creates a custom software product, a custom DMAP for the custom product, a custom Part Number for the custom DMAP, a software entitlement using the custom Part Number, and verifies that a software model is automatically created.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Model Checks for SAP Named Users

</td><td>

Tests that the software model form changes when the publisher is SAP and the product is Named Users.**Note:** Requires the Software Asset Management Professional for SAP \(com.sn\_samp\_sap\) plugin.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Model Checks for SaaS

</td><td>

Tests that the Software Model form changes when a SaaS product is selected.**Note:** Requires the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.

</td><td>

New York

</td></tr><tr><td>

SAM - Validate Fields on SaaS Software Products

</td><td>

Tests that the **Subscription software** and **Ignore installs** fields are present on the Software Product form.**Note:** Requires the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.

</td><td>

New York

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

