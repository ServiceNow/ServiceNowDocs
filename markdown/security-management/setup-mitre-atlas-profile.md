---
title: Activate the MITRE ATLAS framework
description: Activate the MITRE ATLAS profile to ingest MITRE ATLAS data for threat detection in AI and machine learning systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/setup-mitre-atlas-profile.html
release: zurich
topic_type: task
last_updated: "2026-08-05"
reading_time_minutes: 1
breadcrumb: [MITRE ATLAS framework, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Activate the MITRE ATLAS framework

Activate the MITRE ATLAS profile to ingest MITRE ATLAS data for threat detection in AI and machine learning systems.

## Before you begin

Role required: sn\_ti.admin

## About this task

STIX™ \(Structured Threat Information Expression\) is a language for describing cyberthreat information in a standardized and structured manner. Using STIX data and Trusted Automated Exchange of Indicator Information \(TAXII™\) profiles, security teams can share cyberthreat information. This helps isolate threats already identified by your company or by other sources.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Sources** &gt; **TAXII Profiles**.

    You see the available TAXII profiles.\[Omitted image "mitre-atlas-home.png"\] Alt text: MITRE ATLAS - TAXII collection

2.  Select the MITRE ATLAS profile.

    The MITRE ATLAS profile provides only one TAXII collection, ATLAS.

    The ATLAS collection describes adversarial tactics and techniques used against AI and machine learning systems.

3.  In the **TAXII Collections** related list, select **ATLAS** to open the collection record.

    \[Omitted image "mitre-atlas-taxii-collection.png"\] Alt text: MITRE ATLAS Schedule tab

4.  Select the **Active** check box to activate the collection.

    The **Active** check box controls whether the collection imports and refreshes data on a scheduled basis.

    -   On: The collection imports and refreshes MITRE data on a scheduled basis.
    -   Off: Data is refreshed only when an import is manually triggered.
    **Note:** The MITRE ATLAS collection is configured to operate in on-demand mode by default, with automatic refresh turned off. Enabling the MITRE ATLAS collection makes the ATLAS heatmap available.

5.  In the **Schedule** tab, review the **Run** field.

    The **Run** field provides no scheduling choice for the ATLAS collection. **On Demand** is the only mode.

    To refresh the data, select **Execute Now**.


## What to do next

After the TAXII profile setup is complete, the MITRE ATLAS repository data is imported to the ServiceNow AI Platform®. You can see this data by navigating to **MITRE ATLAS Repository** &gt; **Matrices** and **MITRE ATLAS Repository** &gt; **Techniques**.

