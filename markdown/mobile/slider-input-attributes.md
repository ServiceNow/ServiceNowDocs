---
title: Slider types and their input attributes
description: Review the sections to see slider type examples and learn which input attributes are used to create them.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Number render types and compatible input attributes, Input form screen attributes for inputs, Configure inputs, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Slider types and their input attributes

Review the sections to see slider type examples and learn which input attributes are used to create them.

The sections within this topic show the types of sliders that you can create and the input attributes needed to create them. For more information about all the input attributes, see the Number inputs section in the topic [Input form screen attributes for inputs](parameter-screen-var-attr.md).

**Note:**

-   The input attribute DefaultValue is the numerical value displayed when a user first views the slider. In some of the sections below, the DefaultValue input attribute is marked as optional, because you're unable to tell if the attribute was used in the displayed images.
-   The input attribute EnforceStepSize isn't a visual attribute. It's marked as Optional in some of the sections, as you're unable to see if it has been used from the images displayed.

## Default value slider

![Slider with values between 1 and 100 and a default number of 50.](../image/ifs-slider-default.png)

A default value provides a starting point to help users understand a typical or suggested setting. The following are input attributes that are required to create a slider with a displayed default value.

-   Min
-   Max
-   DefaultValue
-   StepSize
-   EnforceStepSize: Optional

## Visual steps slider

![A visual steps slider with a range of 0 to 20. Each step marks an increase of 2. The number displayed is 12.](../image/ifs-slider-visual-steps.png)

A visual step slider makes it clear to users what each position on the slider represents. The following are input attributes that are required to create a slider containing visual steps.

-   Min
-   Max
-   DefaultValue: Optional
-   StepSize
-   VisualStepsEnabled
-   EnforceStepSize: Optional

## Enforced step size slider

![A enforced step slider with an error message stating that the selected number of 0.1 is not a valid and needs to be within a range of 0.0 and 0.5.](../image/ifs-slider-enforced-step-size.png)

Use an enforced step size slider to make sure that users can only select specific predefined incremental values. This slider is a more appropriate choice than a visual step slider, if the range of values is large. The image shows a scenario where the chosen figure doesn't conform with the enforced incremental value. As a consequence, an error message displays. The following are input attributes that are required to create a slider with enforced steps.

-   Min
-   Max
-   DefaultValue: Optional
-   StepSize
-   EnforceStepSize

## Reference point slider

![Slider with values of minus 200 and 200. With a reference point of zero in the middle of the slider.](../image/ifs-slider-reference.png)

Use a reference point within a slider to help users understand where they are within the range of possible values. For example, a reference point at the center, shows users that they're setting a value higher or lower than the expected value. The following are input attributes that are required to create a slider containing a reference point.

-   Min
-   Max
-   DefaultValue: Optional
-   StepSize
-   ReferencePoint
-   EnforceStepSize: Optional

## Decorative step slider

![The render type called slider showing an input called Quality of service with the indicator placed in the orange area, which is listed as Poor.](../image/ifs-slider-decorative.png)

Use a decorative step slider to improve the overall look and feel of the user interface. This is important in design-focused applications where the visual experience is a key aspect. This slider type provides three visual indicators: the numeric value, the label text \(for example, good, poor, and bad\), and the colored slider. These colorful visual elements can aid accessibility. For example, distinct colors and labels for each step can help users better understand the slider's position and options. The following are input attributes that are required to create a decorative step slider.

-   Min
-   Max
-   DefaultValue: Optional
-   StepSize
-   EnforceStepSize: Optional
-   Decoration

For more information, see [Configure a decorative slider](../task/decorative-slider.md).

