---
title: Closing stale detections and findings automatically using auto-close rules
description: Auto-close rules automatically close stale detections and findings based on predefined criteria. These rules ensure that redundant or unwanted findings are marked as closed, helping to maintain an accurate and up-to-date record of the organization's security posture. By automating this process, the rules reduce manual effort and enable teams to focus on active and critical vulnerabilities.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Closing stale detections and findings automatically using auto-close rules

Auto-close rules automatically close stale detections and findings based on predefined criteria. These rules ensure that redundant or unwanted findings are marked as closed, helping to maintain an accurate and up-to-date record of the organization's security posture. By automating this process, the rules reduce manual effort and enable teams to focus on active and critical vulnerabilities.

Auto-close rules can be set up to close stale detections and findings based on factors such as:

-   The status of the vulnerability \(for example, marked as resolved or mitigated\)
-   The age of the finding \(for example, findings older than a certain number of days\)
-   Specific conditions or thresholds \(for example, a certain number of consecutive scans without the vulnerability being detected\)

Auto-close rules are crucial for managing stale detections and findings. When a finding is matched with the filter criteria, the auto-close rule can automatically close the associated record. This helps in maintaining a clean and accurate record of the security status, ensuring that teams can focus on new and critical exposure findings. By automating this process, organizations can improve the efficiency and accuracy of their exposure management practices.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring auto-close rules](sem-configure-auto-close-rules.md#)

