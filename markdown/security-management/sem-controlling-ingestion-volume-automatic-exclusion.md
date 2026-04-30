---
title: Controlling the ingestion volume with automatic exclusion
description: Exclusion rules provide a way to filter or exclude detections from getting converted into VITs during the ingestion process in Vulnerability Response.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Controlling the ingestion volume with automatic exclusion

Exclusion rules provide a way to filter or exclude detections from getting converted into VITs during the ingestion process in Vulnerability Response.

These rules can be set up to handle various scenarios such as:

-   Excluding vulnerabilities with low severity or risk that don’t require immediate remediation.
-   Improving the remediation process by prioritizing the most critical VITs for action.
-   Reducing the processing time during data import by excluding a percentage of detections from VITs conversion.

During the process of ingesting data, there are distinct approaches for handling new and existing detections.

-   For new detections:
    -   If a new detection doesn't meet the conditions of an exclusion rule, a detection is created with the VITs.
    -   If a new detection meets the conditions of an exclusion rule, the rule gets associated with the detection, but a finding isn’t created. Populate the matching Exclusion Rule reference on the Detection record​. The Exclusion rule column is populated with Exclusion Rule reference on the Detection record accordingly.
-   For existing detections:
    -   If the detection doesn't meet the conditions of any exclusion rule, it proceeds with the normal workflow.
    -   If an existing detection matches the conditions of an exclusion rule, the finding associated with that detection stays in its current state but the rule gets associated with the detection. The state of the finding is governed by the value defined in the **sn\_vul.close\_vit\_with\_excluded\_detections** property. By default, the value in this property is set to False. If the value is set to False, then the detections under a finding get excluded and the state of the VITs stays in its current state. However, if the value is set to True, the following scenarios may occur:
        -   If every detection under a finding is excluded, the finding's status is updated to Closed Excluded.
        -   If one detection is marked as Closed while the remaining are excluded, the finding is designated as Closed Fixed.
        -   If the finding has open detections, then the finding remains Open.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring exclusion rules](sem-configure-exclusion-rules.md)

