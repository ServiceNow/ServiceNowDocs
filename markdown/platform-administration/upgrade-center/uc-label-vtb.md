---
title: Update default labels in VTB view
description: Filter skipped records in the task board of the VTB with the implementation of color-coded labels. You can filter the skipped records by assigning a color to each of the products.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Skipped Records visual task board \(VTB\), Reviewing upgrade history, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Update default labels in VTB view

Filter skipped records in the task board of the VTB with the implementation of color-coded labels. You can filter the skipped records by assigning a color to each of the products.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade History**.

2.  Select an upgrade from the list.

    The System Upgrades form appears.

3.  Click the **Skipped Record VTB** related link to view the resolution status of the skipped records over VTB.

    **Note:** The **Skipped Record VTB** related link shows up only when there are skipped records for the version upgrade.

    The VTB view of the resolution status of the skipped records shows up.

4.  Click **Labels** to show the default labels.

    The default labels consist of Include codes, Does not include code and Others categories.

    **Note:** The Include and Does not include codes categories indicate if there is any change in the code of the skipped records. All products fall under Other category of labels. The product labels are assigned with different colors. The tasks get assigned based on the label colors of the products.

5.  If you want to add a label, click **Add Label**.

    Enter the name of the label you want to create. You can also change the color of a label by clicking the color circle.![Image showing Add Label and color change in the VTB view](../image/uc-labels.png)

    **Note:** The new labels and colors are saved only for the current visual task board and don't get rolled over to the next updated board. If you want the new label updates to show up in the next updated board, navigate to **Upgrade Center** &gt; **Administration** &gt; **Properties** &gt; **Upgrade Center VTB Labels**. Set the colors as required and the updated colors start showing up from the next generated board.


## What to do next

Click on a skipped record in the VTB to update the task. See [Upgrade History Task form](../reference/uc-history-task-form.md) for more information.

