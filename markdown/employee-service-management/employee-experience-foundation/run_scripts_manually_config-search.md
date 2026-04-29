---
title: Run fix scripts to update Employee Center
description: Manually run fix scripts to upgrade to the latest taxonomy-based Employee Center. Download the latest version from the ServiceNow Store before running the scripts. The scripts update your existing portal setup to Employee Center without performing multiple set up or configuration steps.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Post installation troubleshooting, Admin configurations, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Run fix scripts to update Employee Center

Manually run fix scripts to upgrade to the latest taxonomy-based Employee Center. Download the latest version from the ServiceNow® Store before running the scripts. The scripts update your existing portal setup to Employee Center without performing multiple set up or configuration steps.

## Before you begin

Role required: admin

## About this task

Manually run the following are the scripts if

-   You are an existing Employee Service Center \(HR\) customer and have modified the portal records.
-   You have not installed the demo data at the time of installation, repair the dependent plugins as described in [Install Employee Center](activate-ec.md) and [Install Employee Center Pro](install-ec-pro.md).

<table id="table_kp2_vv3_2rb"><thead><tr><th>

Fix script

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee Center Easy Install

</td><td>

Helps to uptake taxonomy for Employee Center. This script runs automatically during install or upgrade.Modifies the following if the employee center portal record is not customized.

-   Updates the catalog search source.
-   Associates the taxonomy to portal.
-   Updates the dashboard, theme, and menu in employee center portal record.

**Note:** Running this script overrides and resets any modification made to the portal configuration.

</td></tr><tr><td>

Set primary topics for Employee taxonomy

</td><td>

Fixes features like the **Recommended for you** and the **View as Direct Report** searches, if **Employee** taxonomy is associated to the portal. Updates the **taxonomy\_topic** column in the knowledge articles and catalog items to the corresponding mapping found in m2m\_connected\_content table.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for `Employee Center Easy Install` or `Set primary topics for Employee taxonomy` script, and click to open.

3.  In the **Script** field, change the `runManually` parameter value to **true**.

4.  Click **Run Fix Script**.


## Result

Your existing portal is updated to the latest Employee Center portal that uses unified taxonomy.

## What to do next

Configure AI search to align with curated experience. For more information, see [AI Search for Curated Experiences](align-search-for-curated-exp.md).

**Parent Topic:**[Post installation troubleshooting](../concept/post-install-steps.md)

**Related topics**  


[Run fix-script for RCA approvals](install-rca-fix-script.md)

