---
title: Create and map detection rules
description: Create detection rules and map them against the tactics and techniques. With this mapping, you can see the coverage for the detection rules in your organization.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create and map detection rules

Create detection rules and map them against the tactics and techniques. With this mapping, you can see the coverage for the detection rules in your organization.

## Before you begin

Role required:

-   sn\_ti.admin, sn\_si.admin: create, write, delete access
-   sn\_ti.read: read access

## About this task

Detection rule mapping enables your organization to see which detection rules are available to identify specific techniques.

The primary purpose of the mapping is to provide visibility if your organization has the necessary detection rules to identify when an alert or event is triggered as a result of an attack by an adversary using a specific technique.

For example, view the following illustration that shows a list of the detection rules mapped to various techniques. You can also view this information in [the MITRE-ATT&amp;CK navigator](../concept/mitre-att-ck-heatmap-and-navigator.md#).

![MITRE ATT&CK detection rules.](../image/mitre-detection-rules.png)

If you do not intend to use the base system SIEM auto-extraction rules, then enable the automatic rollup of MITRE-ATT&amp;CK TTPs based on the detection rule mapping. You can populate the alert or event rule that triggers the security incident in the Alert Rule name field. You can also populate the Alert Rule name field by using SIEM integration, email parsing, manual creation, etc. For more information, see [Rollup MITRE-ATT&amp;CK information from detection rules](rollup-mitre-attack-information-detection-rules.md).

**Note:**

The detection rules feature has been updated to include mapping a single tactic to multiple techniques. Previously, you could map a single tactic with a single technique. If you are upgrading the Threat Intelligence plugin from version 12.0.4 to a higher version, then review the following points before using the detection rules in MITRE-ATT&amp;CK module.

-   You find multiple records merged into a single record if the fields - rule name, alert sensor, source, category, subcategory, and MITRE-ATT&amp;CK tactic are common.
-   The old records are marked as true in the deprecated column and false in the active column.
-   The new merged records are available for use and are marked as false in the deprecated column and true in the active column.
-   After you verify the upgrade, and view that all your detection rules are successfully migrated, you can delete the old records that are marked as true in the deprecated column.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Detection Rules - MITRE ATT&amp;CK Mappings**.

2.  Use one of the following methods to create your detection rule:

    Method 1: Manually create detection rules.

    1.  Click **New** and on the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Rule Name|Detection rule's name.|
        |MITRE-ATT&amp;CK Tactic|Relevant MITRE-ATT&amp;CK tactic.|
        |MITRE-ATT&amp;CK Techniques|Relevant MITRE-ATT&amp;CK technique. You can select multiple techniques for a single tactic.|
        |Source|Source of the security incident, such as email, firewall, network monitoring, and so on.|
        |Alert Sensor|Security integration through which you ingest the alert or event data such as CarbonBlack, CrowdStrike, McAfee, and so on.|
        |Subcategory|Subcategory that further defines the issue.|
        |Category|Category that identifies the type of security issue.|
        |MITRE-ATT&amp;CK Technique|Relevant MITRE-ATT&amp;CK technique. You can select multiple techniques for a single tactic.|
        |Security Incident Count|The number of security incidents that the techniques are appended to. This count appears when you have enabled the roll up of MITRE-ATT&amp;CK information automatically from alert rules to security incidents.|
        |Deprecated|The detection rule mapping is deprecated.|
        |Active|Option to specify if the detection rule is active and deployed in your environment.|

        ![Detection Rules example.](../image/mitre-detection-rules-example.png)

    2.  Click **Submit**.
    Method 2: Import and create detection rules.

    1.  Right-click the Rule Name column header.
    2.  From the list, click **Import**.
    3.  Click **Create Excel template**.
    4.  Click **Download** after the export completes. An excel template with the filename sn\_ti\_alert\_rules\_mitre\_attack\_technique\_mapping is downloaded to your computer.

        In the following illustration, you see how to export the excel template, fill the details in the spreadsheet, upload the file, preview the fields, and import it back to the ServiceNow AI Platform.

        ![MITRE download import template.](../image/mitre-import-download.gif)

    5.  Open the spreadsheet, select the second sheet tab, and review what you entered. On the form, fill in the fields and then, save your file.

        |Field|Description|
        |-----|-----------|
        |Rule Name|Detection rule name.|
        |Active|Option to specify if the detection rule is active and deployed in your environment.|
        |Alert Sensor|Security integration through which you ingest the alert or event data such as CarbonBlack, CrowdStrike, McAfee, and so on.|
        |Category|Category that identifies the type of security issue.|
        |Comments|Description about the detection rule.|
        |Deprecated|The detection rule mapping is deprecated.|
        |MITRE-ATT&amp;CK Technique IDs|MITRE-ATT&amp;CK technique ID, such as T1546.008, for Accessibility Features.|
        |MITRE-ATT&amp;CK Tactic ID|MITRE-ATT&amp;CK tactic ID, such as TA0003, for Persistence.|
        |Security Incident Count|The number of security incidents that the techniques are appended to. This count appears when you have enabled the roll up of MITRE-ATT&amp;CK information automatically from alert rules to security incidents and the detection rule is active.|
        |Source|Source of the security incident, such as email, firewall, network monitoring, and so on.|
        |Subcategory|Subcategory that further defines the issue.|
        |MITRE-ATT&amp;CK Tactic|Relevant MITRE-ATT&amp;CK tactic.|
        |MITRE-ATT&amp;CK Technique|Relevant MITRE-ATT&amp;CK technique.|

        The following illustration shows the spreadsheet template. The required fields are highlighted in red - Rule Name, MITRE-ATT&amp;CK Tactic ID, and MITRE-ATT&amp;CK Technique ID.

        ![Update the mapping details in the spreadsheet template.](../image/mitre-rules-mapping-excel.png)

    6.  Click **Choose file** and select the spreadsheet on your computer.
    7.  Click **Upload**.
    8.  Click **Preview Imported Data**.
    9.  Preview the mappings and click **Complete Import**.

        The following illustration shows how to upload the spreadsheet, preview the data, review any errors, and complete the detection rule mapping import process.

        ![Upload the spreadsheet to complete the detection rule mapping.](../image/mitre-import-upload.gif)


**Parent Topic:**[MITRE-ATT&amp;CK administration](../concept/mitre-att-ck-administration.md)

**Related topics**  


[Get started with MITRE-ATT&amp;CK framework](../reference/get-started-with-mitre.md)

[Understand the MITRE to STIX data model](../reference/understand-the-mitre-to-stix-data-model-mapping.md)

[Domain separation and MITRE-ATT&amp;CK](../reference/domain-separation-and-mitre-att-ck.md)

[Set up the MITRE-ATT&amp;CK framework](setup-mitre-profile.md)

[Manage matrices](view-mitre-collection.md)

[Manage techniques](view-techniques.md)

[Manage mitigations](manage-mitigations.md)

[Manage groups](manage-groups-threat-intel.md)

[Manage malware](manage-malware.md)

[Manage tools](manage-tools.md)

[Manage MITRE relationships](manage-mitre-relationships.md)

[Manage CVE and technique mapping](manage-cve-and-technique-mapping.md)

[Extend the MITRE-ATT&amp;CK data](view-and-extend-information.md)

[Define the data source and detection tool mapping](manage-mitre-att-ck-data-sources.md)

[Define the data source and data component mapping](map-the-data-source-and-data-components.md)

[Define the technique detection coverage](define-technique-coverage.md)

[Map your technique detection coverage to a technique](map-technique-coverage.md)

[Define the mitigation coverage](define-the-mitigation-coverage.md)

[Map your mitigation coverage to a technique](map-your-mitigation-coverage-to-a-technique.md)

[Auto-extract technique rules for importing MITRE-ATT&amp;CK information](../concept/auto-extract-technique-rules.md#)

[Review threat group and MITRE-ATT&amp;CK techniques mapping](review-threat-group-and-techniques-mapping.md)

[Threat group to technique heatmap definition](threat-group-to-technique-heatmap-definition.md)

[Review the MITRE-ATT&amp;CK system properties](configure-mitre-att-ck-properties.md)

