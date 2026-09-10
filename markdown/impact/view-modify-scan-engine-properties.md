---
title: Customize Scan Engine definitions
description: You can modify an existing definition to further customize and refine its scanning criteria or deactivate a definition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/view-modify-scan-engine-properties.html
release: australia
topic_type: task
last_updated: "2026-08-21"
reading_time_minutes: 4
keywords: [scan engine definitions, customize, active, override]
breadcrumb: [Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Customize Scan Engine definitions

You can modify an existing definition to further customize and refine its scanning criteria or deactivate a definition.

## Pre-defined definitions

There are various types of definitions available as a baseline in the Impact Scan Engine.

|Category|Description|
|--------|-----------|
|Security|Measures implementation of protocols across a ServiceNow instance to prevent unauthorized access, data breaches, cyber attacks, and potential vulnerabilities.|
|Performance|Measures the efficiency of a ServiceNow instance, encompassing aspects such as speed, responsiveness, resource utilization, and overall dependability.|
|Manageability|Measures the extent to which ServiceNow instances, applications, or infrastructure can be effectively monitored, configured, and maintained.|
|Upgradeability|Assesses the ease of enhancing a ServiceNow instance or application with new features, improvements, security patches, or compatibility adjustments.|
|User Experience|Evaluates the quality of user interactions with applications. Considers the ease of use, efficiency, design, responsiveness, accessibility, and its emotional and functional impact.|

For more information, see [Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md).

## Before you begin

A list of specific Scan Engine definitions are available in your instance and vary based on instance setup.

Scan Engine admins can toggle the Active field on any definition without using the override function. To modify other definition properties, you must use the Override Definition option. Any user with the Scan Engine user role can view definitions.

Role required: Scan Engine admin \(`sn_se.scan_engine_admin`\).

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Definitions**.

2.  Select a definition number to open its details.

3.  Deactivate a definition
4.  To deactivate a definition without requiring an approval override, deselect the **Active** checkbox.

    The Active field is editable without requiring an override. This field deactivates the definition so it will no longer run in any scan type. No other changes to the definition are needed.

    **Note:** Minimum versions required are Scan Engine version 4.0.3 \(Zurich 11\) or Australia AP5.

5.  Modify definition properties
6.  To modify other definition properties, select **Override Definition**.

    When a definition is overridden, the base system definition will no longer be used in any scan type \(real-time, scheduled, update set, application, or on demand\). All fields in the overridden definition become editable. You can then modify the required and optional fields. Refer to [Create custom Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definitions.md) for complete field details.

7.  When updating an overridden definition, review the override field information.

    -   The **Override** field is only visible if a base definition has been overridden using **Override Definition**.
    -   Deleting an overridden definition re-enables the base system definition.
    -   Overridden definitions are considered custom definitions. As a result, they are included in the count of 10 active custom definitions limit for Guided customers.
8.  Select **Update**.

    Related lists appear at the bottom of the definition screen.

<table id="choicetable_fkk_pkx_2hc"><tbody><tr><td id="d55729e288">

**Applicable Tables**

</td><td>

Displays all tables scanned by the definition, as well as the conditions table records must match to be scanned.To add a table to the list:

1.  Select **New**.
2.  In the New Applicable Table form, define the potential tables to scan:
    -   **Definition**: The definition that applies to this record. For the table defined in this record, if the condition matches, the definition in this field will record a finding.
    -   **Table**: Specific table that the definition runs against.
        -   **Configuration tables**: Definitions run against tables that extend the application file \(sys\_metadata\). Scans of these tables can be monitored in real time.
        -   **Non-configuration tables**: Definitions run against all other tables. Scans of these tables cannot be monitored in real time and will only be seen in the results of an update set, application, or other on-demand scan.
    -   **Global Scope**: Some global tables have a type of restricted access, called Caller Restriction. Special handling is required to access these tables from the Scan Engine scope.

See [Restricted Caller Access](https://www.servicenow.com/docs/access?context=restricted-caller-access-privilege) for more information.

    -   **Conditions**: Defines the conditions that table records must meet to be scanned.


</td></tr><tr><td id="d55729e353">

**Findings For This Definition**

</td><td>

Displays any findings, as established by the definition, found during on-demand or scheduled scans.

</td></tr><tr><td id="d55729e362">

**Resolved Finding Histories**

</td><td>

Shows findings that were resolved for this definition.

</td></tr><tr><td id="d55729e371">

**Scan Engine Suites**

</td><td>

Displays all suites assigned to the definition, which allows for scanning entire suites of definitions. Suites are also used in reporting within the Analytics Dashboard. For more information, see [Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definition-suites.md). To assign suites to a definition:

1.  Select **Edit**.
2.  In the **Edit Members** form, assign one or more suites to a definition:
    -   **Collection**: List of available suites that can be assigned to a definition.
    -   **Scan Engine Suites List**: Assigned suites for the current definition.


</td></tr></tbody>
</table>
-   **[Create custom Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definitions.md)**  
The Scan Engine contains preexisting base system definitions and you can create your own.
-   **[Customize Scan Engine definition suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/create-scan-engine-definition-suites.md)**  
Follow these steps to create or modify Scan Engine definition suites.
-   **[Create policies for Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/working-policies-scan-engine.md)**  
Policies let you determine how specific definition findings appear on analytics dashboards; you can ignore them completely or place them in a prioritized view.

**Parent Topic:**[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-initial-scan-engine-settings.md)

