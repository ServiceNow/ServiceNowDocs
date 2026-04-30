---
title: Create Now Assist context Menu configuration
description: Create a new Now Assist context Menu configuration to deploy and activate a custom skill.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Use Now Assist context menu for custom skill deployment, Now Assist context menu, Exploring Now Assist, Now Assist, Enable AI experiences]
---

# Create Now Assist context Menu configuration

Create a new Now Assist context Menu configuration to deploy and activate a custom skill.

## Before you begin

To configure custom skills in action, ensure that the skill is activated in Now Assist.

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Experiences** &gt; **Now Assist Context Menu**.

2.  Select **Configurations** tab in the Now Assist context menu home page.

3.  Select **Create New**.

4.  Enter values for the following fields on the Configure Now Assist context menu form.

    -   Workflow
    -   Product
    -   Name
5.  Select **Start Configuration**.

6.  Provide the following details in the **General settings** tab, on the configuration form:

    -   Name
    -   Description
    -   Table name
7.  Select a location where you want to add the trigger for the Now Assist context menu.

    The options are:

    -   Record form field: Select this option to add the trigger on UI16 form
    -   Custom location: Select this option to add the trigger on any other desired location.
8.  If you select Record form fields, add the form fields where you want the Now Assist context menu icon.

9.  If you select Custom location, choose the context menu display type.

    Choose between the following options of display:

    -   Modeless window: A draggable and resizable dialog box.
    -   Embedded card: A fixed window displayed on the page.
    If you select **Custom location**, ensure that you have completed the UIB Now Assist context menu component configurations. For setup information see [Now Assist context menu UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/sn-now-assist-context-menu/uib-setup).

10. Select **Save and continue**.

    You will land on the Configure experience tab.

11. Select options for the following fields on the Configure experience tab:

    -   Actions
    -   Refinement actions
    -   Turn on to prevent access refinement action
    -   Maximum refinements
    -   Actions for generated content
    -   Enable users to provide feedback on the recommendations
    Provide the same information for each of the form fields you have selected.

    If you proceed without providing the required values for each form field, system will prompt you to provide configuration.

12. When prompted, select **Yes, apply** on the Apply Configurations prompt if you want to apply the same configurations.

13. Select **Save and continue** once you review and edit the values, if required.

    You will land on the Review and activate tab.

14. Select an option from the **Select a record to test the configurations** drop-down menu.

15. Select **Preview** and **Done**.


