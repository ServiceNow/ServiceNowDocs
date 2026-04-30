---
title: Managing software suites
description: Simplify licensing and lower the cost of licenses from vendors. Get visibility into your complex suite licenses, manage compliance, and optimize your spending on these licenses.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Software Asset Management software suites, Explore, Software Asset Management, IT Asset Management]
---

# Managing software suites

Simplify licensing and lower the cost of licenses from vendors. Get visibility into your complex suite licenses, manage compliance, and optimize your spending on these licenses.

Create a suite and add components to the suite so that your organizations' rights are accurately counted during reconciliation.

A software suite is a group of related software that is offered as one unit. An example is the Microsoft Office Professional suite that includes PowerPoint, Word, Excel, Outlook, and Access.

Another example of a server-side suite is the Microsoft Core Infrastructure Server \(CIS\) Suite. The CIS Suite can include the Windows Server software as well as the System Center suite, which includes Configuration Manager, Operations Manager, and other titles. CIS Suite, which is licensed with Microsoft server metrics \(Per Core, Per Core \(with CAL\), Per Instance, Per Processor, Per Server\), are considered during reconciliation.

For any software model, you can specify whether the model is a suite \(parent\) or a component \(child\). A software model can be a component in multiple suites. For example, Microsoft Word is a component in two suites: Microsoft Office Standard and Microsoft Office Professional. Although you can set a single software model as both a suite and a component, software isn’t typically sold as nested suites.

Whenever a software model is automatically created as part of a scheduled job, its child components are automatically created and appear in the [Suite Components](../reference/software-model-fields.md#section_bdp_kmc_xhb) section.

Use the **Inference percent** or **Inference number** and **Mandatory** fields when the suite parent isn’t defined in the install table.

-   **Inference percent**: Specifies the percentage of the components that must be installed for the suite.
-   **Inference Number**: Specifies the number of components installed for the suite.
-   **Mandatory**: Enforces whether a specific component must be installed to infer that the suite is installed. Choices are Optional, Always Mandatory, Mandatory Group.

    **Note:** If two or more software components are part of a Mandatory Group, then at least one of them must be present so that all the software components are considered a suite. This assumes that the inference percent, inference number, and other requirements are also fulfilled.


For example, let's say you specify the **Inference percent** as 75% and set the **Mandatory** field to **Always Mandatory** on Microsoft Access. These settings specify that Microsoft Access must be installed, along with three out of four other products \(Microsoft Word, Microsoft Excel, Microsoft PowerPoint, and Microsoft Outlook\), to infer that Microsoft Office Professional is installed on a device.

When a suite parent is detected during reconciliation, the child components don’t count for the individual license.

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but can’t administer all aspects of software models.

The rules of inference suite ranking are as follows:

-   If one of the software installations belongs to the suite software model, the suite is inferred directly without the need to meet the Inference percentage or the Inference number.
-   If the preceding rule isn’t met, then any suite that meets the Inference percentage or the Inference number on that device can be considered an Inferred suite candidate.
-   The candidate with the highest number of installed components is chosen.
-   If there’s still a tie, the suite with the lower downgrade is chosen. For example, Office 2016 and Office 2013 are both candidates and have the same number of installed components. However, because Office 2013 is the downgraded version of Office 2016, Office 2013 is chosen.
-   If there’s still a tie, the one with the highest percentage of installed components is chosen.

Software Asset Management supports hybrid and subscription-based software suites. In a hybrid software suite, either the suite parent or child component is subscription-based. In a subscription-based software suite, both the suite parent and child component are subscription-based. The license that you use to determine compliance is dependent on whether the suite parent and child component are subscription-based:

-   If only the suite parent is subscription-based, then all the child component installations are inferred as part of the suite parent. You can determine your license compliance using the suite parent license.
-   If only the child component of a suite parent is subscription-based, then the instances of that child component aren’t inferred as part of the suite parent. You can determine your license compliance using the child component license.
-   If both the suite parent and child components are subscription-based, then the instances of the child components are inferred as part of the suite parent. You can determine your license compliance using the suite parent license. For example, Microsoft 365 E5 is a subscription-based software suite that consists of the Office 365 E5, EMS E5, and Windows 10 subscription software. Because both the suite parent and child components are subscription-based, they’re reconciled against the Microsoft 365 E5 parent license.

**Parent Topic:**[Software Asset Management software suites](software-suites.md)

