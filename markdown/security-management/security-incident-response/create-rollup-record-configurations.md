---
title: Step 7. Create rollup record configurations
description: Create rollup record configuration to link and unlink additional records to MSI.Writing a script for a Security Case to roll up record configuration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Rollup example use case implementation for a Security Case, Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Step 7. Create rollup record configurations

Create rollup record configuration to link and unlink additional records to MSI.

## Before you begin

Role required: admin and sn\_msi.workspace\_admin

**Note:** The system admin can create the record and MSI workspace admin can update it.

To rollup information such as configuration items, observables, and indicator of compromise related to a Security case, create a rollup record configuration.

## Procedure

1.  Navigate to **Major Security Incident Response** &gt; **Linked Records Configuration**.

    The Linked Record Configurations page displays.

2.  Select or create a new linked record and navigate to the **Rollup Record Configuration** section from the same page.

    ![Rollup record configuration](../image/roll-up-record-config.png "Rollup Record Configuration section")


## What to do next

-   For more detailed information, see [Configure Rollup Records in Major Security Incident Management](../concept/roll-up-record-configuration-in-major-security-incident-management.md)
-   For a security case example information, see[Writing script for a Security Case](create-rollup-record-configurations.md#)

**Parent Topic:**[Rollup example use case implementation for a Security Case](../concept/use-case-for-a-security-case.md)

## Writing script for a Security Case

Writing a script for a Security Case to roll up record configuration.

### Before you begin

Role required: admin and sn\_msi.workspace\_admin

**Note:** The system admin can create the record and MSI workspace admin can update it.

### Procedure

1.  Search for the Linked Record configurations using the left navigation.

2.  Navigate to **MSI Administration** &gt; **Linked Record Configuration**.

3.  Open the configuration record which was created for a security case.

4.  The Rollup Record configuration will be displayed in the Related List section.

5.  Click **New** to create a new roll up record configuration.

    Below is an example record created to Rollup Observables data related to Security Case we are trying to Rollup with the field values as:

<table id="table_fd3_qtc_35b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roll up Type

</td><td>

Relationship**Note:** The observable information is available in a related list format.

</td></tr><tr><td>

Rollup Script

</td><td>

Input sourceSysId contains security case sys id and msiSysId contains major security incident sys id.![Rollup script](../image/rollup-script-step7.png)

 -   ```
Line 2: As a first step, query for Glide Record for sourceSysId from **Security Case\(sn\_ti\_case\)** table.
```

-   ```
Line 7: Next, query **sn\_ti\_m2m\_task\_observable** table using security case sys ID to figure out all the linked observables to a security case.
```

-   ```
Line 10: Next, iterate over all the linked observables and link them to a Major Security Incident using the method:
```

MSIMRollupEngine.linkToMSI\("entityGr”, “sourceSysId”, “fieldNameInLinkedRecordTable”, “msiSysId”, “isPrimaryRecord”\)

</td></tr></tbody>
</table>
