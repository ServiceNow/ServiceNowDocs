---
title: Create and manage software suites using the legacy Software Asset Management plugin
description: Software uses the concept of suites instead of bundles.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage software models using the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create and manage software suites using the legacy Software Asset Management plugin

Software uses the concept of suites instead of bundles.

A software suite is a group of related software offered as one unit. An example is the Microsoft Office Professional suite of office productivity software tools that includes Powerpoint, Word, Excel, Outlook, and Access. You can use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to create suites and add components to the suite so that the licenses your organization own are counted accurately.

For any software model, you have the option to specify whether the model is a suite \(parent\) or a component \(child\). A software model can be a component in multiple suites. For example, Microsoft Word is a component in Microsoft Office Standard and Microsoft Office Professional. Although you can set a single software model as both a suite and a component, software is not typically sold as nested suites.

Use the **Inference percent** and **Inference mandatory** options for even greater control of suites.

-   **Inference percent**: specifies what percentage of the components in the suite must be installed for the software to be identified as a suite.
-   **Inference mandatory**: enforces that a specific component in a suite must be installed to infer that the suite is installed.

For example, specify the **Inference percent** as 80% and set the **Inference mandatory** option to **true** on Microsoft Access. These settings specify that Microsoft Access must be installed, along with 3 out of 4 other products \(Microsoft Word, Microsoft Excel, Microsoft PowerPoint, and Microsoft Outlook\) to infer that Microsoft Office Professional is installed.

![The interference percent and Interference mandatory fields](../image/InferenceOptionsCalgary.png "The interference percent and interference mandatory fields")

To make the new software model record a parent record in a suite:

1.  Open a software model record.
2.  In the Suite Components section, double-click an empty row under **Suite child**.

    ![The suite child](../image/SoftwareParentSuiteCalgary.png "Suite child")

3.  Add the software to include in the suite.
4.  \[Optional\] Set the **Inference mandatory** option to **true** if the software must be installed to count the model as a suite.
5.  Repeat as necessary.

To make the new software record a child item:

1.  Open a software model record.
2.  In the Suite Parents section, double-click an empty row under **Suite parent**.

    ![The Suite parent](../image/SoftwareChildSuiteCalgary.png "Suite parent")

3.  Add the suite to which this software model should belong.
4.  Repeat as necessary.

    **Note:** When a change is made to a suite, a scheduled job called **Calculate suites \[Software Suite Model\]** is created. The job runs instantly, calculates any suites, and then deletes itself. The calculations are stored in the cmdb\_sam\_sw\_install table under inferred suite.


**Parent Topic:**[Manage software models using the legacy Software Asset Management plugin](../task/t_ManagingSoftwareModels.md)

