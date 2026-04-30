---
title: Configure descriptive elements for input form screens
description: Add descriptive elements, such as simple text, rich text, or an image, before an input field within an input form screen. This additional on-screen information provides a context to your users, enabling them to better understand what is required as they enter data into an input form.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-03-05"
reading_time_minutes: 5
breadcrumb: [Data sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure descriptive elements for input form screens

Add descriptive elements, such as simple text, rich text, or an image, before an input field within an input form screen. This additional on-screen information provides a context to your users, enabling them to better understand what is required as they enter data into an input form.

## Before you begin

Role required: admin

## About this task

You can add descriptive elements to input fields, sections that contain input fields, or input form sections without any inputs. Descriptive elements can be a selection of simple text, rich text, or an image that precedes an input.

You must have the following elements configured before you create descriptive elements:

-   A data source that contains at least one element identifier. Data sources facilitate the mapping of the descriptive element to the input form screen. For more information, see [Data sources](../concept/data-sources.md).
-   A record section that can either be an input or an input form section:
    -   An input form section is a group of inputs in a defined area of the input form screen, usually with a defined header.
    -   Inputs are individual fields for users to complete within the input form screen. Inputs can be located either within a section or independent of a section.

**Note:** There can be multiple descriptive elements for each input or for each input form section. However, you must create a separate record for each descriptive element of every input.

The following stages are required when creating a descriptive element: First, declare what the descriptive element is and what it's related to. Next, determine whether the descriptive element is associated with an input or an input form section. Then, create attributes for each type of descriptive element you have selected. Finally, map the descriptive element into an input form screen UI element.

|Descriptive elements of image and rich text on an input form screen|Descriptive elements of image and plain text on an input form screen|
|-------------------------------------------------------------------|--------------------------------------------------------------------|
|![Descriptive elements of an image and rich text in an input form screen.](../image/des-elements2-callouts.png)|![Descriptive elements of an image and plain text in an input form screen.](../image/des-elements1-callouts.png)|

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **All mobile records** from the menu.

4.  From the **Record type** field, select **Descriptive element \[sys\_sg\_descriptive\_element\]** and then select **New**.

5.  Complete the following fields as needed.

<table id="table_msb_ybn_p2c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

A unique name for your descriptive element.

</td></tr><tr><td>

Label

</td><td>

A label that displays above the descriptive element.

</td></tr><tr><td colspan="2">

Settings

</td></tr><tr><td>

Descriptive element types

</td><td>

Three descriptive elements are available:-   **Rich text**: Supports HTML tags such as, bold, underline, italic, bullets, numbered lists, and font color.
-   **Text**: Plain text without any rich text elements.
-   **Image**: A single image to accompany the descriptive element.
**Note:** Attributes available with the **Descriptive elements attributes** field differ according to the descriptive element that you select.

</td></tr><tr><td>

Order

</td><td>

The order this descriptive element displays before the input.

</td></tr><tr><td colspan="2">

Descriptive element placement

</td></tr><tr><td>

Parent table

</td><td>

Option to place the descriptive element within a specified area. The following options are available:-   **Input**: The descriptive element precedes the input.
-   **Input form section**: The descriptive element exists within the specific section.
**Note:** Usually a descriptive element is placed at the top of a section. However, there's also an option to include a descriptive element within a section without displaying any inputs. For configuration instructions, see Step 8.

</td></tr><tr><td>

Parent record

</td><td>

The input or input form section the parent table relates to.

</td></tr><tr><td>

Descriptive element attributes

</td><td>

Use attributes to determine how descriptive elements are shown on the mobile device. Select **New** to add attributes. The following attributes are available for all the descriptive element types \(Rich text, Text, and Image\):-   **_DataSourceId_**

The unique identifier for the data source you're working with. This attribute must be used for descriptive elements.

-   **_ElementIdentifier_**

The unique identifier for each UI element. This attribute must be used for descriptive elements.

**Note:** This identifier is listed as *valuesMapper.addRecordMapping* in the data source script

-   **_MergeWithNextUIElement_**

This is how the descriptive element appears on the input form screen. Mark as `true` to create a gap between inputs or input sections.

**Note:** The following default values exist:

    -   The **Parent table** of type `Input` has a value of `false`.
    -   The **Parent table** of type `Input form section` has a value of `true`.
The following attributes are also available for the descriptive element type, Image:

-   **_AlternativeText_**

Ability to enter an alternative text to be read out to users.

-   **_MediaHeight_**

The height of the image. The default value is 210 pixels.

-   **_Scaling_**

Select **Fit** to ensure that the frame fits the image, maintaining its aspect ratio. Select **Fill** to have the image cropped to fill the frame. This is the default value.

</td></tr></tbody>
</table>6.  Enter a **Name** for your descriptive element.

7.  Select the **Descriptive element type**, \(either Rich text, Text, or Image\) to display before the input value.

8.  In the **Parent table field**, select if the descriptive element displays before an input or at the top of a section.

    **Note:** Usually a descriptive element is placed at the top of a section. However, there's also an option to include a descriptive element within a section without displaying any inputs. To apply this layout, you need to do apply the following configuration.

    1.  Open the web-based UI.
    2.  Navigate to **All** &gt; **sys\_sg\_section\_attribute.list**.
    3.  Select **New**.
    4.  In the **Name** field add the attribute name *HideIfDescriptiveOnly* with a value of `false`. This setting states that descriptive elements are displayed even if there are no inputs in that section.
    5.  In the **Selection** field, select the section of the input form where this attribute applies.
    6.  Select **Submit**.
9.  In the **Parent record** field, select the input or input form section the parent table relates to.

10. In the **Descriptive elements attributes** field, select **New** and do the following:

    1.  Select **DataSourceID** in the **Name** field.
    2.  In the **Value** field, select a value as listed in the data source script.
    3.  Select **Save**.
    4.  Select **ElementIdentifier** in the **Name** field.
    5.  Enter the element identifier as is written in the data source script.
    6.  Select **Save**.
    **Note:** The value available for data sources and element identifier are detailed in the data source script. You select which data source contains the mapping to the element identifier that you want to use for this descriptive element.

11. Select any other descriptive elements attributes that are relevant to the descriptive element you're working on.

12. Select **Save**.


