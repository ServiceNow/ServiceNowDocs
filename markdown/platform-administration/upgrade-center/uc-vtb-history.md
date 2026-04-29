---
title: Skipped Records visual task board \(VTB\)
description: View the resolution status of any previous upgrade with skipped records using the visual task board \(VTB\) view. An upgrade history record is created for each upgrade that is run.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reviewing upgrade history, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Skipped Records visual task board \(VTB\)

View the resolution status of any previous upgrade with skipped records using the visual task board \(VTB\) view. An upgrade history record is created for each upgrade that is run.

To view the history report navigate to **Upgrade Center** &gt; **Upgrade History**. You can then select an upgrade from the list to view the upgrade history details. Click the **Skipped Record VTB** related link to view and manage the skipped records over VTB.

**Note:** The **Skipped Record VTB** related link shows up only when there are skipped records for the version upgrade.

|Field|Description|
|-----|-----------|
|Not Reviewed|Tasks which have not been reviewed|
|Reviewed|Tasks which have been reviewed|
|Merged|Tasks which have both the old and new changes|
|Retained|Tasks which have retained the updates from the latest upgrade|
|Reverted|Tasks which have reverted its changes to the base system|

The skipped records are prioritized based on the importance of the file types. The prioritization is done as follows:

-   Priority 1 \(highest priority\): UI pages, UI macros, and more
-   Priority 2: Business Rules, Security ACLs, and more
-   Priority 3: Reports and more
-   Priority 4: Form Sections, Choice Sets, and more
-   Priority 5 \(lowest priority\): other

![Image showing the VTB view of skipped records resolution status](../image/uc-vtb.png)

