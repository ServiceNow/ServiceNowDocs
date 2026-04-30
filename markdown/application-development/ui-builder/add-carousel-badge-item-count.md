---
title: Add Carousel badge item count
description: How to create a dynamic carousel item count \(displayed in the badge\) where the items in the carousel are controlled by a repeater pulling its data from a data resource.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [UIB, UI Builder, Carousel, Components]
breadcrumb: [Learn components by example, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add Carousel badge item count

How to create a dynamic carousel item count \(displayed in the badge\) where the items in the carousel are controlled by a repeater pulling its data from a data resource.

## Before you begin

Role required: workspace\_admin or ui\_builder\_admin

This procedure uses UI Builder components to create dynamic, interactive layouts. For more information on how to configure components, see:

-   [Add and configure components](add-components.md#)
-   [UI Builder Quick Bits: Navigating Component Configuration](https://www.servicenow.com/community/next-experience-blog/ui-builder-quick-bits-navigating-component-configuration/ba-p/3181624)

<table id="table_exc_zzf_dhc"><thead><tr><th>

Component

</th><th>

Documentation links

</th></tr></thead><tbody><tr><td>

Carousel

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/sn-carousel?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/sn-carousel/uib-setup%23properties)

</td></tr></tbody>
</table>## Procedure

1.  Set up Carousel to use a repeater pulling its data from a data resource.

2.  To create an object that determines the badge properties, open the page's **Client state parameters** dialog.

    ![Pointer hovering over selected Client state parameters and the Edit client state parameters dialog as it first appears](../../../build/component-uib-setup/image/badge-edit-clientstateparams.png)

    1.  Replace the **Name** with `badgeConfigState`, and from the **Type** dropdown, choose **JSON**.

        ![Edit client state parameters dialog with the Name changed to badgeConfigState and JSON being selected from the Type dropdown](../../../build/component-uib-setup/image/badge-edit-02clientstateparams.png)

    2.  Hover over the **Initial value** field box and select **Edit**.

    3.  Choose the JSON type **object** from the dropdown.

    4.  Select **Add property** and add the badge **color**, **label**, and **variant** properties.

        ![Initial Value pop up with 3 properties added, color, label, and variant](../../../build/component-uib-setup/image/badge-client-state01.png)

    5.  Select **Apply** to return to the **Edit client state parameters** dialog.

        ![Returned to Edit client state parameters with badgeConfigState JSON parameters](../../../build/component-uib-setup/image/badge-client-state02.png)

    6.  Close the dialog.

        Later, you will use a script to update this object's properties after the data resource loads.

3.  To set the badge config to the object just created, in the **Content** tree, select the **Carousel** component.

    1.  On the **Config** tab for your Carousel component, hover over the **Badge configuration** property and select the **Bind data or use scripts** icon.

        ![Carousel Badge configuration showing the 3 parameters added and the pointer hovering over the Bind data or use scripts button](../../../build/component-uib-setup/image/badge-bind-data-badgeconfig.png)

    2.  In the **Bind data to Badge configuration** dialog, select the data type **Client states**.

    3.  Select **badgeConfigState \(3\)**, and to add it to the data output area, select the up arrow icon.

        ![Bind data to Badge configuration dialog with Client states selected in Data types and badgeConfigState 3 highlighted with pointer hovering over up arrow button](../../../build/component-uib-setup/image/badge-02bind-data-badgeconfig.png)

    4.  Select **Apply**.

        The **badgeConfigState** parameter should be added to the Carousel **Badge configuration**.

    ![Carousel Configure tab with the Badge configuration field displaying badgeConfigState in addition to the 3 previously added parameters](../../../build/component-uib-setup/image/badge-config-final.png)

4.  Open the **Edit client script** dialog by selecting **Add a new** **Edit client script**.

    ![Pointer hovering over Add new plus sign button and Edit client script dialog that appears when Add new button is selected](../../../build/component-uib-setup/image/badge-edit-clientscript01.png)

5.  To create a client script that updates the **badgeClientState "label"** parameter value to the number of items in the Carousel, enter: `api.setState(`badgeConfigState`, {...api.state.badgeConfigState, "label": `count: ${api.data.look_up_multiple_records_1.results.length}`});`

    ![Edit client script dialog with client script added](../../../build/component-uib-setup/image/badge-edit-clientscript04.png)

6.  Add an event to the data resource so that your client script triggers whenever the data resource is updated.

    1.  In the bottom left, select the data resource **Look up multiple records 1** &gt; **Events tab**.

        ![Pointer, in the Data and scripts section, hovering over the Look up multiple records 1 data resource and Edit Look up multiple records 1 dialog Events tab selected](../../../build/component-uib-setup/image/badge-edit-dataresource01.png)

    2.  Select **Add event mapping**, select **Data Fetch Succeeded**, and select **Continue**.

    3.  Select **Add handler**, scroll down, and select the new client script you created, and select **Continue**.

        ![Dialog for adding the New client script 1 event handler](../../../build/component-uib-setup/image/badge-choose-eventhandler.png)

    4.  When to trigger should be set to **Always**.

    5.  Select **Continue**.

    6.  Select **Add** and close the **Edit** dialog.

7.  In the upper right corner, select **Save** &gt; **select the Preview dropdown arrow** &gt; **Open URL path**.

    ![Final display showing the Title followed by count: 12](../../../build/component-uib-setup/image/badge-final01.png)

    The **Title** of your carousel should have a badge **count** followed by the number of carousel items.


**Parent Topic:**[Learn components by example](../concept/learning-components-by-example.md)

