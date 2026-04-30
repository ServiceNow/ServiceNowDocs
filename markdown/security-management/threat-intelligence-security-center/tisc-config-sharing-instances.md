---
title: Share Threat Intelligence data between TISC instances
description: You can share threat intelligence data between TISC instances using one of the following methods.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-02-18"
reading_time_minutes: 1
breadcrumb: [Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Share Threat Intelligence data between TISC instances

You can share threat intelligence data between TISC instances using one of the following methods.

## Sharing Methods

-   **Manual sharing through the user interface \(GUI\)**: Manually curate and share intelligence records with a target instance through the TISC interface. For more information, see [Sharing of Outbound Intelligence Records from the GUI](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-create-intel-records-lib.html).
-   **Automated sharing using flows**: Configure flows to automatically share intelligence data to a target instance based on a defined condition. For more information, see [Automated Sharing of Outbound Intelligence Records](https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-automated-outbound-intel-share.html).
-   **Sharing through a TAXII server**: Exchange threat intelligence data through TAXII collections using standardized threat intelligence sharing protocols. For more information, see .

**Data transfer mechanism**

-   For Manual sharing via GUI and automated flow based sharing, the source TISC instance pushes the data directly to the target instance.
-   For TAXII based sharing, the target TISC instance pulls data from TAXII collections configured on the source instance.

**Related topics**  


[tisc-create-intel-records-lib]

[Add to TAXII Collections from Library List View](../task/tisc-obs-add-taxii-collects.md)

