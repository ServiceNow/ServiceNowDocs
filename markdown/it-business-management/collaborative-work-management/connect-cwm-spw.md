---
title: Connecting CWM with Strategic Planning or Portfolio Planning
description: Configure Strategic Planning or Portfolio Planning to include CWM Boards so that you can plan, roadmap, and associate goals to Boards in a portfolio plan.For the lens that you want to use to build portfolio plans, update the configuration to include CWM Board as a planning item in Strategic Planning or Portfolio Planning.Add the lens entity field to the CWM Board form so users can link Boards and have them appear in the right portfolio plan in Strategic Planning or Portfolio Planning workspaces.Link CWM Boards to a lens entity so that these Boards appear in the corresponding portfolio plans in Strategic Planning or Portfolio Planning workspaces.
locale: en-US
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Collaborative Work Management, Strategic Portfolio Management]
---

# Connecting CWM with Strategic Planning or Portfolio Planning

Configure Strategic Planning or Portfolio Planning to include CWM Boards so that you can plan, roadmap, and associate goals to Boards in a portfolio plan.

By adding CWM Boards to a lens configuration, you can access them in the Prioritization, Roadmap, and Goals pages of a portfolio plan as planning items.

**Note:** This functionality requires installing the Strategic Planning or Portfolio Planning application from ServiceNow Store.

To successfully enable planning with CWM Boards in Strategic Planning or Portfolio Planning, complete the following tasks.

## Add CWM Boards to lens configuration

For the lens that you want to use to build portfolio plans, update the configuration to include CWM Board as a planning item in Strategic Planning or Portfolio Planning.

### Before you begin

Role required: admin

Ensure that the Application scope of your instance is set to **Portfolio Planning Core**.

### About this task

All default lenses support CWM Board as a planning item. For example, if you are building portfolio plans using Organization lens, then you can add CWM Board as a planning item in the Organization lens configuration.

### Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Lenses**.

2.  Select a lens.

3.  From the Available list of planning items, move **CWM Board** to the Selected list.

    ![Lens configuration including CWM Boards as planning item.](../images/cwm-add-board-to-lens.png)

    **Note:** If you don't see CWM Board in the Available list, update the system property **sn\_align\_core.planning\_item\_types\_allow\_list** to allow it.

4.  Select**Update**.


### What to do next

[Configure CWM Board form layout](connect-cwm-spw.md#).

## Configure CWM Board form layout

Add the lens entity field to the CWM Board form so users can link Boards and have them appear in the right portfolio plan in Strategic Planning or Portfolio Planning workspaces.

### Before you begin

Role required: admin

Ensure that the Application scope of your instance is set to **Collaborative Work Management**.

### About this task

Include the field for your lens entity in the CWM Board form. This allows CWM users to link their Boards to the lens entity so that the Boards appear in the corresponding portfolio plan. For example, using the project Portfolio lens, you could create a portfolio plan for the Technology portfolio. When CWM users associate their Boards with the Technology portfolio, those Boards will automatically show up in the Technology portfolio's portfolio plan.

Similarly, you can associate Boards to goals or portfolios. To ensure that your CWM users can perform this association, configure the Board form to include these fields.

### Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  From the list of tables, search for and select **sn\_cwm\_board**.

3.  From the Related Links section, select **Layout Form**.

4.  From the list of fields in the Available section, move your desired field to the Selected section.

    For example, move the **Portfolio** field to the Selected section.

    ![Configuring the form layout for CWM Board.](../images/cwm-configure-board-form.png)

5.  Repeat this step for other fields that you want to add to the CWM Board form.

6.  Select **Save**.


### Result

The CWM Board form now shows the new fields added to its layout.

Your CWM users can add details of their departments, portfolios, or primary goals depending on the portfolio plans they want these Boards to show up in.

### What to do next

[Associate Boards with portfolio plan entities](connect-cwm-spw.md#).

## Associate Boards with portfolio plan entities

Link CWM Boards to a lens entity so that these Boards appear in the corresponding portfolio plans in Strategic Planning or Portfolio Planning workspaces.

### Before you begin

Role required: sn\_cwm.cwm\_user

### Procedure

1.  Navigate to **Workspaces** &gt; **Collaborative Work Management**.

2.  From a Space, select a Board.

3.  From the Board header, select the Edit icon \(![Edit icon.](../images/cwm-icon-edit-pencil.png)\).

4.  In the Board form, select a department, primary goal, strategic program, or portfolio to associate with this Board.

    ![CWM Board form showing fields of Department, Primary goal, Strategic program, and Portfolio to enable associating a Board to a portfolio plan.](../images/cwm-board-form-entities.png)

5.  Select **Update**.


### Result

-   If a primary goal is added, this Board will show up in the aligned work for the selected goal in Strategic Planning workspace.

    ![Aligned work shown for a goal in Strategic Planning Workspace.](../images/cwm-board-aligned-work.png)

-   If you add a department, and the Board's dates align with that department’s portfolio plan, the Board will automatically appear as a planning item on the roadmap.

    ![CWM Boards as a planning item.](../images/cwm-board-on-roadmap.png)

-   If a portfolio is added, and the Board’s dates align with the portfolio plan, the Board will appear as a planning item in that portfolio plan’s roadmap.

    If there are no dates added to your CWM Board, you can check for Unscheduled items on the Roadmap side panel and add the Board to your roadmap.![CWM Boards as unscheduled items in a portfolio plan's roadmap.](../images/cwm-board-unscheduled-roadmap.png)


