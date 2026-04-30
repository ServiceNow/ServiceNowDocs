---
title: Customize a Discovery pattern for Software Asset Management Foundation plugin
description: Software Asset Management Foundation plugin automatically leverages SQL Server, Exchange, and Oracle Database Discovery patterns, but you can perform steps for Software Asset Management Foundation plugin to utilize additional Discovery patterns, if needed.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up Software Asset Management Foundation plugin, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Customize a Discovery pattern for Software Asset Management Foundation plugin

Software Asset Management Foundation plugin automatically leverages SQL Server, Exchange, and Oracle Database Discovery patterns, but you can perform steps for Software Asset Management Foundation plugin to utilize additional Discovery patterns, if needed.

## Before you begin

Role required: sam\_admin

## About this task

Discovery uses a series of scripts and operations \(probes, sensors, and patterns\) with the base system to collect data, process it, and update the CMDB. Although Software Asset Management Foundation plugin is already set up to utilize three common patterns \([MSSQL server discovery](https://www.servicenow.com/docs/access?context=mssql-data-collected-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), [Exchange MailBox discovery](https://www.servicenow.com/docs/access?context=r-ExchangeMailBox&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), and [Oracle database discovery](https://www.servicenow.com/docs/access?context=c_OracleDatabaseDiscovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)\), you can perform a configuration procedure to include additional patterns.

This customization automatically copies the records from the discovered pattern to the Software Installation \[cmdb\_sam\_sw\_install\] table so Software Asset Management Foundation plugin can utilize this data for reconciliation.

For more information on pattern customization, see [Discovery patterns used by ITOM Visibility](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Procedure

1.  Configure a post processing step in the discovery pattern.

    1.  Navigate to **Pattern Designer** &gt; **Discovery Patterns**.

    2.  Open the pattern record from which you would like to collect data for Software Asset Management \(for example, the discovery pattern for MySQL\).

    3.  Select and copy the **Class Name** field value.

        You will need to paste this class name value into a record field in the Software Installation Name Mapping \[cmdb\_sam\_sw\_name\_mapping\] table as part of this configuration procedure.

    4.  Click the **Pre/Post Processing** related link.

    5.  In the Sync Installed Software section, select the desired software from the list to add it \(for example, MySQL\).

        Data discovered relating to the software you select is automatically copied into the Software Installation \[cmdb\_sam\_sw\_install\] table as part of the discovery process.

    6.  Click **Update**.

2.  Add the pattern data to a new record in the Software Installation Name Mapping \[cmdb\_sam\_sw\_name\_mapping\] table.

    1.  Create a new record \(see table for field descriptions\).

<table id="table_hst_4w3_b1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Class name

</td><td>

Class name of the discovery pattern.Paste the value that you copied from the class field in discovery pattern.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the product \(for example, Oracle\).

</td></tr><tr><td>

Product

</td><td>

Product name \(for example, MySQL\).

</td></tr></tbody>
</table>    2.  Click **Submit**.

    When discovery is run, the records for the software product relating to the customized discovery pattern are utilized by Software Asset Management.

    No further configuration is needed unless you know the software product consists of an edition that is not being discovered automatically.


## What to do next

If the software product has an edition that is not being discovered, [Manually override SAM Foundation edition value](t_ManOverrideEditionSAMF.md) so the software can be successfully reconciled.

**Parent Topic:**[Setting up Software Asset Management Foundation plugin](t_SAMSetupSAMF.md)

