---
title: Zurich Patch 2 Hotfix 1
description: The Zurich Patch 2 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-05"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 2 Hotfix 1

The Zurich Patch 2 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-03-2025\_0248

    Build tag: glide-zurich-07-01-2025\_\_patch2-hotfix1-10-31-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Flow Engine

 PRB1941990

</td><td>

Trigger inputs aren't accessible after a do-until loop execution

</td><td>

This issue is caused by the changes to GlideFlowStages Updater.java \(older name GlideStage UpdateListener.java\). It's observed that, in this specific flow structure, the 'in.request\_item' flow input isn't passed to the 'Create Catalog Task' action. Querying the sys\_flow\_value table, there are 2 entries for 'in.request\_item' one for the flow input and another with the parent loop associated. As the same key 'in.request\_item' is now associated with parent loops, it can only be accessed in the loop body \(and for the specific iteration\), and all other references to it out side the loop aren't available.

</td><td>

1.  Import the flow XML.
2.  Open Service Portal.
3.  Place a request for 'iPad Pro' with the color set to 'Silver'.
4.  Retrieve the RITM.
5.  Open Flow Designer.
6.  Test run the flow XML with the copied RITM as the input.
7.  Open the RITM when the flow waits at the AFA.
8.  Approve the request created for Abel Tuter.

 Expected behavior: The flow resumes, exits the loop, and reached the 'Create Catalog Task' and will be in the 'Waiting' state.

 Actual behavior: After exiting the loop, it is errored at 'Create Catalog Task' with an error executing the instruction.

</td></tr><tr><td>

Mobile Platform

 PRB1953826

</td><td>

UI policies applicable to the screen table are not applied in Mobile Offline when the underlying record comes from an extended table of the screen table

</td><td>

The page document should not be rebuilt unless there were changes in offline to the records referenced in the screen.

</td><td>

1.  Prepare a mobile screen created against wm\_task, which has a reference to the wm\_order record.
2.  Creating the wm\_task record.
3.  Update the wm\_order record.
4.  Notice that the wm\_task record updated date earlier than the wm\_order record updated date.
5.  Open the offline Download cache.

 Notice that when navigating to the wm\_task detail screen for the record, it results in an underlying document being rebuilt when it is not required.

</td></tr><tr><td>

Mobile Platform

 PRB1953804

</td><td>

The processing of hierarchy of tables results in the loss of fields, causing a returned object containing only a partial set of fields for M

</td><td>

This also results in actions not appearing due to missing values used in the button condition.

</td><td>

1.  Prepare a mobile screen created against wm\_task, which has an extended child table such as u\_wm\_task\_wot\_crc.
2.  Open the offline Download cache.

 Notice that when the screen is built, the field values are missing for fields that do have data.

</td></tr><tr><td>

Mobile Platform

 PRB1953824

</td><td>

The document is rebuilt when there are no changes in Mobile Offline due to an incorrect logic comparing the server update time on the **Reference** field in the screen to the current screen record update time

</td><td>

 

</td><td>

1.  Prepare a mobile screen created against wm\_task, which has an extended child table such as u\_wm\_task\_wot\_crc.
2.  Open the offline Download cache.

 Notice that when the screen is built, the field values are missing for fields that do have data.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

