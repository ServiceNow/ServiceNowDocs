---
title: Create multiple Now Assist context menu skill configurations
description: Create multiple Now Assist context menu configuration for the same field and table.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-14"
reading_time_minutes: 2
breadcrumb: [Use Now Assist context menu for custom skill deployment, Now Assist context menu, Exploring Now Assist, Now Assist, Enable AI experiences]
---

# Create multiple Now Assist context menu skill configurations

Create multiple Now Assist context menu configuration for the same field and table.

## Before you begin

You can now have multiple Now Assist context menu configurations on the same record form and field. You just have to create the required configuration and add to the form or field.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Experiences** &gt; **Now Assist Context Menu**.

2.  Select **Configurations** tab in the Now Assist context menu home page.

3.  Select **Create New**.

4.  Enter values for the following fields on the Configure Now Assist context menu form.

    -   Workflow
    -   Product
    -   Name
5.  Select **Start Configuration**.

6.  Provide the following details in the **General details** page, on the configuration form:

    -   Name
    -   Description
    -   Table name
    The UI now allows you to add multiple configurations to the same field without any errors. This is applicable only if you select Record form field.

7.  Select Record form field as the location, to add the trigger for the Now Assist context menu on the UI16 form.

8.  Add and select one or multiple form fields in the **Form Fields** field.

9.  Select **Save and continue**.

    You will land on the Configure experience page. You will see a table that lists the skill configurations along the order value, for the selected record field. The precedence is always given to the configuration with the lowest order value.

    **Note:**

    -   In case there is a conflict due multiple configurations to the same field in a table,the precedence is give to the configuration with the lowest order value.
    -   In case there are multiple configurations, but the order value is same, the configuration with the most recently modified date is applied to field.
10. Select options for the following fields on the Configure experience page:

    -   Default Action
    -   Actions
    -   Refinement actions
    -   Turn on to prevent access refinement action
    -   Maximum refinements
    -   Actions for generated content
    -   Enable support for extended tables.
    Provide the same information for each of the form fields you have selected.

    **Note:**

    -   To disable the inheritance model for child tables, toggle off the **Enable support for extended tables** button. This model applies the parent table's configurations to a child table if the child table does not have its own configuration.
    -   Do not merge configurations. Use only the child table configuration and retrieve configurations from the child table.
    -   Apply the merging logic to use the lowest value configuration for the fields.
    If you proceed without providing the required values for each form field, system will prompt you to provide configuration.

11. Select **Save and continue** once you review and edit the values, if required.

    You will land on the Review and activate page.

12. Select an option from the **Select a record to test the configurations** drop-down menu.

13. Select **Preview** and **Done**.


