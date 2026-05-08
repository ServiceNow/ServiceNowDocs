---
title: Configure related lists for vertical navigation on record pages
description: Configure the related lists that appear in the vertical navigation layout on record pages in the Vendor Management Workspace.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Configure related lists for vertical navigation on record pages

Configure the related lists that appear in the vertical navigation layout on record pages in the Vendor Management Workspace.

## Before you begin

Role required: admin

## About this task

Beginning with version 21.1.x, record pages in the Vendor Management Workspace use a structured vertical navigation layout instead of the legacy horizontal tab-based layout. The vertical navigation panel groups related lists and pages into logical sections.

Configuring related lists for vertical navigation requires two steps. First, configure the related list on the record form using the workspace record view used by the Vendor Management Workspace. Second, explicitly add the related list to the vertical navigation using configuration tables.

The second step is required because related lists configured on the record form do not automatically appear in the vertical navigation layout.

The following related list tables can be configured for display in the vertical navigation layout:

|Name|Table|
|----|-----|
|Assessment template|Assessment template \[sn\_vdr\_risk\_asmt\_template\]|
|Documents|Documents \[ds\_document\]|
|Due diligence|Third-party due diligence request \[sn\_tprm\_dd\_request\]|
|Engagement|Third-party engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]|
|Event-driven management history|Event-driven management history \[sn\_tprm\_dd\_rule\_execution\_history\]|
|Event-driven management rule|Event-driven management rule \[sn\_tprm\_dd\_generation\_rule\]|
|External assessments|External assessment \[sn\_vdr\_risk\_asmt\_assessment\]|
|Internal assessments|Internal assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]|
|IRQ|Internal assessment \[sn\_vdr\_risk\_asmt\_internal\_assessment\]|
|Issues|Third-party risk issue \[sn\_vdr\_risk\_asmt\_issue\]|
|Risk intelligence providers|Risk intelligence provider \[sn\_vdr\_risk\_asmt\_tpss\_provider\_basic\]|
|Risk intelligence providers service|Risk intelligence provider service \[sn\_vdr\_risk\_asmt\_tpss\_provider\]|
|Risk intelligence report request|Risk intelligence report request \[sn\_tprm\_dd\_risk\_intel\_request\]|
|Risk intelligence request type|Risk intelligence request type \[sn\_tprm\_dd\_risk\_intel\_request\_type\]|
|Tasks|Third-party risk task \[sn\_vdr\_risk\_asmt\_task\]|
|Third-party|Company \[core\_company\]|
|Vendor contacts|Vendor Contact \[vm\_vdr\_contact\]|

For more information about related lists, see Related lists.

## Procedure

1.  Select the Vendor Risk Management Workspace application scope.

    1.  In the header, open the application scope picker.

    2.  Select **GRC: Vendor Risk Management Workspace**.

    Selecting this scope makes workspace-specific views and configuration tables available.

2.  Configure the related list on the record form.

    1.  In the Application Navigator \(All\), enter the target table name followed by `.list` \(for example, `core_company.list`\).

    2.  Open an existing record from the list.

    3.  From the form header, select **Configure** &gt; **Related Lists**.

    4.  Select **Edit this view**.

    5.  From the view selector, choose the workspace record view used by the Vendor Management Workspace.

    6.  In the Available list, select the related list.

    7.  Move the related list to the Selected list.

    8.  Select **Save**.

    9.  Verify that the related list appears on the form in the selected view.

    This step makes the related list available to the workspace but does not add it to the vertical navigation.

3.  Navigate to the vertical navigation configuration table.

    1.  In the Application Navigator \(All\), enter `sn_rec_pg_vertical_view_config.list`.

    2.  Select **VRM vertical nav configuration**.

    This table defines which related lists appear in the vertical navigation for workspace record pages.

4.  Create or update a vertical navigation entry.

    1.  To create a new entry, select **New**.

    2.  To update an existing entry, open it from the list.

5.  Configure the vertical navigation entry.

    1.  In the **Table** field, select the target table.

    2.  In the **Group** field, select the group where the related list should appear.

    3.  Set the **Type** field to **Related list**.

    4.  Set the display order.

    5.  Select **Save**.

6.  Verify the related list appears in the vertical navigation.

    1.  Open a record page in the Vendor Management Workspace.

    2.  Refresh the page if it was already open.

    3.  Confirm that the related list appears under the selected group in the vertical navigation panel.


## Result

The related list appears in the vertical navigation layout on the configured record page in the Vendor Management Workspace.

## What to do next

If the related list does not appear, confirm that:

-   The related list is configured on the workspace record view.
-   A configuration entry exists in the vertical layout table.
-   The correct application scope is selected.

