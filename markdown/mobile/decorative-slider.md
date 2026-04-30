---
title: Configure a decorative slider
description: Create a colored slider option for a number input on your input form screen. Decorative sliders contain sections that can be associated with a specific color and label to aid visual representation. These labels are translatable.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Number render types and compatible input attributes, Input form screen attributes for inputs, Configure inputs, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a decorative slider

Create a colored slider option for a number input on your input form screen. Decorative sliders contain sections that can be associated with a specific color and label to aid visual representation. These labels are translatable.

## Before you begin

Role required: admin

This task assumes that you already have the basis of an input form screen configured before adding the slider option for a number input. For more information, see [Configure an input form screen](parameter-screen-config.md).

## About this task

Creating a slider render type is more involved than for the other render types: integer, line, percentage. The configuration involves the creation of multiple input attributes. Required attributes are Min. Max, and StepSize. For a complete list of input attributes you can use with a number slider, see [Number render types and compatible input attributes](../reference/number-compatible-input-attributes.md).

You must add an additional input attribute called Decoration, which gives the slider a colorful and segmented appearance. A decorative slider has between two through eight sections, where you define a start value and end value. The start value must match the end value of the previous entry. In addition, you must select a color for each section. A JSON example script is provided, which contains four defined sections. This script is editable.

There's an option when configuring a decorative slider type to add translated values, so that users can view the slider in their selected language. For more information, see [Configure translated values for decorative slider](decorative-slider-translation.md).

![A colorful decorative slider with the marker placed in the orange area, indicating that the quality of service is marked as poor.](../image/ifs-slider-decorative.png)

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the  **Screens**  category and then select the input form screen for which you want to configure inputs.

4.  Scroll down to the Inputs section of the form and then either select an input to modify or select  **New**  to create an input.

    The Input form appears. For more information about configuring inputs, see [Configure input form screen inputs](param-screen-config-inputs.md).

5.  In the **Input type** field within the Settings area, select **Number**.

6.  Select **New** in the Inputs attributes area.

7.  Select **RenderType** from the **Name** field, select **Slider** from the **Value** field, then select **Save**.

8.  Create and save the input attributes for Min, Max, and StepSize and define their values.

    For configuration details, see [Configure a slider option for a number input](configure-slider.md).

    **Note:** RenderType, Min, Max, and StepSize are required input attributes for sliders. Other input attributes are optional. For a complete list of input attributes, see the Number inputs section within the topic [Input form screen attributes for inputs](../reference/parameter-screen-var-attr.md).

9.  Select **New** in the Inputs attributes area.

10. Select **Decoration** from the **Name** field.

    A JSON script displays with a default script, which you can edit as needed.

    ```
      "Range": [ 
    
        { 
          "Label": "Critically Low", 
          "StartValue": 0, 
          "EndValue": 10, 
          "Color": "#000000" 
        }, 
        { 
          "Label": "Low", 
          "StartValue": 10, 
          "EndValue": 50, 
          "Color": "Slider-2" 
        }, 
        { 
          "Label": "Medium", 
          "StartValue": 50, 
          "EndValue": 75, 
          "Color": "Slider-1" 
        }, 
        { 
          "Label": "High", 
          "StartValue": 75, 
          "EndValue": 100, 
          "Color": "Slider-0" 
        } 
      ] 
    } 
    ```

    This example script lists four sections contained within a slider. A decorative slider can contain between two and eight sections. Each segment has the following values:

    -   Label: A name attributed to each section. In the example, they are: Critically low, Low, Medium, and High. The names are editable.

        **Note:** The names contained within the label value can be translated. To do this, double curly braces must be added to the `Label` value. For example, `Medium` becomes `{{Medium}}`. For more information, see [Configure translated values for decorative slider](decorative-slider-translation.md).

    -   StartValue and EndValue: These can be any value. Usually these values are divisible by the number of sections. The StartValue of one section must correspond to the EndValue of the previous section.
    -   Color: The color value can either be a HEX code or the label of a variable from your current mobile theme. The JSON script provides the following default colors:

        -   `#000000` corresponds to green.
        -   `Slider-1` corresponds to yellow.
        -   `Slider-2` corresponds to orange.
        -   `Slider-3` corresponds to red.
        For a complete list of variables, navigate to **All** &gt; **sys\_ux\_style.list** and search for Mobile Colors Default.

11. Select **Save**.


## What to do next

You can add translated text to each of the text values displays on your slider. For more information, see [Configure translated values for decorative slider](decorative-slider-translation.md).

