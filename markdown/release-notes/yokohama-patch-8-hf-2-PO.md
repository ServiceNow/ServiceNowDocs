---
title: Yokohama Patch 8 Hotfix 2
description: The Yokohama Patch 8 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-05"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 8 Hotfix 2

The Yokohama Patch 8 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-31-2025\_1629

    Build tag: glide-yokohama-12-18-2024\_\_patch8-hotfix2-10-30-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

Advanced Work Assignment

 PRB1950558

</td><td>

Advanced Work Assignment \(AWA\) should be able to determine if the work item is rejected due to time out or Asynchronous Message Bus \(AMB\) disconnection

</td><td>

When the work item times out, the work item reason on the awa\_work\_item\_rejection table is 'Timed out' instead of 'AMB connection lost'.

</td><td>

1.  Install the Agent Chat plugin with the demo data.
2.  Open the AWA assignment rule.
3.  Update the timeout time to 15 seconds.
4.  Open a browser \(browser 1\).
5.  Log in to the workspace as an agent in browser 1.
6.  Open another browser \(browser 2\).
7.  Log in to the instance as a requestor.
8.  Open the URL $sn-va-web-client-app.do in browser 2.
9.  In browser 1, close the workspace tab completely as an agent.
10. Notice that the agent presence will not be set to offline immediately because the default idle check gives a 5 min buffer, and the agent is still available to receive work item at the moment.
11. In browser 2, start the live agent handoff.
12. Wait for 15 seconds so the work item will be timed out.
13. As an admin, navigate to the awa\_work\_item\_rejection table.
14. Check the rejection record for the previous interaction.

 Expected behavior: The reason should be 'AMB connection lost'.

 Actual behavior: The rejection reason is 'Timed out'.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 8 Hotfix 1](yokohama-patch-8-hf-1-PO.md)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

