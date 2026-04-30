---
title: Configure input form sections
description: Input form sections are reusable components consisting of grouped inputs. You can associate these sections with any number of input form pages.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure input form sections

Input form sections are reusable components consisting of grouped inputs. You can associate these sections with any number of input form pages.

## Before you begin

You must create an input form screen that contains inputs before you create sections. For information about creating an input form screen and inputs, see [Configure an input form screen](parameter-screen-config.md) and [Configure input form screen inputs](param-screen-config-inputs.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and then select the input form screen for which you want to configure a section.

4.  Scroll down to the **Input form page display** section and make sure that **Custom page and section setup** is selected.

    If **Custom page and section setup** is not selected, the option to configure Sections does not appear in the form.

5.  Scroll down to the Section mappings section of the form and select **New** to configure an input form screen section.

    The Input Form Section mapping page appears.

6.  Complete the following fields:

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|The name of your section mapping.|
    |Label|The display name for your input form section.|
    |Active|Sets whether the section displays.|
    |**Settings**|
    |Order|Enter a number to define the placement order of this section within the page.|

7.  In the Input form section area, **Choose** an existing input form section or select **New** to create an input form section.

    The Input Form Section page appears.

8.  Complete the following fields:

    |Field|Description|
    |-----|-----------|
    |Name|The name of your section.|
    |Inputs|The inputs that appear in your section. Select an existing input or select **New** to create an input.|
    |Variables|The information that is collected automatically or that is defined by default for the input.|

9.  Select **Save**.

10. Map inputs to designated sections.

    1.  Select the input form screen where you want to use the section you configured.

        The input form screen appears.

    2.  Scroll down to the Inputs section and select the input you want to map to a section.

    3.  In the Input form, scroll down to the Input placement section, and make sure that the Input form screen you want to use is selected.

    4.  In the Input form section field, select the section to which you want to map this input.

11. Select **Save**.


## Result

Your input form can contain any number of inputs and reusable sections within any number of pages.

![Input form displaying a page containing inputs and a section.](../image/input-form-screen-sections.png)

## What to do next

There is an option that enables you to control the visibility of an entire section if it contains only descriptive elements and no input fields.

1.  In the web-based UI go to **All** and enter `sys_sg_section_attribute`.
2.  Select **New** and in the **Name** field add the attribute name `HideIfDescriptiveOnly`.
3.  In the **Value** field enter the either true or false. If left blank the default value is false and the descriptive element is shown even if there isn't an input value field.
4.  Select **Save**.

