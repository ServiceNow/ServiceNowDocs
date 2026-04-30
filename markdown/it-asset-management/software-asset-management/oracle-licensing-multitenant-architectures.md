---
title: Oracle Database licensing in multitenant architectures
description: The Software Asset Management application supports licensing rules for Oracle databases in multitenant architectures.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Database licensing in multitenant architectures

The Software Asset Management application supports licensing rules for Oracle databases in multitenant architectures.

The Oracle multitenant architecture simplifies database management by enabling you to consolidate multiple pluggable databases \(PDBs\) into a single container database \(CDB\). With a CDB, you can track, provision, clone, manage resources for, and upgrade multiple PDBs simultaneously. This multitenant architecture is supported on Oracle Database version 12c Release 1 \(12.1\) and later.

To run an Oracle database in a multitenant architecture, you must purchase and manage licenses for both Oracle Database and the Oracle Multitenant option. In most cases, Oracle Multitenant option licenses must be purchased and managed separately from Oracle Database licenses. However, Oracle Database Cloud Service Enterprise Edition - High Performance \(DBCS EE-HP\), Oracle Database Cloud Service Enterprise Edition - Extreme Performance \(DBCS EE-EP\), and Oracle Database Exadata Cloud Service \(ExaCS\) do not require a separate license for the Oracle Multitenant option, as it is already included in the database license. For more information on Oracle Database licensing, see [Software Asset Management publisher pack for Oracle](oracle-publisher-pack.md).

## Oracle Multitenant option licensing

The Oracle Multitenant option supports both the Named User Plus and Per Processor license metrics. The Named User Plus license metric licenses all users and physical devices that access a user-created PDB. The Per Processor license metric licenses the processor cores on all physical hosts that are running a user-created PDB. For more information on these license metrics, see [Oracle license metrics](oracle-publisher-pack.md#section_q2j_3dn_qpb).

**Important:** Oracle Multitenant option licensing accounts for user-created PDBs only. It does not account for proxy PDBs or seed PDBs.

You can determine whether Oracle Multitenant option licensing is required for your database deployment based on the following criteria:

-   The Oracle Database version and edition of your PDBs and CDBs.
-   The number of user-created PDBs within each database instance that is running on the database installation.

<table id="table_ck2_wy5_vrb"><thead><tr><th>

Oracle Database version

</th><th>

Oracle Database edition

</th><th>

Licensing requirement

</th></tr></thead><tbody><tr><td rowspan="4">

12c Release 1 \(12.1\)

</td><td>

Oracle Database Standard Edition \(SE\)

</td><td rowspan="3">

The Oracle Multitenant option is not supported.

</td></tr><tr><td>

Oracle Database Standard Edition One \(SE1\)

</td></tr><tr><td>

Oracle Database Standard Edition 2 \(SE2\)

</td></tr><tr><td>

Oracle Database Enterprise Edition \(EE\)

</td><td>

-   If every database instance contains only one user-created PDB each, licensing is not required since the Oracle Multitenant option is not in use.
-   If any database instance contains more than one user-created PDB, licensing is required using either the Named User Plus or Per Processor license metric.

**Important:** This version and edition of Oracle Database supports up to 252 user-created PDBs per database instance. If a database instance contains more than 252 user-created PDBs, Software Asset Management creates removal candidates for the additional PDBs. You must remove the additional PDBs to maintain compliance.


</td></tr><tr><td rowspan="5">

12c Release 2 \(12.2\) and 18c

</td><td>

Oracle Database Enterprise Edition \(EE\)

</td><td>

-   If every database instance contains only one user-created PDB each, licensing is not required since the Oracle Multitenant option is not in use.
-   If any database instance contains more than one user-created PDB, licensing is required using either the Named User Plus or Per Processor license metric.

**Important:** This version and edition of Oracle Database supports up to 252 user-created PDBs per database instance. If a database instance contains more than 252 user-created PDBs, Software Asset Management creates removal candidates for the additional PDBs. You must remove the additional PDBs to maintain compliance.


</td></tr><tr><td>

Oracle Database Standard Edition 2 \(SE2\)

</td><td>

The Oracle Multitenant option is supported only in deployments where every database instance contains one user-created PDB each. However, licensing is not required since the Oracle Multitenant option is not in use.

</td></tr><tr><td>

Oracle Database Cloud Service Enterprise Edition - High Performance \(DBCS EE-HP\)

</td><td rowspan="3">

-   If every database instance contains one user-created PDB each, licensing is not required since the Oracle Multitenant option is not in use.
-   If any database instance contains more than one user-created PDB, the Oracle Multitenant option is in use. However, separate licensing is not required for this option since it is already included in the Oracle Database license.

**Important:** These versions and editions of Oracle Database support up to 4,096 user-created PDBs per database instance. If a database instance contains more than 4,096 user-created PDBs, Software Asset Management creates removal candidates for the additional PDBs. You must remove the additional PDBs to maintain compliance.


</td></tr><tr><td>

Oracle Database Cloud Service Enterprise Edition - Extreme Performance \(DBCS EE-EP\)

</td></tr><tr><td>

Oracle Database Exadata Cloud Service \(ExaCS\)

</td></tr><tr><td rowspan="5">

19c and later

</td><td>

Oracle Database Enterprise Edition \(EE\)

</td><td>

-   If every database instance contains three or less user-created PDBs each, licensing is not required since the Oracle Multitenant option is not in use.
-   If any database instance contains more than three user-created PDBs, licensing is required using either the Named User Plus or Per Processor license metric.

**Important:** This version and edition of Oracle Database supports up to 252 user-created PDBs per database instance. If a database instance contains more than 252 user-created PDBs, Software Asset Management creates removal candidates for the additional PDBs. You must remove the additional PDBs to maintain compliance.


</td></tr><tr><td>

Oracle Database Standard Edition 2 \(SE2\)

</td><td>

The Oracle Multitenant option is supported only in deployments where every database instance contains three or less user-created PDBs each. However, licensing is not required since the Oracle Multitenant option is not in use.

</td></tr><tr><td>

Oracle Database Cloud Service Enterprise Edition - High Performance \(DBCS EE-HP\)

</td><td rowspan="3">

-   If every database instance contains three or less user-created PDBs each, licensing is not required since the Oracle Multitenant option is not in use.
-   If any database instance contains more than three user-created PDBs, the Oracle Multitenant option is in use. However, separate licensing is not required for this option since it is already included in the Oracle Database license.

**Important:** These versions and editions of Oracle Database support up to 4,096 user-created PDBs per database instance. If a database instance contains more than 4,096 user-created PDBs, Software Asset Management creates removal candidates for the additional PDBs. You must remove the additional PDBs to maintain compliance.


</td></tr><tr><td>

Oracle Database Cloud Service Enterprise Edition - Extreme Performance \(DBCS EE-EP\)

</td></tr><tr><td>

Oracle Database Exadata Cloud Service \(ExaCS\)

</td></tr></tbody>
</table>-   **[Oracle Multitenant option use cases](oracle-multitenant-use-cases.md)**  
You can view the following use cases to better understand licensing requirements for the Oracle Multitenant option.

**Parent Topic:**[Software Asset Management publisher pack for Oracle](oracle-publisher-pack.md)

