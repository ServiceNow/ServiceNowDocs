---
title: Manage a SAM Foundation software suite
description: Create a suite and add the corresponding components to the suite so the rights that your organization owns are counted accurately during reconciliation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/software-asset-management-foundation-plugin/manage-samf-software-suite.html
release: brazil
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Setting up Basic Software Asset Management plugin, Basic Software Asset Management, ITSM Software Asset Management, Asset Management common applications, IT Service Management]
---

# Manage a SAM Foundation software suite

Create a suite and add the corresponding components to the suite so the rights that your organization owns are counted accurately during reconciliation.

A software suite is a group of related software offered as one unit. An example is the Microsoft Office Professional suite of office productivity software tools that includes PowerPoint, Word, Excel, Outlook, and Access.

For any software model, you have the option to specify whether the model is a suite \(parent\) or a component \(child\). A software model can be a component in multiple suites. For example, Microsoft Word is a component in Microsoft Office Standard and Microsoft Office Professional. Although you can set a single software model as both a suite and a component, software is not typically sold as nested suites.

When a suite parent is detected during reconciliation, the suite components don't count for the individual license.

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but can't administer all aspects of software models.

## Automated suite inference

The Software Asset Management application calculates the inference percentage in automated mode based on your software install footprint and current entitlements. For example, if you have only Windows Server installations, no System Centre installations, and hold entitlements only for CIS, the inference percentage will be set to 0%. This value is calculated during reconciliation so you don't have to manually configure it.

If you prefer to calculate the inference percentage manually and revert to the default 75%, you must override the automated option. To override, clear the **Automatic determination of inference** option after navigating to **Product Catalog** &gt; **Product Model** &gt; **Software Models** &gt; **Suite Components**.

If the system property **com.snc.sam.auto\_suite\_inference** is set to true, the inference percent is automatically calculated. As a result, the parent software model suite is automatically inferred for a software model based on its child software models. An explanation of the inferred suite is included on the Software Model page that specifies the reason this install was inferred, the suites considered for inference, and the reason for selecting those suites.

Use the **Inference percent** or **Inference Number**, and **Mandatory** fields when the suite parent is not defined in the install table.

-   **Inference percent**: Specifies what percentage of the components in the suite must be installed for the software to be identified as a suite.
-   **Inference Number**: Specifies the number of components installed for the suite.
-   **Mandatory**: Enforces whether a specific component in a suite must be installed to infer that the suite is installed. Choices are: Optional, Always Mandatory, Mandatory Group.

For example, you set the **Inference percent** to 75% and the **Mandatory** field to **Always Mandatory** for Microsoft Access. For Microsoft Office Professional to be inferred on a device, Microsoft Access must be installed along with at least three of the following four components: Microsoft Word, Microsoft Excel, Microsoft PowerPoint, and Microsoft Outlook.

**Parent Topic:**[Setting up Basic Software Asset Management plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/software-asset-management-foundation-plugin/t_SAMSetupSAMF.md)

