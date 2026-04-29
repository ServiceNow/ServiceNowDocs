---
title: Save Microsoft Word document as a template
description: Save your Microsoft Word document as a template using the Design template provided in the Document designer, enabling you to create a reusable template in your instance.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Generating reports using Document designer, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Save Microsoft Word document as a template

Save your Microsoft Word document as a template using the Design template provided in the Document designer, enabling you to create a reusable template in your instance.

## Before you begin

Role required:sn\_bcm.admin, sn\_bcm.manager

## About this task

Install and activate the Document designer with Microsoft Word \(sn\_grc\_doc\_design\) plugin. For more information, see [Install Document designer with Microsoft Word](install-document-designer-with-word-plugin.md).

Confirm that you have the templates configured. For more information, see [Set up the template configurations](set-up-document-designer-templates.md).

## Procedure

1.  Navigate to the Microsoft Word document that you want to use for template creation.

    Make sure to relaunch Microsoft Word after installing the add-in.

2.  In Microsoft Word, select **Add-ins** and select **Document Designer**.

3.  Select **Design template** on the ribbon.

4.  To log in to your ServiceNow instance, complete the steps.

    1.  On the ServiceNow login screen, provide your credentials in the **User name** and **Password** fields.

    2.  Select **Log in** using the BCM administrator or BCM manager credentials.

    3.  To enable the ServiceNow add-ins for Microsoft Office 365 application to connect to your ServiceNow account on the instance, select **Allow**.

    On the Document designer pane, the Design template is displayed.

    ![Design template TOC.](../image/design-template.png)

5.  On the Document designer pane, fill in the fields.

    1.  Select the **Data** tab then the **Data element** field and from the list, select the fields you would like to see on the template.

        Only the configured fields are available for selection.

    2.  Move the mouse device at the point where you want to insert data and insert the fields such as Logo, Type, Name.

    3.  Select the **Table** tab, in the **Table element** field, from the list, select the configured table elements that you would like to see on the template.

        For example, the list of top five high priority issues.

6.  To insert a content block with styling that can appear repeatedly, select **Block**.

    1.  In the document, add the content that must be used for repeated styling.

    2.  In the Content block source field, select the item that you want to map to the content block.

    3.  Select **Add content block**.

        The content in the document is wrapped in the content block and the options **Data** and **Table** are available.

    4.  To insert data from the configured columns in the content block, select **Data**.

    5.  Select **Add**.

    6.  To insert content from a table, select **Table**.

        After selecting the table, select **Edit columns** to reorder columns as needed.

    7.  Select **Add**.

        **Note:**

        For best practices, continue these steps:

        -   Keep content blocks separate \(no nesting\).
        -   Use up to 10 images according to block.
        -   Include one table according to content block.
        -   Create up to 2 content blocks according to document.
7.  Save the template and upload it in your instance.

    You can use the saved Microsoft Word document as a template.


**Related topics**  


[Set up Microsoft 365 reporting configuration](https://www.servicenow.com/docs/access?context=configure-o365-reporting-configs&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)

[Add additional reporting configuration filters for a Microsoft 365 configuration record](https://www.servicenow.com/docs/access?context=add-additional-reporting-filters&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)

[Add related fields to a Microsoft 365 configuration record](https://www.servicenow.com/docs/access?context=add-related-fields-0365&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)

