---
title: Input form screen attributes for inputs
description: Different types of inputs are available for use in input form screens, and you can use different attributes to configure the inputs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Configure inputs, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Input form screen attributes for inputs

Different types of inputs are available for use in input form screens, and you can use different attributes to configure the inputs.

Use input attributes to define the appearance and set limitations on your inputs. Examples include setting minimum and maximum values, or displaying an input value as a percentage.

**Note:** All attributes are case-sensitive.

## General attribute

You can use this attribute with any input form screen, regardless of the input type.

<table id="table_s1p_pcy_2qb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**DescriptionRenderType**

</td><td>

Define a render type for the input description.**html**: Enables you to use HTML tags to format the text in the **Description** field of your input.

</td></tr><tr><td>

DataSourceId

</td><td>

Define this attribute whenever you create a data source mechanism to load input values. For more information, see [Data sources](../concept/data-sources.md).**Note:**

This attribute is not supported with signature inputs.

</td></tr><tr><td>

ElementIdentifier

</td><td>

Define this attribute whenever you create a data source mechanism to load input values. For more information, see [Data sources](../concept/data-sources.md).**Note:**

This attribute is not supported with signature inputs.

</td></tr></tbody>
</table>## Attachment inputs

<table id="table_uxr_k1x_b4b"><tbody><tr><td>

Use attachment inputs to enable users to attach files in an input form screen. Attachment inputs require a scripted action item and an **actionResult** object to upload a file.

**Note:** Attachment inputs are only supported for scripted actions.

</td><td>

![Attachment input example.](../image/param-input-attachment-1.png)

</td></tr></tbody>
</table>The following is an example of code that contains attachment inputs.

```
(function WriteBackAction(parm_input, parm_variable, actionResult) {

  //other write-back inputs and variables here

    actionResult.addAttachment("attach", "incident", gr.getUniqueValue()); //where "attach" is the input name from above screenshot, and “incident” is the table name

})(parm_input, parm_variable, actionResult); 

```

-   **Restrict attachment sources to users**

    You have the option to limit the origins of attachments, to ensure that images are sourced from one or all of the following:

    -   on-site via a camera
    -   from the user’s phone gallery
    -   from the user’s file system
    In the Input attribute record, select `HiddenAttachmentSources`. Select either `camera`, `files` or `gallery`, from the **Value** field and then select **Save**. Repeat the process if you want to include more than one attachment source. For more information, see [Define attachment sources available to users](../task/attachment-source-define.md).

<table id="table_qyx_sfg_zdc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**HiddenAttachmentSources**

</td><td>

Decide where you don’t want images sourced from. Select one of the following source values: `camera`, `files` or `gallery`, from the **Value** field.**Note:** To avoid images and files being obtained from more than one source, add additional **HiddenAttachmentSources** attributes after you save the attribute you are currently configuring.

</td></tr></tbody>
</table>
## Barcode inputs

Use barcode inputs to scan single or multiple barcodes. Barcodes are machine-readable codes in the form of numbers and a pattern of parallel lines of varying widths. These codes are used to identify items such as products, parts, or assets. You can use this input type to enter information about items into your ServiceNow instance by using your mobile app.

-   Barcode inputs can be configured for single scans, multi-scans, or grouped scans. Single scans enable the user to scan only once. In this case, the user must rescan by tapping the scan icon, which clears the scan value. You don't need to configure an attribute for a single scan barcode input.
-   Multi-scan inputs can be configured with the **MaxEntries** attribute. If your input form screen barcode input is configured with the **MaxEntries** attribute, users can quickly scan multiple barcodes sequentially without leaving the scanning interface.
-   Grouped scans can be configured to scan multiple barcodes associated with an asset that must be grouped in a set. To configure a grouped barcode input, you must create a barcode section in the input form screen that has barcode inputs only. Then the section **MaxEntries** attribute must be configured for the grouped barcode section so that users can scan multiple groups of barcodes.

![Examples of scanning a barcode with a mobile app.](../image/barcode-input.png "Barcode scanning in a mobile app")

You can use this attribute with barcode inputs.

<table id="table_dsm_44s_rvb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**MaxEntries**

</td><td>

Used only for configuring multi-scanning and multiple groups of barcodes. Sets the maximum number of barcodes that a user can scan at a time. For example, you can set the value to `5` to enable users to rescan 5 times.**Note:** Use this attribute for multi-scan barcode inputs only. If your barcode input is intended for single scans, no attribute is required.

</td></tr></tbody>
</table>For information about creating an input form screen with barcode inputs, see [Configure input form screens with single and multi-scan barcode inputs](../task/single-multi-barcode-input-config.md) and [Configure input form screens with grouped scan barcode inputs](../task/config-grouped-scan-barcode-inputs.md).

## Boolean inputs

<table id="table_wdg_rmw_b4b"><tbody><tr><td>

Use Boolean inputs for inputs with true or false values. You can configure Boolean inputs to appear either as a check box or as a toggle switch.

</td><td>

![Examples of boolean inputs configured as a check box or toggle switch.](../image/param-input-boolean-1.png)

</td></tr></tbody>
</table>You can use these attributes with Boolean inputs.

<table id="table_u3b_1br_b4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**RenderType**

</td><td>

Specify a render type for the Boolean input.-   **Checkbox**

Displays the input as a check box.

-   **toggle**

Displays the input as a toggle.


</td></tr></tbody>
</table>## Choice inputs

<table id="table_ckj_vmw_b4b"><tbody><tr><td>

Use choice inputs to give your users options to select from. You can create these choices manually or use an existing table and field to provide the choices.

 Configure a choice input to enable users to select a single choice, or multiple choices. The option to select more than one chip in a category is marked by a + sign on the chips.

 Define the number of chips to display, enabling the user to see all options available on a single input form screen. If the defined number of chips to display exceed the defined amount, a **See all** button is displayed. Tap on the **See all** button to open a page with all the options listed.

</td><td>

![Single and multiple choice input options on input form screen.](../image/inline-choice.png "Single and multiple choice input options on an input form screen")

</td></tr></tbody>
</table>You can use these attributes with choice inputs.

<table id="table_gdn_4br_b4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**MultiSelect**

</td><td>

Option to enable users to select multiple choices for the input. The value must be **true** or **false**. Multi-select options are indicated with a "+" sign on the chip.

</td></tr><tr><td>

**Table**

</td><td>

The table where the choice field is located.**Note:** Use this option to use the choices in an existing table and field rather than manually creating choices. You must select a field on this table using the **Field** attribute.

</td></tr><tr><td>

**Field**

</td><td>

The field that contains your choices.**Note:** Use this option to use the choices in an existing table and field rather than manually creating choices. The field defined in this attribute must be on the table defined in the **Table** attribute.

</td></tr><tr><td>

**Inline**

</td><td>

Option to select how to display your choice inputs. By default, the value is **false**, meaning that the choice display is on the same screen, removing the need to navigate to a separate screen. For a visual example, see the image in the Choice inputs introduction.If you select **true**, a list-type option displays where users are required to navigate to an additional screen, after a selection is made.

![Inline choice option showing the need for a secondary selection screen.](../image/param-input-choice-1.png "Inline choice list-style option showing the need for a secondary screen")

</td></tr><tr><td>

**InlineMaxItems**

</td><td>

Option to define the number of chips to display within an input form screen section. The following inputs in the **Value** field are available:-   Empty: Displays the default of up to 8 choice values. If there are more choices than 8 choice values, the **See all** button displays.
-   Negative numerical value: Displays all the choice values, even if it exceeds 8 values.
-   Positive numerical value: Displays the number of choice values defined. If there are more choices than the entered numerical value a **See all** button displays.

The following image illustrates a scenario where 8 is the value entered and there are 12 choice values. The first screen displays 8 values. When the user taps the **See all** button, a new screen opens with all the 12 choice values displayed.![Choice list with See all button.](../image/inline-choice-see-all.png "Choice list with See all button")

</td></tr><tr><td>

**RenderType**

</td><td>

Option to render the choice options as an image for the choice input. The value must be `image`.

</td></tr><tr><td>

**EnableSearch**

</td><td>

Option to display the search bar. The value must be **true** or **false**.

</td></tr><tr><td>

**SearchPlaceholder**

</td><td>

Text that appears in a search bar as a placeholder.

</td></tr><tr><td>

**SearchType**

</td><td>

Defines the query used for search. The value can be `starts_with` or `contains`. If this attribute isn’t configured, the instance uses **starts\_with** by default on the display label column.

</td></tr></tbody>
</table>## Custom map inputs

<table id="table_cust_map_b4b"><tbody><tr><td>

Use custom map inputs to add a link to an indoor map in your mobile app. Users can use these maps to get directions to and reserve resources such as desks, meeting rooms, or lockers.

 Admins can also configure a parametrized data item with query conditions that enable sorting and filtering of the custom map input.

 **Important:**

Custom map inputs that support parametrized data items must only use the **ScreenId** attribute. Don't use any other type of attribute for custom map inputs that support parametrized data items.

If you're modifying an existing custom map input that uses the advanced reference qualifier to use a parametrized data item, use the **ScreenId** attribute only and remove all other attributes.

</td><td>

![Shows how the custom map input is displayed in a mobile app where you select 'Next' to view the map.](../image/input-form-custom-map-input.png)

</td></tr></tbody>
</table>You can use these attributes with custom map inputs.

**Note:** You can add the custom map input type to your mobile app by using Mobile App Builder, but you must configure the attributes in the platform web UI of your instance.

<table id="table_w3f_lh4_c5b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**CustomMapConfigId**

</td><td>

The sys\_id of the sys\_sg\_custom\_map\_config table.

</td></tr><tr><td>

**CustomMapDefaultProviderId**

</td><td>

The sys\_id of the provider record in the sys\_sg\_custom\_map\_provider table.

</td></tr><tr><td>

**CustomMapInputs**

</td><td>

The sys\_id of the floor in the sys\_sg\_input table. This value must be entered as a JSON array.

</td></tr><tr><td>

**ScreenId**

</td><td>

The sys\_id of a parameterized data item used to sort and filter custom map inputs.**Important:** This attribute can't be used with any other custom map input attribute. If you use the **ScreenId** attribute with a custom map input, don't use any other attributes with the input.

</td></tr><tr><td>

**TargetTable**

</td><td>

Set to `sn_wsd_core_space`.

</td></tr></tbody>
</table>## Date/time inputs

<table id="table_uxk_hww_b4b"><tbody><tr><td>

Use date/time inputs to enable your users to input date and time values. You can configure the input for date and time, or date only.

</td><td>

![Examples of date and date time configurations.](../image/param-input-datetime-1.png)

</td></tr></tbody>
</table>You can use these attributes with date/time inputs.

<table id="table_wxk_hww_b4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**RenderType**

</td><td>

Specify a render type for the date/time input.-   **date-time**

Displays date and time. If no RenderType is defined, this option is the default.

-   **date**

Displays only the date.


</td></tr><tr><td>

**IncludeTimezone**

</td><td>

The time zone of the mobile device where the input is being added. The value must be **true** or **false**.

 When set to **true**, the mobile client sends the Device Time Zone information along with the date and time value to the back-end instance in the following format:

 YYYY-MM-DDThh:mm:ss.sssTZD

 **Note:** The Device Time Zone is different from the User Profile Time Zone that is configured on the platform.

 If this attribute is not configured, the mobile client doesn't include Device Time Zone information in the date/time input values. This behavior is the default. The date/time input values are in the following format:

 YYYY-MM-DD hh:mm:ss

 For information about setting up the IncludeTimezone attribute of date/time inputs for different action types, see [Date/time input setup for different action item types](../concept/datetime-input-setup-4-action-items.md).

 For information about action item types, see [Configure an action item](../task/sg-studio-create-action-item.md).

</td></tr><tr><td>

**MaxRangeDays**

</td><td>

Optional attribute that determines whether future dates can be selected when a date/time input is added. This attribute supports both positive and negative integer values. Setting **MaxRangeDays** to `0` prevents users from selecting future dates and restricts them to current or past dates.

 **Note:** **MaxRangeDays** can be used together with **MinRangeDays**, **MaxRangeHours**, and **MinRangeHours**.

</td></tr><tr><td>

**MinRangeDays**

</td><td>

Optional attribute that determines whether past dates can be selected when a date/time input is added. This attribute supports both positive and negative integer values. Setting **MinRangeDays** to `0` prevents users from selecting past dates and restricts them to current or future dates.

 **Note:** **MinRangeDays** can be used together with **MaxRangeDays**, **MaxRangeHours**, and **MinRangeHours**.

</td></tr><tr><td>

**MaxRangeHours**

</td><td>

Optional attribute that determines whether future hours can be selected when a date/time input is added. This attribute supports both positive and negative integer values. Setting **MaxRangeHours** to `0` prevents users from selecting future date times and restricts them to current or past date times.

 **Note:** **MaxRangeHours** can be used together with **MaxRangeDays**, **MinRangeDays**, and **MinRangeHours**.

</td></tr><tr><td>

**MinRangeHours**

</td><td>

Optional attribute that determines whether past hours can be selected when a date/time input is added. This attribute supports both positive and negative integer values. Setting **MinRangeHours** to `0` prevents users from selecting past date times and restricts them to current or future date times.

 **Note:** **MinRangeHours** can be used together with **MaxRangeDays**, **MinRangeDays**, and **MaxRangeHours**.

</td></tr></tbody>
</table>## Number inputs

<table id="table_wln_n4w_b4b"><tbody><tr><td>

Use number inputs to enable your users to enter numerical values. Define optional minimum and maximum values to define a number range for your input.

 You can optionally configure a number input to appear as a percentage.

 By default, number inputs support decimals.

 To have the basic box input for a number, within an Input record, complete all the mandatory fields and select **Number** in the **Input type** field.

</td><td>

![Examples of number inputs configured as a numerical or percentage values.](../image/ifs-number-box.png)

</td></tr></tbody>
</table>To add additional elements to the number inputs, you can use the input attributes listed in the table. From the **Inputs attributes** field select **New** for each attribute you want to add.

**Note:** The **Translated value attribute** toggle is only relevant when selecting the Decoration input attribute. The Decoration input attribute is relevant for the slider Render type. For more information see, [Configure a slider option for a number input](../task/configure-slider.md).

<table id="table_qmz_d1r_b4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**CustomErrorMessage**

</td><td>

Sets a custom error message that you can specify. This message displays when the associated UI rule condition is met.

</td></tr><tr><td>

**Max**

</td><td>

Specify a maximum value for the input.

</td></tr><tr><td>

**Min**

</td><td>

Specify a minimum value for the input.

</td></tr><tr><td>

**RenderType**

</td><td>

Specify a render type for the number input.-   **integer**

Displays whole integers, such as `3`, `1003`, or `57`. When **integer** is used, end users can only enter integers and can't enter decimals.

![The render type called integer showing an input called Number of outlets with a value of 60.](../image/ifs-number-box2.png)

-   **line**

Displays the input as a line field.

![The render type called line showing an input called Subscription duration in months with a value of 73.](../image/ifs-number-line.png)

-   **percentage**

Displays a percent symbol\(%\) after the number in the input.

![The render type called percentage showing an input called Interest rate in percentage with a value of 8%.](../image/ifs-number-percent.png)

-   **slider**

Displays the input as slider value and a box input. For more information about sliders and how to configure them, see [Configure a slider option for a number input](../task/configure-slider.md).

![The render type called slider showing an input called Weight of package in kilograms with a value of 44.25.](../image/ifs-slider-float-step-size.png)


**Note:** For a table showing which attributes can be used with which render type, see [Number render types and compatible input attributes](number-compatible-input-attributes.md).

</td></tr><tr><td>

**SkipValidationWhenHidden**

</td><td>

**Note:** This attribute can only be used with line and percentage render types.

Can be set to either `true` or `false`. It's set to `false` by default, which means that by default the associated UI rule validation is run on the hidden inputs. Only set this to `true` when you want to skip the validation on hidden inputs.

</td></tr></tbody>
</table>The following input attributes listed in this table apply only to the slider render type. For more information, see [Slider types and their input attributes](slider-input-attributes.md).

<table id="table_lx5_npt_bgc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**DefaultValue**

</td><td>

The value displayed when the user first views the slider. If no value is entered, the value displayed is zero. The default value must be between the min and max values.

 **Note:** This defined value is the the starting point, unless a loading mechanism, which takes priority, is configured. See, [Loading mechanisms for input form screens](../concept/loading-mechanisms.md).

</td></tr><tr><td>

**StepSize**

</td><td>

The size of each step on the slider. The steps must be a number divisible between the max and min number. For example the min number is 20 and the max number is 80, the StepSize can be numbers like 2, 5, or 10.

</td></tr><tr><td>

**ReferencePoint**

</td><td>

When set to **true** a marker is added to the slider, providing a visual reference point for the user.**Note:** For the sake of visual clarity, this input attribute should not be used with the input attribute VisualStepsEnabled.

</td></tr><tr><td>

**VisualStepsEnabled**

</td><td>

When set to **true** the slider displays visual increments based on the specified StepSize input attribute.**Note:** For the sake of visual clarity, this input attribute should not be used with the input attribute ReferencePoint.

</td></tr><tr><td>

**EnforceStepSize**

</td><td>

When set to **true** users are unable to enter a value in the number box that does not align with the StepSize value.

</td></tr><tr><td>

**Decoration**

</td><td>

Defines sections on the slider with corresponding labels that appear when a user taps a section or enters a value. Each section can be associated with a specific color to aid visual representation. For more information, see [Configure a slider option for a number input](../task/configure-slider.md).

</td></tr></tbody>
</table>## Ranking inputs

<table id="table_ymw_vxw_b4b"><tbody><tr><td>

Use ranking inputs to enable your users to sort the available choices in order of preference or priority. Users tap and drag the available choices.

 Choices for the ranking input must be manually defined.

</td><td>

![Ranking input example.](../image/param-input-ranking-1.png)

</td></tr></tbody>
</table>There are no attributes for ranking inputs other than the general attributes listed in this topic.

## Reference inputs

Use reference inputs for inputs that reference a field on a table. These inputs work like reference fields in the forms on your instance. You can configure your reference input with conditions, reference qualifiers, and a search option to help your users find what they need quickly.

The optional search option uses "For text" keyword searches and can search for elements within the mobile view.

You can use these attributes with reference inputs.

|Attribute|Description|
|---------|-----------|
|**SourceTable**|The source table for your reference qualifier.|
|**SourceFieldName**|The field name of the referenced field in the source table.|
|**TargetTable**|The table that you want to target for your reference qualifier.|

The following additional attributes are optional:

|Attribute|Description|
|---------|-----------|
|**MultiSelect**|Option to enable users to select multiple choices for the input. The value must be **true** or **false**.|
|**MobileViewId**|Mobile view ID \(View config\) to use for reference list items​.|
|**EnableSearch**|Option to display the search bar. The value must be **true** or **false**.|
|**SearchPlaceholder**|Text that appears in a search bar as a placeholder.|
|**Conditions**|Enter an encoded query to apply conditions to your reference list. For details on creating these queries, see Encoded query strings.|
|**SearchType**|Defines the query used for search. The value can be `starts_with` or `contains`. If this attribute isn’t configured, the instance uses **starts\_with** by default on the display label column.|

This example creates an input form screen input for the **Assigned to** field on the Incident \[incident\] table. To create this input, you use the three required attributes: **TargetTable**, **SourceTable**, and **SourceFieldName**.

1.  Your users select from a list of users to assign the incident to. So, you set the **TargetTable** attribute to `sys_user`.
2.  Because you're adding the user to an incident record, the **SourceTable** attribute is set to `incident`.
3.  Set the **SourceFieldName** to `assigned_to` so that the selected user is assigned to the **Assigned to** field.

![Input form screen input for the assigned_to field configured in Mobile App Builder.](../image/reference-input-example.png "Reference input for the assigned_to field configured in Mobile App Builder")

![Input form screen input attributes for the assigned_to field configured in Mobile App Builder.](../image/reference-input-attribute-example.png "Reference input attributes for the assigned_to field configured in Mobile App Builder")

## Signature inputs

Use signature inputs to capture e-signatures on an input form screen. Signature inputs can be included on input form screen sections or pages.

![Signature inputs in an input form screen on a mobile device.](../image/signature-inputs.png "Signature inputs in an input form screen on a mobile device")

You can use the optional **IsOverlay** attribute with signature inputs. By default, signatures are rendered in the full modal window. When the **IsOverlay** attribute **Value** is set to `true`, signatures are rendered in a half modal window.

<table id="table_isp_vxc_tvb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**IsOverlay**

</td><td>

Sets whether the signature input is opened in a half modal window. You can set the **Value** to `true` or `false`. A value of **true** configures the signature to open in a half modal window.**Note:** If the signature input is configured as the only input on a page and the **isOverlay** attribute is set to `true`, the **isOverlay** attribute is ignored, and the signature input is displayed in the full screen.

</td></tr></tbody>
</table>For information about creating an input form screen with signature inputs, see [Configure input form screens with signature inputs](../task/configure-signature-inputs.md).

**Note:** The data source loading mechanism, which uses the **DataSouceId** and **ElementIdentifier** attributes is not compatible with signature inputs.

## String inputs

<table id="table_jqf_nsw_b4b"><tbody><tr><td>

Use string inputs for text input. You can define a maximum character length for this input.

</td><td>

![String input example.](../image/param-input-string-1.png)

</td></tr></tbody>
</table>You can use these attributes with string inputs.

|Attribute|Description|
|---------|-----------|
|**Inline**|Option to show the input inline, or to open the input in a separate modal. The value must be **true** or **false**.|
|**MaxLength**|Maximum number of characters for the input value.|
|**ShowDeleteAll**|Option to display a delete button whenever there is text in the input field. This value must be **true** or **false**, and is set to **false** by default.|
|**ConfirmDeletion**|Option to show the user a confirmation message before text is deleted when using **ShowDeleteAll**. The value must be **true** or **false**, and is set to **true** by default.|

## Screen inputs

Use a screen input to transform a list screen into selectable list input. Users can select multiple list items and perform a write-back operation to the cache.

![Screen input example in a mobile app.](../image/input-screen-form-screen-input.png)

You can use these attributes with screen inputs.

|Attribute|Description|
|---------|-----------|
|**ScreenId**|Configures the list screen that is used for the selectable list input. The value is the sys\_id of the list screen.|
|**GetDataFromParent**|Transforms a list screen from a parent screen into the selectable list input. The filters that are applied to the parent list screen are carried over to the screen input. Enter `true` to enable this attribute. By default, it's turned off on the instance.|

