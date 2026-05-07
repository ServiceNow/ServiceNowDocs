---
title: Configure Rollup Records in Major Security Incident Management
description: Configure Roll up records in Major Security Incident Management to control the information, which will be rolled up when the source record is linked/proposed/promoted as Major Security Incidents.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Rollup Records in Major Security Incident Management

Configure Roll up records in Major Security Incident Management to control the information, which will be rolled up when the source record is linked/proposed/promoted as Major Security Incidents.

Role required: admin and sn\_msi.workspace\_admin.

**Note:** The system admin can create the record and MSI workspace admin can update it.

**Procedure**

1.  Navigate to **Major Security Incident Response** &gt; **Linked Records Configuration**. The Linked Record Configurations page displays.
2.  Select or create a new linked record and navigate to the **Roll up Record Configuration** section from the same page.

    ![Rollup record configuration](../image/roll-up-record-config.png "Rollup Record Configuration section")

3.  Select **New**.

    ![Rollup record configuration page](../image/roll-up-record-config-page.png)

4.  On the configuration page, fill the details.

<table id="table_sbs_d1v_h5b"><thead><tr><th>

Field Name

</th><th>

Field Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Indicates the name of the rolling up record.

</td></tr><tr><td>

Active

</td><td>

Select this check box to implement the current configuration when rollup of source record happens.

</td></tr><tr><td>

Linked Record Configuration

</td><td>

Indicates a unique number, which refers to your parent linked records configuration and read-only.

</td></tr><tr><td>

Source Table

</td><td>

The source table name used in the Linked Record configuration, which is read-only.

</td></tr><tr><td>

Rollup Type

</td><td>

Describes the type of information which should be rolled up.-   **Relationship**: Select this option if the data need to be present as a related list.
-   **Reference**: Select this option if the data is present as a reference field on the source table form.


</td></tr><tr><td>

Rollup Script

</td><td>

If the rollup type is: **Relationship**, then the **Rollup Script** field is enabled, which allows you to write script and can be used to rollup information. Here the script will receive the inputs which contains information of the source record and major security incident. The script should be able to find the information from the relationship tables and rollup to Linked Record \(sn\_msi\_m2m\_child\) table.

</td></tr><tr><td>

Source Field

</td><td>

If the rollup type is: **Reference**, then the **Source Field** is available. This enables you to select the Source Table reference field which contains the information that needed to be rolled up.

</td></tr><tr><td>

Target Field

</td><td>

If the rollup type is: **Reference**, then the **Target Field** is available. This enables you to reference field from the Linked Record\(sn\_msi\_m2m\_child\) table and will store the data which is present in the selected Source Field and in the Source Table record.

</td></tr></tbody>
</table>
**Writing script for rollup**

<table id="table_zmh_yjc_35b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

-   sourceSysId: Sys ID of source table record which is either getting linked / proposed / promoted.
-   msiSysId: Sys ID of major security incident to which source record is getting linked / proposed / promoted.

</td></tr><tr><td>

Output

</td><td>

No output return value.

</td></tr><tr><td>

Responsibility

</td><td>

Script should rollup information to Linked Record\(sn\_msi\_m2m\_child\) table.-   Use sourceSysID to query data from ServiceNow relationship tables.
-   After the data is fetched, roll up the data to a Linked Record \(sn\_msi\_m2m\_child\) using MSIRollupEngine utility to roll up data.

</td></tr></tbody>
</table>**Parent Topic:**[Rollup Framework for MSIM](roll-up-framework-for-major-security-incident-management.md)

**Related topics**  


[Configure Linked Records in Major Security Incident Management](../task/configuring-linked-records-in-major-security-incident-management.md)

[Configure List Layout in Major Security Incident Management](list-layout-confguration.md)

[Rollup example use case implementation for a Security Case](use-case-for-a-security-case.md)

[Perform on demand atomic rollup](perform-on-demand-atomic-rollup.md)

