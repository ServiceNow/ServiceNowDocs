---
title: Software installation fields
description: Software Installation form and related list field descriptions.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Software installation fields

Software Installation form and related list field descriptions.

The list view for software installations shows the total number of software installation records for your organization based on the value specified in the **SAM Workspace License operations list count limit** system property \(**sn\_sam\_workspace.sam\_license\_operations\_list\_count**\). The default value for the record count is set to **5000000**. However, the SAM administrator can set the value for the count in the system property as required. If there are less than five million records, then the exact count is shown. If there are more than five million records, then the count is shown as 5000000+. For more information on this system property, see [Software Asset Management properties](sam-properties.md).

**Note:** This topic describes only the fields that are available on the Software Installation form. For details on all fields that are available on both the Software Installation form and the Software Installation \[cmdb\_sam\_sw\_install\] table, see [Software Installations Table Attribute Review](https://community.servicenow.com/community?id=community_article&sys_id=b1cabc88dbfe0550b3c099ead39619f6).

## Software Installation form

<table id="table_rgq_jnk_fbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the software installation as it appears in the record lists. Can be a combination of the discovered product name and edition.

</td></tr><tr><td>

Discovery model

</td><td>

Software discovery model that represents the installed software.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software.

</td></tr><tr><td>

Version

</td><td>

Version of the software.

</td></tr><tr><td>

Edition Override

</td><td>

Override of the software edition setting.For Office 365 subscriptions, this field is set from the software subscriptions record.

 If the edition for the software was not discovered, you can edit this field to set the edition, if known, so reconciliation can be performed successfully.

</td></tr><tr><td class="sub-head" colspan="2">

Installation tab

</td></tr><tr><td>

Prod id**Note:** This field has been deprecated. However, it still appears on the **Installation** tab with an empty value.

</td><td>

Unique ID for the product assigned by the manufacturer. Found through discovery.

</td></tr><tr><td>

Install location

</td><td>

Path under which the software is installed.

</td></tr><tr><td>

Install date

</td><td>

Date that the software was installed.

</td></tr><tr><td>

Revision**Note:** This field has been deprecated. However, it still appears on the **Installation** tab with an empty value.

</td><td>

Revision of the software.

</td></tr><tr><td>

Instance key

</td><td>

Unique ID for the instantiation of the software. Automatically generated when the software is installed.

</td></tr><tr><td>

Installed on

</td><td>

Hardware on which the software is installed.

</td></tr><tr><td>

Uninstall string

</td><td>

Identifier used to uninstall the software.

</td></tr><tr><td>

ISO serial number

</td><td>

ISO number of the software.

</td></tr><tr><td class="sub-head" colspan="2">

Reconciliation tab

</td></tr><tr><td>

Entitlement**Note:** This field has been deprecated. However, it still appears on the **Reconciliation** tab with an empty value.

</td><td>

The entitlement found to use with this installation.

</td></tr><tr><td>

Inferred suite

</td><td>

The inferred suite model this installation belongs to.

</td></tr><tr><td>

Omit from suites

</td><td>

Check box for not counting the software install as a component of a suite during reconciliation.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

