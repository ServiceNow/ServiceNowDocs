---
title: Use the XmlTemplate component
description: Create templates from existing XML or PDF documents by adding custom data or fields to the documents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Modellers, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the XmlTemplate component

Create templates from existing XML or PDF documents by adding custom data or fields to the documents.

## Before you begin

Role required: none

## About this task

The XmlTemplate component also provides methods to work with the templates. To expose the methods, see [View the XmlTemplate methods](view-xmltemplate-methods.md).

## Procedure

1.  In the Toolbox pane, navigate to **Data Modellers** &gt; **XMLTemplate**.

2.  Drag the XmlTemplate component under Global Objects in the Project Explorer.

3.  Click to expand the Global Objects node.

4.  Right-click XmlTemplate.

5.  Click **Configure**.

6.  Under the **TEMPLATES** section, click the add templates icon \(![Add templates icon.](../image/add-image-icon.png)\).

7.  Click the template added.

    A new template is by default named in the `Template<number>` format. You can rename it from the Name field in the PROPERTIES section on the XML TEMPLATE DESIGNER window.

8.  To select an existing PDF or XML document, in the **XML/PDF File** field, click the Load XML or PDF File icon \(![Load XML or PDF File icon.](../image/folder-icon.png)\).

9.  Select the XML or PDF file from the local drive.

    The preview displays the document data under corresponding XML tags.

10. To add a field to the file, right-click the required XML tag.

11. Click one of the following field options.

    -   Text
    -   Text Array
    -   Table
    -   XPath
    You’ve successfully updated the template by adding fields.

12. In the Name field of the PROPERTIES section, provide a custom name to the template you added.

13. Repeat the steps to add more fields.

14. Close the XML TEMPLATE DESIGNER window.


**Parent Topic:**[Data Modellers](../concept/data-modellers.md)

