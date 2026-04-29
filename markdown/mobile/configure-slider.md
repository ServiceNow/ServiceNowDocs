---
title: Configure a slider option for a number input
description: Create a slider option for a number input on your input form screen. Sliders help users visualize the input range and reduce errors by limiting choices to defined minimum and maximum values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Number render types and compatible input attributes, Input form screen attributes for inputs, Configure inputs, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a slider option for a number input

Create a slider option for a number input on your input form screen. Sliders help users visualize the input range and reduce errors by limiting choices to defined minimum and maximum values.

## Before you begin

Role required: admin

This task assumes that you already have the basis of an input form screen configured before adding the slider option for a number input. For more information, see [Configure an input form screen](parameter-screen-config.md).

## About this task

Creating a slider render type is more involved than for the other render types: integer, line, percentage. The configuration involves the creation of multiple input attributes, some are required and others are optional. To create a slider option for a number input, you must have at least the following configurations:

-   RenderType is Slider
-   Min input attribute
-   Max input attribute
-   StepSize input attribute

You can add additional number input attributes to the ones listed. For a complete list, check the Number inputs section in [Input form screen attributes for inputs](../reference/parameter-screen-var-attr.md).

To view how different types of sliders display, see [Slider types and their input attributes](../reference/slider-input-attributes.md).

|Slider containing a reference point|Decorative slider with number a textual indicator|
|-----------------------------------|-------------------------------------------------|
|![A slider with a reference point of zero in the center of high and low values.](../image/ifs-slider-reference.png)|![A colorful decorative slider with the marker placed in the orange area, indicating that the quality of service is marked as poor.](../image/ifs-slider-decorative.png)|

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the  **Screens** category.

4.  Select either an existing input form screen or select **New**, then the Input form and then **Continue**.

5.  Scroll down to the Inputs section of the form and then either select an input to modify it or select  **New**  to create an input.

    The Input form appears. For more information about configuring inputs, see [Configure input form screen inputs](param-screen-config-inputs.md).

6.  In the **Input type** field within the **Settings** area, select **Number**.

7.  Complete any other fields as required and select **Save**.

8.  Select **RenderType** from the **Name** field, select **Slider** from the **Value** field, then select **Save**.

9.  Select the Input record from the navigation tree, then select **New** in the Input attributes area.

10. From the **Name** field, select **Min** and enter the lowest value to be displayed at the start of your slider, then select **Save**.

11. Select the Input record from the navigation tree, then select **New** in the Input attributes area.

12. From the **Name** field, select **Max** and enter the highest value to be displayed at the end of your slider, then select **Save**.

13. Select the Input record from the navigation tree, then select **New** in the Input attributes area.

14. From the **Name** field, select **StepSize** and enter a number that represents each incremental number on the slider, then select **Save**.

    **Note:** The steps must be a number divisible between the max and min size input attributes.

15. Add any additional input parameters that are applicable to the slider you want to create.

    For a list of the slider types, see [Slider types and their input attributes](../reference/slider-input-attributes.md).

    **Note:** If you select the Decoration input attribute, which displays sections on the slider with corresponding labels, you must apply additional configuration. For more information, see [Configure a decorative slider](decorative-slider.md).

16. Select **Save**.


