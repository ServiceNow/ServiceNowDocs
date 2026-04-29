---
title: Mobile Card Builder components
description: Learn about the components that make up mobile cards
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [User interface, Mobile Card Builder, Building tools, Building mobile apps, Mobile Platform]
---

# Mobile Card Builder components

Learn about the components that make up mobile cards

## Adding and removing components

## Buttons

Button components allow users to perform an action when the button is selected. Use buttons to add actions to your cards.

<table id="table_a5m_jb4_zcc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Element ID

</td><td>

The button's unique JSON ID attribute.

</td></tr><tr><td colspan="2">

Display

</td></tr><tr><td>

Height

</td><td>

Height of your button in pixels

</td></tr><tr><td>

Width

</td><td>

Width of your button in pixels. If this property is left blank, the button fills the available space.

</td></tr><tr><td>

Corner radius

</td><td>

The corner radius of your button. Increase this value to create rounded corners for your button.

</td></tr><tr><td>

Margin top

</td><td>

The top margin of your button in pixels

</td></tr><tr><td>

Margin bottom

</td><td>

The bottom margin of your button in pixels

</td></tr><tr><td>

Margin left

</td><td>

The left margin of your button in pixels

</td></tr><tr><td>

Margin right

</td><td>

The right margin of your button in pixels

</td></tr><tr><td>

Border width

</td><td>

Width of your button’s border in pixels.

</td></tr><tr><td colspan="2">

Button properties

</td></tr><tr><td>

Format

</td><td>

Determine whether your button will appear with a text label, icon, or both.

 Select from the following options:

-   Label
-   Icon
-   Label and icon

</td></tr><tr><td>

Label

</td><td>

The button's text label.**Note:** This option will only appear if either the **Label** or **Label and icon** format is selected.

</td></tr><tr><td>

Icon

</td><td>

The icon that will display on your button. Choose an icon from the provided drop-down list.**Note:** This option will only appear if either the **Icon** or **Label and icon** format is selected.

</td></tr><tr><td>

Accessible name

</td><td>

The alternative text that will be read aloud to people using assistive devices so that they know the purpose of the button.**Note:** This option will only appear if the **Icon** format is selected.

</td></tr><tr><td colspan="2">

Actions

</td></tr><tr><td>

Multiple

</td><td>

Create a menu of multiple different actions that users can choose from when they select the button.

</td></tr><tr><td>

Function

</td><td>

Choose either a Predefined or Configurable function. Configurable functions are taken from the sys\_sg\_button table.

 Available predefined functions:

-   Cancel
-   Continue
-   Log out

</td></tr><tr><td colspan="2">

Button appearance

</td></tr><tr><td>

Text and icon style

</td><td>

The formatting style of your text, icon, or both.

</td></tr><tr><td>

Background color variable

</td><td>

The button background’s color variable.

</td></tr><tr><td>

Background color

</td><td>

The button background’s color. The value for this property is an HTML color code, for example `#A0522D` for sienna.

</td></tr><tr><td>

Text and icon color variable

</td><td>

The button's text and icon’s color variable.

</td></tr><tr><td>

Text and icon color

</td><td>

The button's text and variable color. The value for this property is an HTML color code, for example `#A0522D` for sienna.

</td></tr><tr><td>

Border color variable

</td><td>

The button border’s color variable.

</td></tr><tr><td>

Border color

</td><td>

The button border's color. The value for this property is an HTML color code, for example `#A0522D` for sienna.

</td></tr></tbody>
</table>## Containers

Containers components contain other components. A container can contain any card component, including another container. Use containers to organize your card components, and determine how the components within the container are aligned and distributed.

<table id="table_nm2_bp4_ynb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Properties

</td></tr><tr><td>

Element ID

</td><td>

The container's unique JSON ID attribute.

</td></tr><tr><td colspan="2">

Display

</td></tr><tr><td>

Height

</td><td>

Height of your container in pixels

</td></tr><tr><td>

Width

</td><td>

Width of your container in pixels. If this property is left blank, the container fills the available space.

</td></tr><tr><td>

Margin top

</td><td>

The top margin of your container in pixels

</td></tr><tr><td>

Margin bottom

</td><td>

The bottom margin of your container in pixels

</td></tr><tr><td>

Margin left

</td><td>

The left margin of your container in pixels

</td></tr><tr><td>

Margin right

</td><td>

The right margin of your container in pixels

</td></tr><tr><td>

Corner radius

</td><td>

The corner radius of your container. Increase this value to create rounded corners for your container.

</td></tr><tr><td colspan="2">

Appearance

</td></tr><tr><td>

Container direction

</td><td>

Determines orientation direction of the components within the container. Select from these values:-   Horizontal
-   Vertical

</td></tr><tr><td>

Alignment

</td><td>

Determines the alignment of the components within the container. Select from these values:-   Stretch
-   Center
-   Left
-   Right
-   Top
-   Bottom

</td></tr><tr><td>

Distribution

</td><td>

Determines the distribution of the components within the container. Select from these values:-   Equal
-   Auto

</td></tr><tr><td>

Background type

</td><td>

The type of background the container will have. Select from these values:-   None
-   Color
-   Image

</td></tr></tbody>
</table>## Icons

Icon components are used to display an icon on your card. You can choose an icon from the Icon dropdown menu in the Config screen.

|Property|Description|
|--------|-----------|
|Properties|
|Element ID|The icon's unique JSON ID attribute.|
|Display|
|Icon|The icon to be displayed.|
|Margin top|The top margin of your icon in pixels.|
|Margin right|The right margin of your icon in pixels.|
|Margin bottom|The bottom margin of your icon in pixels.|
|Margin left|The left margin of your icon in pixels.|
|Appearance|
|Color variable|The color variable of your icon.|
|Color|The color of your icon. The value for this property is an HTML color code, for example `#A0522D` for sienna.|

## Images

Image components are used to display an image. You define an image to display by selecting a field on your record that contains an image, for example, the **Avatar** field on a **User** record.

<table id="table_lwl_gr4_ynb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Properties

</td></tr><tr><td>

Element ID

</td><td>

The image's unique JSON ID attribute.

</td></tr><tr><td colspan="2">

Display

</td></tr><tr><td>

Height

</td><td>

Height of your image in pixels.

</td></tr><tr><td>

Width

</td><td>

Width of your image in pixels.

</td></tr><tr><td>

Margin top

</td><td>

The top margin of your image in pixels.

</td></tr><tr><td>

Margin right

</td><td>

The right margin of your image in pixels.

</td></tr><tr><td>

Margin bottom

</td><td>

The bottom margin of your image in pixels.

</td></tr><tr><td>

Margin left

</td><td>

The left margin of your image in pixels.

</td></tr><tr><td>

Corner radius

</td><td>

The corner radius of your image. Increase this value to create rounded corners for your image.

</td></tr><tr><td colspan="2">

Image

</td></tr><tr><td>

Use mapped field

</td><td>

Choose whether the image will use a mapped field.

</td></tr><tr><td>

Field value

</td><td>

The value of the mapped field for your image. This property is only visible if **Use mapped field** is selected.

</td></tr><tr><td>

Attachment

</td><td>

The attached image to use. This property is only visible if **Use mapped field** is not selected.

</td></tr><tr><td>

Image scaling

</td><td>

The scaling for your image. Select from these values:-   Fill
-   Fit

</td></tr></tbody>
</table>## Text

Text components display text on your card. This can be static text, or text from the label of value of a field. Use text components to the information your users need to see first when viewing lists of records.

<table id="table_pjv_jt4_ynb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Properties

</td></tr><tr><td>

Element ID

</td><td>

The text's unique JSON ID attribute.

</td></tr><tr><td colspan="2">

Display

</td></tr><tr><td>

Field type

</td><td>

The type of text field. Select from these values:-   Field value
-   Field label
-   Static text

</td></tr><tr><td>

Text value

</td><td>

The text that appears in the text component. This value is only used when you have selected **Static text** in the **Field type** property.

</td></tr><tr><td>

Height

</td><td>

Height of your text component in pixels.

</td></tr><tr><td>

Width

</td><td>

Width of your text component in pixels.

</td></tr><tr><td>

Margin top

</td><td>

The top margin of your text component in pixels.

</td></tr><tr><td>

Margin right

</td><td>

The right margin of your text component in pixels.

</td></tr><tr><td>

Margin bottom

</td><td>

The bottom margin of your text component in pixels.

</td></tr><tr><td>

Margin left

</td><td>

The left margin of your text component in pixels.

</td></tr><tr><td colspan="2">

Appearance

</td></tr><tr><td>

Text style

</td><td>

The formatting style of your text.

</td></tr><tr><td>

Text alignment

</td><td>

Alignment for the text in your component. Select from these values:-   Left
-   Center
-   Right

</td></tr><tr><td>

Max number of lines

</td><td>

The maximum number of lines for the text in your element.

</td></tr><tr><td>

Text color variable

</td><td>

The color variable for your text.

</td></tr><tr><td>

Text color

</td><td>

The color of your text. The value for this property is an HTML color code, for example `#A0522D` for sienna. **Note:** You cannot change the background color of a text component, but you can place your text component within a container component, and change the container background color.

</td></tr></tbody>
</table>## Videos

Video components display an embedded video in your card. Both Youtube and Viemo video URLs are supported.

<table id="table_lvf_qfz_fdc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Properties

</td></tr><tr><td>

Element ID

</td><td>

The video's unique JSON ID attribute.

</td></tr><tr><td colspan="2">

Display

</td></tr><tr><td>

Use mapped field

</td><td>

Choose whether the video will use a mapped field.

</td></tr><tr><td>

Field value

</td><td>

The value of the mapped field for your video. This property is only visible if **Use mapped field** is selected.

</td></tr><tr><td>

URL

</td><td>

The URL of the video to be embedded. This property is only visible if **Use mapped field** is not selected.

</td></tr><tr><td>

Playback mode

</td><td>

How the video will display on a mobile device. Select from these values:-   Fullscreen
-   Inline

</td></tr><tr><td>

Width

</td><td>

Width of your video component in pixels.

</td></tr><tr><td>

Height

</td><td>

Height of your video component in pixels.

</td></tr><tr><td>

Margin top

</td><td>

The top margin of your video component in pixels.

</td></tr><tr><td>

Margin right

</td><td>

The right margin of your video component in pixels.

</td></tr><tr><td>

Margin bottom

</td><td>

The bottom margin of your video component in pixels.

</td></tr><tr><td>

Margin left

</td><td>

The left margin of your video component in pixels.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile Card Builder user interface](mcb-stage-ui.md)

