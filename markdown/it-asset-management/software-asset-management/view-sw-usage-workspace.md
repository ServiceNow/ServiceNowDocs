---
title: View or create software usage in workspace
description: View software usage records to track the usage of software products that you've created reclamation rules for in the Software Asset Workspace. You can also create software usage records manually from third party integrations or Microsoft SCCM integrations.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [License operations view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# View or create software usage in workspace

View software usage records to track the usage of software products that you've created reclamation rules for in the Software Asset Workspace. You can also create software usage records manually from third party integrations or Microsoft SCCM integrations.

## About this task

The Software Usage \[samp\_sw\_usage\] table tracks usage down to the product level and not to the version or edition level.

## Before you begin

Role required: sam\_admin or sam\_user

## About this task

Use the following steps to create software usage records manually.

## Procedure

1.  From your ServiceNow instance, navigate to **Software asset** &gt; **Software Asset Workspace**.

    The Software Asset Workspace launches in a new tab.

2.  On the left navigation menu of the Software Asset Workspace, select **License operations**.

    The License operations view opens.

3.  On the **Lists** tab of the License operations view, navigate to **Discovery** &gt; **Software usage**.

4.  Select **New**.

5.  On the Create New Software Usage form, fill in the fields.

<table id="table_w2y_w11_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Software usage

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software product.

</td></tr><tr><td>

Product

</td><td>

Name of the software product.

</td></tr><tr><td>

Reclamation type

</td><td>

Type of reclamation used on the software installation. The options are **Total Usage Time** and **Last Used Date**.**Note:** If you select **Total Usage Time**, the Usage Metering Data form section appears. If you select **Last Used Date**, the Last Used Data form section appears.

</td></tr><tr><td>

Configuration Item

</td><td>

Configuration item \(CI\) that the software product is associated with. **Note:** If the CI **Status** or **Hardware Status** field changes to Retired or Stolen, installations that are related to the CI are deleted.

</td></tr><tr><td>

User

</td><td>

Name of the user who is using the software product.

</td></tr><tr><td>

Discovery source

</td><td>

Discovery source of your software usage data. If the appropriate discovery source is not displayed on the **Discovery source** list, you can display it by right-clicking the **Discovery source** field name and then selecting **Configure Choices**. When prompted, use one of the following options to display the discovery source:

-   If the discovery source already exists on your ServiceNow instance, it appears in the Available list. Move the discovery source to the Selected list so that it displays on the **Discovery source** list. Select **Save** to return to the Create New Software Usage form, where you can view the updated **Discovery source** list.
-   If the discovery source does not already exist on your ServiceNow instance, enter the name of the discovery source in the **Enter new item** field and then select **Add**. Move the new discovery source from the Available list to the Selected list so that it displays on the **Discovery source** list. Select **Save** to return to the Create New Software Usage form, where you can view the updated **Discovery source** list.


</td></tr><tr><td class="sub-head" colspan="2">

Usage Metering Data**Note:** This form section appears only if the **Reclamation type** is set to **Total Usage Time**.

</td></tr><tr><td>

Month

</td><td>

Month that the software product was used.

</td></tr><tr><td>

Year

</td><td>

Year that the software product was used.

</td></tr><tr><td>

Usage count

</td><td>

Number of times that the software product was accessed.

</td></tr><tr><td>

Total seconds used

</td><td>

Amount of time \(in seconds\) that the software product was used.

</td></tr><tr><td class="sub-head" colspan="2">

Last Used Data**Note:** This form section appears only if the **Reclamation type** is set to **Last Used Date**.

</td></tr><tr><td>

Last used time

</td><td>

Date and time that the software product was last used.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

After the software usage is created, you can view it by navigating to **License operations** &gt; **Discovery** &gt; **Software usage**.

