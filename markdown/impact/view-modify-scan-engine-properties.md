---
title: View and modify Scan Engine definitions
description: You can modify an existing definition to further customize and refine its scanning criteria.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scan Engine definitions, Scan Engine, Platform Health, Using Impact, Impact]
---

# View and modify Scan Engine definitions

You can modify an existing definition to further customize and refine its scanning criteria.

## Before you begin

Role required: Scan Engine admin \(`sn_se.scan_engine_admin`\) .

While only Scan Engine admins can modify definitions, any user with the Scan Engine user role can view them.

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definitions**.

2.  Select a definition number to open its details.

3.  To modify a base system definition’s properties, select **Override Definition**.

    When a definition is overridden, the base system definition will no longer be used in any scan \(real-time, scheduled, update set, application, or on demand\). All fields in the overridden definition become editable.

4.  Modify the required and optional fields.

    -   Refer to [Create custom Scan Engine definitions](create-scan-engine-definitions.md#) for details.
    -   In addition to those fields, when viewing an existing definition, you will also see **Override**. To modify a base system definition, use the override field to disable it and create a new custom definition.
    The definition is overridden to create the current definition.

    This field is only visible if a base definition has been overridden using **Override Definition**. Deleting an overridden definition re-enables the base system definition.

    **Note:** Overridden definitions are considered custom definitions. As a result, they are included in the count of 10 active custom definitions limit for Guided customers.

5.  Select **Update**.

    Selecting Delete will delete the override, meaning the base system definition will be used going forward.

    Related lists appear at the bottom of the definition screen.

<table id="choicetable_fkk_pkx_2hc"><tbody><tr><td id="d52620e153">

**Applicable Tables**

</td><td>

Displays all tables scanned by the definition, as well as the conditions table records must match in order to be scanned.To add a table to the list:

1.  Select **New**.
2.  In the New Applicable Table form, define the potential tables to scan:
    -   **Definition**: The definition that applies to this record. For the table defined in this record, if the condition matches, the definition in this field will record a finding.
    -   **Table**: Specific table that the definition runs against.
        -   **Configuration tables**: Definitions run against tables that extend the application file \(sys\_metadata\). Scans of these tables can be monitored in real time.
        -   **Non-configuration tables**: Definitions run against all other tables. Scans of these tables cannot be monitored in real time and will only be seen in the results of an update set, application, or other on-demand scan.
    -   **Global Scope**: Some global tables have a type of restricted access, called Caller Restriction. Special handling is required to access these tables from the Scan Engine scope.

See [Restricted Caller Access](https://www.servicenow.com/docs/csh?topicname=restricted-caller-access-privilege.html&version=latest) for more information.

    -   **Conditions**: Defines the conditions that table records must meet in order to be scanned.


</td></tr><tr><td id="d52620e218">

**Findings For This Definition**

</td><td>

Displays any findings, as established by the definition, found during on-demand or scheduled scans.

</td></tr><tr><td id="d52620e227">

**Resolved Finding Histories**

</td><td>

Shows findings that were resolved for this definition.

</td></tr><tr><td id="d52620e236">

**Scan Engine Suites**

</td><td>

Displays all suites assigned to the definition, which allows for scanning entire suites of definitions. Suites are also used in reporting within the Analytics Dashboard. For more information, see [Create Scan Engine definition suites](create-scan-engine-definition-suites.md#). To assign suites to a definition:

1.  Select **Edit**.
2.  In the **Edit Members** form, assign one or more suites to a definition:
    -   **Collection**: List of available suites that can be assigned to a definition.
    -   **Scan Engine Suites List**: Assigned suites for the current definition.


</td></tr></tbody>
</table>
