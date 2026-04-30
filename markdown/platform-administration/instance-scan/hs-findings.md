---
title: Findings
description: A finding is a reference to a record that has violated a rule from a check on the instance. You can find the source record and the number of times the record triggered rules of a given check.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reviewing of scans, Use, Instance Scan, Maintain and monitor, Administer]
---

# Findings

A finding is a reference to a record that has violated a rule from a check on the instance. You can find the source record and the number of times the record triggered rules of a given check.

Each finding is specific to a result and each result is specific to a scan that has been executed.

**Note:** When you run a scan, you definitely get a result of the scan but might not get any findings. There might be no findings encountered during the execution of the checks.

**Note:** If a record is inactive, the checks don't generate any findings for that record.

The Scan Finding gives information about the check that has been violated by a record. The **Source Table** and **Source** fields point to the record that has violated a rule from a check during the execution. You can find more information about the record by clicking the information icon. The **Count** field shows the number of times the record has violated the check rules. The finding also shows the version of the check that generated the finding. The **Product Family** field shows you the product family for each check. The **Task** field helps you to assign a task to an individual or a group. See [Creating scan tasks](../task/hc-create-scan-tasks.md) for more information. If you want to avoid a finding from being generated from any future scans, use the **Mute Rule**.

**Note:** If you use the **Mute Rule**, you must also select a reason for muting the finding.

-   **[Mute a finding](../task/hc-update-scan-finding-form.md)**  
Mute a finding on the Scan Finding form to avoid the finding from being reported in the later scan results.
-   **[Creating scan tasks](../task/hc-create-scan-tasks.md)**  
Create a scan task to facilitate task assignments from the finding of a record.

**Parent Topic:**[Reviewing of scans](../reference/hs-review-scans.md)

