---
title: Manage a SAM Foundation software suite
description: Create a suite and add the corresponding components to the suite so the rights that your organization owns are counted accurately during reconciliation.
locale: en-US
release: xanadu
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Software Asset Management Foundation plugin, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Manage a SAM Foundation software suite

Create a suite and add the corresponding components to the suite so the rights that your organization owns are counted accurately during reconciliation.

A software suite is a group of related software offered as one unit. An example is the Microsoft Office Professional suite of office productivity software tools that includes PowerPoint, Word, Excel, Outlook, and Access.

For any software model, you have the option to specify whether the model is a suite \(parent\) or a component \(child\). A software model can be a component in multiple suites. For example, Microsoft Word is a component in Microsoft Office Standard and Microsoft Office Professional. Although you can set a single software model as both a suite and a component, software is not typically sold as nested suites.

Use the **Inference percent** and **Mandatory** fields when the suite parent is not defined in the install table.

-   **Inference percent**: Specifies what percentage of the components in the suite must be installed for the software to be identified as a suite.
-   **Mandatory**: Enforces whether a specific component in a suite must be installed to infer that the suite is installed. Choices are: Optional, Always Mandatory, Mandatory Group.

For example, say you specify the **Inference percent** as 80% and set the **Mandatory** field to **Always Mandatory** on Microsoft Access. These settings specify that Microsoft Access must be installed, along with three out of four other products \(Microsoft Word, Microsoft Excel, Microsoft PowerPoint, and Microsoft Outlook\) to infer that Microsoft Office Professional is installed on a device.

When a suite parent is detected during reconciliation, the suite components do not count for the individual license.

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but cannot administer all aspects of software models.

**Parent Topic:**[Setting up Software Asset Management Foundation plugin](../task/t_SAMSetupSAMF.md)

