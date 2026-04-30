---
title: Severity mapping for Unified Security Exposure Management
description: Severity mapping is a critical feature that enables organizations to standardize and normalize the severity levels of findings detected across different sources. This process involves mapping the severity levels from various scanners and sources to a common severity scale used within Unified Security Exposure Management.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Severity mapping for Unified Security Exposure Management

Severity mapping is a critical feature that enables organizations to standardize and normalize the severity levels of findings detected across different sources. This process involves mapping the severity levels from various scanners and sources to a common severity scale used within Unified Security Exposure Management.

## Severity Mapping

**Note:** Business rules run in the background to evaluate the priority for Qualys data and perform the corresponding mapping to the **Priority** field. Therefore, the business rule is responsible for handling the mapping of Qualys data.

<table id="table_hwk_krm_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Normalised\_Severity

</td><td>

Calculates the severity values received from the scanner.

</td></tr><tr><td>

Source\_severity

</td><td>

-   Data from the severity\_score table is mapped to the source\_severity table during the execution of the **Rapid7 Vulnerability Integration- API.**
-   Data from the SEVERITY\_LEVEL is mapped to the source\_severity table during the execution of the **Qualys Knowledge Base Integration**.
-   Data for risk\_factor table is mapped to source\_severity during the execution of the **Tenable.io Plugin Integration**.
-   Data for riskFactor table is mapped to source\_severity during the execution of the **Tenable.io Plugin Integration**.
-   Data from severity table is mapped to source\_severity during the execution of the **Microsoft TVM Vulnerability\(CVE\) Integration**.

.

</td></tr></tbody>
</table>**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configure a severity map in the Security Exposure Management Workspace](../task/sem-configure-severity-map.md)

