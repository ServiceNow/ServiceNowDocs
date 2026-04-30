---
title: View previewed upgrade
description: Use the Upgrade Preview form to have an alternate view of a previewed upgrade.
locale: en-US
release: yokohama
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Previewing an upgrade, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# View previewed upgrade

Use the Upgrade Preview form to have an alternate view of a previewed upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Preview module**.

2.  Select the target version to be previewed.

3.  Click **Go** or **Refresh Preview** to run the selected preview.

4.  Click **View preview details** on the **Previewing version** card to view the following related lists.

    -   **Predicted Skips to Review related list**: The Upgrade Preview process informs you about the customizations that are predicted to be skipped during an upgrade. The upgrade preview process the skip files that have been customized. Predicted Skips to Review lists all the skipped files that haven't been reviewed yet.
    -   **Predicted Skips Reviewed related list**: Predicted Skips Reviewed related list displays the records which have previously appeared on the Predicted Skips to Review related list and have been reviewed. When you select a skipped record to review and the **Resolution Status** has been set to a value other than **Not Reviewed**, the updated record moves to the Predicted Skips Reviewed related list.
    -   **Previewed Changes related list**: Previewed Changes related list gives the total number of records that are predicted to change when the upgrade occurs. Total record changes also includes possible predicted skip files known as Predicted skipped records.
    See [Previewed changes](../reference/uc-previewed-changes.md) for more details about the related lists.

    ![Image showing Upgrade Preview form](../image/uc-upgrade-preview-form.png)

<table id="table_b5b_p14_dlb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Source version

</td><td>

Current version of the instance

</td></tr><tr><td>

Target version

</td><td>

Target version to which the instance is upgraded to be previewed

</td></tr><tr><td>

Preview status

</td><td>

Status of the preview.-   Pending
-   In Progress
-   Complete
-   Cancelled
-   Failed


</td></tr><tr><td>

Preview Started

</td><td>

Date and time on which the preview started

</td></tr><tr><td>

Preview Finished

</td><td>

Date and time on which the preview completed

</td></tr></tbody>
</table>
