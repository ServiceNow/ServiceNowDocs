---
title: Create ServiceNow Otto context menu configuration
description: Create a ServiceNow Otto context menu configuration to deploy and activate a custom skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/create-now-assist-configuration-with-guided-setup.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use ServiceNow Otto context menu for custom skill deployment, ServiceNow Otto context menu, ServiceNow Otto Experiences, Exploring AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Create ServiceNow Otto context menu configuration

Create a ServiceNow Otto context menu configuration to deploy and activate a custom skill.

## Before you begin

To configure custom skills in action, ensure that the skill is activated in ServiceNow Otto.

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **AI Admin Hub** &gt; **AI Experiences** &gt; **ServiceNow Otto Context Menu**.

2.  Select **Configurations** tab in the ServiceNow Otto context menu home page.

3.  Select **Create New**.

4.  Enter values for the following fields on the Configure ServiceNow Otto context menu form.

    -   **Workflow**
    -   **Product**
    -   **Name**
5.  Select **Start Configuration**.

6.  Enter the following details on the **General details** page.

    -   **Name**
    -   **Description**
    -   **Table name**
7.  Select a location where you want to add the trigger for the ServiceNow Otto context menu.

    The options are:

    -   Record form field: Select this option to add the trigger on UI16 form.
    -   Custom location: Select this option to add the trigger on any other desired location.
8.  If you select Record form fields, add the form fields where you want the ServiceNow Otto context menu icon.

    **Note:** ServiceNow Otto context menu can only be set up at the table level. Filtering or configuring options based on specific record conditions is not supported.

9.  Select **Custom location**, choose the context menu display type.

    Choose between the following options of display:

    -   Modeless window: A draggable and resizable dialog box.
    -   Embedded card: A fixed window displayed on the page.
    If you select **Custom location**, confirm that you have completed the UIB Now Assist context menu component configurations. For setup information see [Now Assist context menu UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/sn-now-assist-context-menu/uib-setup).

10. Select **Save and continue**.

    The Configure experience page opens.

11. Select options for the following fields on the Configure experience page.

    -   **Actions**
    -   **Refinement actions**
    -   **Turn on to prevent access refinement action**
    -   **Maximum refinements**
    -   **Actions for generated content**
    -   **Enable users to provide feedback on the recommendations**
    Provide the same information for each of the form fields you have selected.

    If you proceed without providing the required values for each form field, a prompt appears, requesting the required configuration.

12. When prompted, select **Yes, apply** on the Apply Configurations prompt if you want to apply the same configurations.

13. After reviewing and editing the values, select **Save and continue**.

    The Review and activate page opens.

14. From the **Select a record to test the configurations** list, select a record.

15. Select **Preview** and **Done**.


**Parent Topic:**[Use ServiceNow Otto context menu for custom skill deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/use-now-assist-context-menu-for-custom-skill-deployment.md)

