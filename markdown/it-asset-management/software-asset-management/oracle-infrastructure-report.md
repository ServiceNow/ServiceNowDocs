---
title: Oracle Infrastructure report
description: You can use the Oracle Infrastructure report to gain visibility into your Oracle infrastructure. This report includes information about the Oracle databases that you are running and the configuration items that are supporting these databases.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Infrastructure report

You can use the Oracle Infrastructure report to gain visibility into your Oracle infrastructure. This report includes information about the Oracle databases that you are running and the configuration items that are supporting these databases.

**Note:** The Oracle Infrastructure report is domain separated.

You can view the Oracle Infrastructure report in both the Software Asset Management classic application and the Software Asset Workspace.

To view this report in the Software Asset Management classic application, navigate to **All** &gt; **Reports** &gt; **View/Run** on your ServiceNow instance. At the top of the Reports page, select **All**. From the list of all available reports, locate and select **Oracle infrastructure report**.

To view this report in the Software Asset Workspace, navigate to **Workspaces** &gt; **Software Asset Workspace** on your ServiceNow instance. After the Software Asset Workspace launches, navigate to **License usage** &gt; **Reports** &gt; **Oracle infrastructure report**.

<table id="table_eny_lzk_npb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required by \(Device\)

</td><td>

Configuration item, such as a server, cluster, vCenter, or datacenter, that the Oracle database, database option, or management pack is installed on.Select an entry to view additional information about the licensing requirements for that configuration item. See [Licenses Required By form](oracle-infrastructure-report.md#section_ahj_vhh_vpb) for more details.

</td></tr><tr><td>

Database option

</td><td>

Database option or management pack that is being used with the Oracle database.

</td></tr><tr><td>

Version

</td><td>

Oracle Database version that is installed on your configuration item.

</td></tr><tr><td>

Edition

</td><td>

Oracle Database edition that is installed on your configuration item.

</td></tr><tr><td>

Software model

</td><td>

Software model that is associated with the Oracle database, database option, or management pack.

</td></tr><tr><td>

License metric result

</td><td>

License metric that the Oracle license is counted against when reconciliation runs. The options are **Named User Plus** and **Per Processor**.

</td></tr><tr><td>

Licenses required

</td><td>

Number of rights that are required for license compliance.

</td></tr><tr><td>

Model ID

</td><td>

Model ID of the configuration item that the Oracle database, database option, or management pack is installed on.

</td></tr><tr><td>

CPU manufacturer

</td><td>

Manufacturer of the CPU that is used by the configuration item.

</td></tr><tr><td>

CPU type

</td><td>

Type of CPU that is used by the configuration item.

</td></tr><tr><td>

CPU count

</td><td>

Number of CPUs within the configuration item.

</td></tr><tr><td>

CPU core count

</td><td>

Number of cores within each CPU.

</td></tr><tr><td>

CPU core thread

</td><td>

Number of threads that divide each core within a CPU.

</td></tr><tr><td>

Oracle core factor

</td><td>

Oracle processor core factor that is used to determine the number of required rights.

</td></tr><tr><td>

CPU speed \(MHz\)

</td><td>

Clock speed \(in megahertz\) of the CPU that is used by the configuration item.

</td></tr><tr><td>

Purchased

</td><td>

Number of rights that you have purchased.

</td></tr><tr><td>

Operating System

</td><td>

Operating system of the configuration item that the Oracle database, database option, or management pack is installed on.

</td></tr><tr><td>

Socket Count

</td><td>

Number of slots available on the motherboard.

</td></tr></tbody>
</table>## Licenses Required By form

To view additional information about the licensing requirements for a specific configuration item, select the configuration item from the **Required by \(Device\)** field of the Oracle Infrastructure report. The corresponding Licenses Required By form opens, where you can view information about the license consumption, Oracle Database software installations, Oracle Database options and management packs, and database instances that are associated with the selected configuration item.

<table id="table_xtz_s2h_vpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Required by

</td><td>

Configuration item, such as a server, cluster, vCenter, or datacenter, that the Oracle database, database option, or management pack is installed on.

</td></tr><tr><td>

License metric result

</td><td>

License metric that the Oracle license is counted against when reconciliation runs. The options are **Named User Plus** and **Per Processor**.

</td></tr><tr><td>

Licenses required

</td><td>

Number of rights that are required for license compliance.

</td></tr><tr><td>

Licensing status

</td><td>

Licensing status of the Oracle database, database option, or management pack.

</td></tr><tr><td class="sub-head" colspan="2">

License Consumption Details related list

</td></tr><tr><td>

Required by

</td><td>

Configuration item that the Oracle database, database option, or management pack is installed on.

</td></tr><tr><td>

Model ID

</td><td>

Model ID of the configuration item.

</td></tr><tr><td>

Processor name

</td><td>

Name of the processors that are running on the configuration item.

</td></tr><tr><td>

Processors

</td><td>

Number of processors that are running on the configuration item.

</td></tr><tr><td>

Cores

</td><td>

Total number of cores within the configuration item.

</td></tr><tr><td>

CPU count

</td><td>

Number of CPUs within the configuration item.

</td></tr><tr><td>

CPU core count

</td><td>

Number of cores within each CPU.

</td></tr><tr><td>

CPU core thread

</td><td>

Number of threads that divide each core within a CPU.

</td></tr><tr><td>

Core Factor

</td><td>

Oracle processor core factor that is used to determine the number of required rights.

</td></tr><tr><td>

Licenses required

</td><td>

Number of rights that are required for license compliance.

</td></tr><tr><td>

CPU speed \(MHz\)

</td><td>

Clock speed \(in megahertz\) of the CPU that is used by the configuration item.

</td></tr><tr><td>

Purchased

</td><td>

Number of rights that you have purchased.

</td></tr><tr><td>

Operating System

</td><td>

Operating system of the configuration item.

</td></tr><tr><td class="sub-head" colspan="2">

Options related list**Note:** This related list appears only when the software model for the required license is associated with an Oracle Database option or management pack.

</td></tr><tr><td>

Instance

</td><td>

Database instance that accesses and manages data that is related to your Oracle Database option or management pack.

</td></tr><tr><td>

Option

</td><td>

Oracle Database option or management pack that is installed on your configuration item.

</td></tr><tr><td>

Licensable

</td><td>

Value that indicates whether the Oracle Database option or management pack is licensable. If the option or management pack is licensable, the value is automatically set to **true**. If the option or management pack is not licensable, the value is automatically set to **false**.

</td></tr><tr><td>

Currently used

</td><td>

Value that indicates whether the Oracle Database option or management pack has current or past usage. If the option or management pack has any current or past usage, the value is automatically set to **In Use**. If the option or management pack does not have any current or past usage, the value is automatically set to **Not In Use**.

</td></tr><tr><td>

First usage date

</td><td>

Date on which you first started using the Oracle Database option or management pack.

</td></tr><tr><td>

Last usage date

</td><td>

Date on which you last used the Oracle Database option or management pack.

</td></tr><tr><td class="sub-head" colspan="2">

Installs related list**Note:** This related list appears only when the software model for the required license is associated with an Oracle Database software installation.

</td></tr><tr><td>

Display name

</td><td>

Name of the Oracle Database software installation.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the installed software. This field is always set to **Oracle**.

</td></tr><tr><td>

Version

</td><td>

Oracle Database version that is installed on your configuration item.

</td></tr><tr><td>

Discovery model

</td><td>

Discovery model that is associated with the Oracle Database software installation.

</td></tr><tr><td>

Installed on

</td><td>

Configuration item that the Oracle Database software is installed on.

</td></tr><tr><td>

Assigned to

</td><td>

User that is associated with the Oracle Database software installation.

</td></tr><tr><td class="sub-head" colspan="2">

Instances related list**Note:** This related list appears only when the software model for the required license is associated with an Oracle Database software installation.

</td></tr><tr><td>

Name

</td><td>

Name of the database instance that accesses and manages the data in your Oracle database.

</td></tr><tr><td>

Environment

</td><td>

Environment that the database instance resides in.

</td></tr><tr><td>

Version

</td><td>

Version of the database that the database instance accesses and manages.

</td></tr><tr><td>

Vendor

</td><td>

Vendor of the database that the database instance accesses and manages. This field is always set to **Oracle**.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management publisher pack for Oracle](../concept/oracle-publisher-pack.md)

