---
title: Create a Microsoft PowerPoint template
description: Configure the Export to PowerPoint add-in in your Microsoft PowerPoint to interact with your instance and fetch the data required to generate and download your status reports. Create your own custom template with the required data to generate a report, based on the reporting needs of your organization.
locale: en-US
release: yokohama
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Use, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Create a Microsoft PowerPoint template

Configure the Export to PowerPoint add-in in your Microsoft PowerPoint to interact with your instance and fetch the data required to generate and download your status reports. Create your own custom template with the required data to generate a report, based on the reporting needs of your organization.

## Before you begin

-   Let us connect your instance to the Microsoft PowerPoint using the add-in login and create a template Portfolio Planning to generate a report for epic details.
-   Role required: sn\_ppt\_export.ppt\_user

## Procedure

1.  Open your Microsoft PowerPoint application and select the ServiceNow add-in icon \(![ServiceNow Export to PowerPoint add-in.](../image/icon-servicenow-addin.png)\) on the **Home** tab.

    A side panel appears with a login option to access your ServiceNow instance.

2.  Select **Log in**.

3.  Enter your ServiceNow instance credentials and select **Log in**.

    A prompt with your instance details is displayed.

4.  Check your instance details and select **Allow**.

    The landing page of the add-in appears on the side panel.

    ![Export to PowerPoint add-in landing page.](../image/icon-ppt-addin-landing-page.png)

5.  Select **Personal portfolio report** from the Type list.

    Select the data type you want to populate.

    -   Text – Text entries from the parent table. Example: Portfolio name, owner name, and so on.
    -   Table – Table entries mapped using [related tables](manage-components-export-ppt.md).
    -   Repeater – To populate additional details for each of the selected records.
    -   Line and Bar chart – Graph entries mapped using [scripted elements](manage-components-export-ppt.md).
    **Note:** While creating a template, you can:

    -   Change the font size and color for the token values to reflect the same in your status report.
    -   Move around the token to place them in a required format.
    -   Add your custom or organization logos on the slides.
    -   Resize the chart tokens according to the requirement.
    You can customize data retrieval for template tokens by appending link attributes. The following attributes are available:

    |Attribute|Description|Example|
    |---------|-----------|-------|
    |orderByColumnName|Sorts the data by the specified column name in ascending or descending order.|`orderByColumnName=priority^orderByDirection=asc`|
    |filterQuery|Applies an encoded query to filter the data populated in the template token.|`filterQuery=state=2^priority=1`|
    |maxRows|Limits the maximum number of rows returned for a table or repeater token.|`maxRows=10`|

    Apply these attributes by appending them to the token URL in the template field properties. For details on configuring related tables and scripted elements, see [Manage components](manage-components-export-ppt.md).

6.  To populate the Portfolio name on the first slide:

    1.  Select **Text** from the data type.
    2.  Filter the Column list to locate Name and select it. A token value representing the portfolio name is generated in the subsequent empty text box.
    3.  Select the **Copy text** button to copy the token.
    4.  Paste the token on the slide.
    ![Portfolio name selection.](../image/portfolio-name.gif)

    Add a new slide to Microsoft PowerPoint, insert a table with three columns and two rows to generate the Epics with their numbers, status, and due date.

7.  To populate Epics details such as numbers, status, and due date:

    1.  From the add-in landing page, select **Table** from the Data list.

        Use the **Back** \(![PPT add-in back button.](../image/ppt-addin-back-button.png)\) button to go back to the add-in landing page.

    2.  Select **Epic** from the Related table list.
    3.  From the Related table \(optional\) list, select a related table to the Epic.
    4.  Select the number of rows that you want to populate and By default, five rows are selected.

        You can select a minimum of one row and a maximum of 10 rows.

    5.  Use the filter icon to see any existing filter or to define a condition to populate the data.

        Here, we’re picking Epics which are in either Ready or Work in progress state with a deadline on April 30.

    6.  Select **Next**.
    7.  Select **Number** from the Column list.
    8.  Copy the token value and paste it in the table.
    9.  Similarly, copy and paste the token values of **State** and **Assigned to** fields from the Column list.

        ![Epics details selection.](../image/epics-selection.gif)

    Add slide to Microsoft PowerPoint.

8.  To populate the required details of each of the selected records:

    1.  From the add-in landing page, select **Table** from the Data list.

        Use the **Back** \(![PPT add-in back button.](../image/ppt-addin-back-button.png)\) button to go back to the add-in landing page.

    2.  Select **Repeater** from the Data list.
    3.  Select **Epic** from the Related table list.
    4.  Add the required filter using the filter option and select **Next**.
    5.  Select the required fields to copy and paste the token on the slide.
    6.  Copy and paste the repeater token to the slide

        **Note:** The repeater token doesn’t generate any values in the status report.

    ![GIF showing repeater token selection while creating PowerPoint template.](../image/repeater-token-export-ppt.gif)

    Add a new slide to Microsoft PowerPoint.

9.  To populate a line or bar chart:

    1.  From the add-in landing page, select **Line Chart** or **Bar Chart** from the Data list.

        Use the **Back** \(![PPT add-in back button.](../image/ppt-addin-back-button.png)\) button to go back to the add-in landing page.

    2.  From the Select a chart \(defined using scripted elements\) list, select a chart you want to populate for your report and select **Next**.
    3.  Select the **Copy to clipboard** button to copy the chart token.
    4.  Paste the token on a slide.
    ![Line chart selection for Export to PowerPoint.](../image/select-line-chart-export-ppt.gif)

10. Save the Microsoft PowerPoint file in the `.pptx` format with a maximum of 50 slides and file size not exceeding 15 MB.

    **Note:** The Export to PowerPoint for Strategic Portfolio Management application comes with default templates which you can use to generate reports and consider as a reference to create templates.


**Parent Topic:**[Using Export to PowerPoint](../concept/using-export-to-ppt.md)

