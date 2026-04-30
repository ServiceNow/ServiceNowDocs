---
title: Return excluded security artifacts to a case
description: After you have excluded artifacts from a list in a case, you can return them to the case you can continue to work on them.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security artifact exclusion and inclusion, Security artifact analysis, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Return excluded security artifacts to a case

After you have excluded artifacts from a list in a case, you can return them to the case you can continue to work on them.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## Procedure

1.  Open a case that contains artifacts that you previous excluded from a list that you want to return to the list.

2.  Click the **Case Artifacts** related list.

3.  Click the tab associated with the artifacts you want to return to the list.

4.  Click the Artifact Filter drop-down list and select **Excluded Artifacts**.

    ![Excluded Artifacts list](../image/exclude-filter.png)

5.  Select one or more artifact records that you want to return to the Include list.

6.  From the **Actions on selected items** drop-down list, select **Include**.

    ![Select artifacts and return them to the Include list](../image/re-include-artifacts.png)

7.  Click **Include** in the confirmation box.

    The selected artifacts are removed from the list of excluded artifacts and returned to the list of artifacts included in the case.


**Parent Topic:**[Security artifact exclusion and inclusion](../concept/artifact-inclusion-exclusion.md)

**Related topics**  


[Exclude security artifacts from a case](exclude-records.md)

