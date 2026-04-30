---
title: Scan findings
description: A finding is a reference to a record that has violated a rule from a check on the instance. You can find the source record and the number of times the record triggered the rules of a given check.
locale: en-US
release: zurich
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security scanner, Security configuration console, Security Center, Platform Security]
---

# Scan findings

A finding is a reference to a record that has violated a rule from a check on the instance. You can find the source record and the number of times the record triggered the rules of a given check.

![Security scanner tab in the Security Center](../images/security-scanner.png)

Navigate to the **Findings** tab to view scan findings in a list. The cards above the list provide a count of the findings that match specific criteria listed on the card. Select any of these cards to filter the list to show only those that match the criteria.

Select the **+Create task** button to create a Security Task to resolve a finding. This button appears both on the list and within the finding record. For details on Security Tasks, see [Security Tasks](security-task-manager.md).

## Scan findings

Select a link under the **Count** column to view a finding record, which displays granular details related to a specific finding.

![Scan finding record](../images/scan-finding.png)

-   **Check**

    List of checks associated with the scan.

-   **Category**

    Security category associated with the scan. For example, access control or malicious code.

-   **Count**

    Number of times the record violated check rules.

-   **Priority**

    Severity of the security risk: 1 is highest priority while 4 is lowest.

-   **Result**

    Status and type of scan.

-   **Check Version**

    Version of the check.

-   **Source Table**

    Record that has violated a rule from the check.

-   **Mute Reason**

    Reason for muting the finding.

-   **Source**

    Date the finding was created.

-   **Task**

    Task record associated with the scan. Used to facilitate task assignments from the finding of a record.

-   **Domain**

    Which domain the scan is applied to.

-   **Short Description**

    Brief explanation of the scan.

-   **Resolution Details**

    Instructions on how to resolve issues reported by the scan.


Findings can be muted by selecting the **Mute / Unmute** button. When muting a scan finding, you're prompted a reason for muting the finding. Findings muted in the last six months are available in the muted findings card in the **Scan Findings** page.

**Parent Topic:**[Security scanner](sc-scanning.md)

