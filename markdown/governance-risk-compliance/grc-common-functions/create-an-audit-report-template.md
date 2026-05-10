---
title: Create an audit report template using ServiceNow Document Designer
description: Use the template configurations to create placeholders for an audit report template tailored to your needs.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure document templates using Document Designer, Common GRC features, Governance, Risk, and Compliance]
---

# Create an audit report template using ServiceNow Document Designer

Use the template configurations to create placeholders for an audit report template tailored to your needs.

## Before you begin

Install and activate the ServiceNow Document Designer with Word \(sn\_grc\_doc\_design\) plugin. For more information, see [Install the ServiceNow Document Designer add-in](install-document-designer.md).

Confirm that you have the templates configured. For more information, see [Configure templates for Document Designer](configure-template-for-document-designer.md).

If you want to insert and update reporting content, set up Microsoft 365 reporting. For more information see, [Set up Microsoft 365 reporting configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configure-o365-reporting-configs.md) and [Add additional reporting configuration filters for a Microsoft 365 configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/add-additional-reporting-filters.md).

Role required: sn\_audit.manager and sn\_grc\_doc\_design.reader

## Procedure

1.  Navigate to the Microsoft Word document that you want to use for template creation.

2.  To create placeholders, select **Design template** On the ribbon.

3.  To log in to your ServiceNow instance, select **Log in** using the audit manager credentials.

    1.  On the ServiceNow login screen, provide your credentials.

    2.  Select **Allow**.

4.  On the ServiceNow Document Designer pane, fill in the following fields.

    1.  In the **Business domain** field, select **Audit**.

    2.  In the **Template configuration** field, select the configuration record you want to insert.

    3.  To confirm the selected template configuration, select **Confirm**.

    4.  Select the **Data** tab then the **Data element** field and from the list, select the fields you would like to see on the template.

        Only the configured fields are available for selection.

    5.  Move the mouse device at the point where you want to insert data and insert the fields such as Logo, Type, Name, and so on.

    6.  Select the **Table** tab, in the **Table element** field, from the list, select the configured table elements that you would like to see on the template.

        For example, the list of top five high priority issues.

5.  To insert a content block with styling that can appear repeatedly, select **Block**.

    1.  In the document, add the content that must be used for repeated styling.

    2.  In the Content block source field, select the item that you want to map to the content block.

    3.  Select **Add content block**.

        The content in the document is wrapped in the content block and the options **Data** and **Table** are available.

    4.  To insert data from the configured columns in the content block, select **Data**.

    5.  Select **Add**.

    6.  To insert content from a table, select **Table**.

        After selecting the table you want, you can select **Edit columns** to reorder columns as needed.

    7.  Select **Add**.

6.  To insert reporting content, select **Insert content** on the ribbon.

    1.  Select the **Data** tab.

    2.  In the **Business domain** field, select **Audit**.

    3.  In the **Reporting item** field, select the configuration record you want.

    4.  In the available fields, make the selections that you would like to see on the template.

        Only the configured fields are available for selection.

    5.  Move the mouse device at the point where you want to insert content and select **Add**.

        The data is inserted in to the template. The inserted text takes the formatting of the document. You can modify the formatting as required.

    6.  Select the **Table** tab.

    7.  In the **Business domain** field, select **Audit**.

    8.  In the **Reporting item** field, select the configuration record you want.

    9.  In the available fields, make the selections that you would like to see on the template.

        Only the configured fields are available for selection.

    10. Move the mouse device at the point where you want to insert the table and select **Add**.

        The table is inserted in to the template. The inserted table takes the formatting of the document. You can modify the formatting as required.

    11. Select the **Chart** tab.

    12. In the **Business domain** field, select **Audit**.

    13. In the **Reporting item** field, select the configuration record you want.

    14. In the available fields, make the selections that you would like to see on the template.

        Only the configured fields are available for selection.

    15. Move the mouse device at the point where you want to insert the chart and select **Add**.

        The chart is inserted in to the template. The inserted chart can be modified according to your preferences. For example, you can change the colors, the type of chart and so on.

7.  To update reporting content, select **Update content**.

    1.  Select the field that you would like to get the updated data for and select **View and refresh links**.

        Only the fields added to the table are available for selection.

        The selected fields and content are updated with the latest data available.

    **Note:**

    To help avoid potential errors:

    -   Don't add a content block within another content block.
    -   Don't add more than 10 images.
    -   Don't add more than one table inside a content block.
    -   Don't add more than two content blocks.
8.  Save the template.


**Related topics**  


[Set up Microsoft 365 reporting configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/configure-o365-reporting-configs.md)

[Add additional reporting configuration filters for a Microsoft 365 configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/add-additional-reporting-filters.md)

[Add related fields to a Microsoft 365 configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/add-related-fields-0365.md)

