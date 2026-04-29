---
title: NIST CSF tables
description: A few tables are impacted by the NIST CSF guidance.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [NIST CSF Use Case Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# NIST CSF tables

A few tables are impacted by the NIST CSF guidance.

|Table|Purpose|
|-----|-------|
|Target \[sn\_grc\_target\]|Target is a core table of design to be shared component among the ServiceNow GRC application and GRC use-case content packs.Target is like entity in its purpose, but is used to track any attributes specific to use-case content packs. No two target records can reference the same entity at any time.|
|NIST CSF Activity \[sn\_irm\_nist\_csf\_nist\_csf\_activity\]|NIST CSF Activity table is used to track cybersecurity activity relevant for a target. The activity also helps in performing gap analysis that identifies the gaps, non-complaint controls, risks, issues, failed indicators and action plans for a cybersecurity activity.|
|Gaps \[sn\_irm\_nist\_csf\_m2m\_policy\_state\_nist\_csf\_act\]|Gaps table in NIST CSF is used to track control objectives that aren’t yet implemented as gaps. This table comes handy for reporting and drill down purposes. It's an m2m table that associates Gaps to Targets.|
|Non-compliant Control \[sn\_irm\_nist\_csf\_m2m\_cxontrols\_nist\_csf\_act\]|Non-compliant Control table in NIST CSF is used to track controls that are identified as non-compliant. Only cybersecurity control objectives as defined by the framework core which are implemented as controls and non-compliant are tracked. This table comes handy for reporting and drill down purposes. It's an m2m table that associates Non-compliant Controls to Targets.|
|Risk \[sn\_irm\_nist\_csf\_m2m\_risks\_nist\_csf\_activities\]|Risk table in NIST CSF is used to track risks that are associated with controls that have been implemented for cybersecurity control objectives as defined by the framework core. This table comes handy for reporting and drill down purposes. It's an m2m table that associates Risks to Targets.|
|Issue \[sn\_irm\_nist\_csf\_m2m\_issues\_nist\_csf\_act\]|Issue table in NIST CSF is used to track issues that are associated with controls that have been implemented for cybersecurity control objectives as defined by the framework core. Issues of risks associated with these controls are also included in the metric. This table comes handy for reporting and drill down purposes. It's an m2m table that associates Issues to Targets.|
|Action Plan \[sn\_irm\_nist\_csf\_m2m\_remediation\_nist\_csf\_act\]|Action Plan table in NIST CSF is used to track the action plans that are identified for the issues. This table comes handy for reporting and drill down purposes. It's an m2m table that associates Action Plans \(remediation tasks\) to Targets.|
|Failed Indicators \[sn\_irm\_nist\_csf\_m2m\_indicators\_nist\_csf\_act\]|Failed indicators table in NIST CSF is used to track the failed indicators of the target and the control or risk. This table comes handy for reporting and drill down purposes. It's an m2m table that associates Failed Indicators to Targets.|
|Related Control Objectives \[sn\_compliance\_m2m\_policy\_stmt\_policy\_stmt\]|Related Control Objectives table in NIST CSF is used to track the associations between control objectives. In base implementation, parent and child control objectives are supported, but this table introduces a concept to relate the control objectives at the same level.|

**Parent Topic:**[NIST CSF Use Case Accelerator](../concept/grc-csf-usecase-accelerator.md)

