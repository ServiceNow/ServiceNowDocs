---
title: Software suites inference
description: Suite inference is used to determine whether the software is part of a suite and to infer the best or efficient suite to use when licensing.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Software Asset Management software suites, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software suites inference

Suite inference is used to determine whether the software is part of a suite and to infer the best or efficient suite to use when licensing.

This video explains the software inference feature and how the Software Asset Management application works with this feature. 

## Suite inference flow

The process of suite inference is divided into two stages:

-   Building the suite structure.
-   Inferring the best suite for the software installation or subscription records.

After the suite structure is built based on the entitlements, software models, and suite relationships, the installs and subscription records are processed.

After the suite engine runs, the Inferred suite column of all install and subscription records that are part of a suite is stamped with a reference to the software model of the most optimal suite parent. For more information about the rules ranking, see the **Suite inference rules**. Entitlements for this software model license are each stamped record.

The suite engine prioritizes subscription suite models and inferences on software subscription records. Next, on-premises suite models and software installation records are inferred.

When a suite parent licensing is used, the individual child components licensing isn't used.

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but can’t administer all aspects of software models.

The system property **Use component licenses to optimize compliance when suite licenses run out** is set by default to **false** for Microsoft license metrics, which enables you to use both suite component and suite parent licenses. This property only applies to Microsoft license metrics.

## Inference options

Use the **Mandatory** and the **Inference option** fields when the suite parent isn’t defined in the install table.

The **Mandatory** field enforces whether a component must be installed to infer that the suite is installed. Choices are **Optional**, **Always Mandatory**, and **Mandatory Group**.

The **Inference option** field contains the following options:

-   Number: Specifies the number of components installed for the suite. The number can be any non-negative number.

    **Note:** For any new software models being created with suite components, the **Number** option is selected by default.

-   Percent: Specifies what percentage of the components must be installed for the suite.

    **Note:** For existing software models with suite components that were using the inference percent, the **Percent** option is selected by default. However, you can choose to use the **Number** option.


If the system property **Use component licenses to optimize compliance when suite licenses run out** is set to true, the inference number and inference percent specifies a threshold to determine whether the suite or component licensing is optimal.

To illustrate the usage of the inference number, consider the scenario where Microsoft Office has an inference number of 2. If you have two Microsoft Office components such as Microsoft Word and Microsoft Excel, the inference number suggests using the Microsoft Office license instead of individual components.

To illustrate the usage of the inference percent, consider a scenario where Core Infrastructure Suites\(CIS\) has two components such as Windows Server and System Center with an inference percent of 50%. This inference percent suggests using the CIS license when more than 50% of the individual components are installed. When less than 50% of the individual components are installed, using the component licenses is optimal.

## Suite inference rules

The rules of suite inference ranking are as follows:

1.  If one of the software installations belongs to the suite software model, the suite is inferred directly without the need to meet the Inference percentage.
2.  If the first rule isn’t met, then any suite that meets the Inference percentage on that device can be considered an Inferred suite candidate.
3.  The candidate with the highest number of installed components is chosen.
4.  If there’s still a tie, the suite with the lower downgrade is chosen. For example, Office 2016 and Office 2013 are both candidates and have the same number of installed components. However, since Office 2013 is the downgrade of Office 2016, Office 2013 is chosen.
5.  If there’s still a tie, the one with the highest percentage of installed components is chosen.

## Suite inference rules for Microsoft license metrics

Based on the system property **Use component licenses to optimize compliance when suite licenses run out**, the Software Asset Management application uses suite or component licenses. For example, if you have both Core Infrastructure Server \(CIS\) suites and Windows Server installations, both have their individual licenses. If Windows Server installations are discovered, then the Software Asset Management application will first license using the available Windows Server licenses. Following the utilization of all the Windows Server licenses, the CIS licenses will be used.

When the system property **Use component licenses to optimize compliance when suite licenses run out** is set to true, the rules ranking for Microsoft license metrics are as follows:

1.  If there are multiple suites that can be inferred for the component, then the suite which meets the inference percent is preferred.
2.  The suite candidate with the highest number of installed components is preferred.
3.  If there’s still a tie, the suite with the lower downgrade rights is chosen. For example, CIS 2019 and CIS 2016 are both candidates and have the same number of installed components. However, since CIS 2016 is the downgrade of CIS 2019 and it has fewer downgrade rights, CIS 2016 is chosen.
4.  The parent suite that meets the inference percent is preferred over the child suite. If the parent suite doesn't meet the inference percent, the child suite is preferred.
5.  If there’s still a tie, the one with the highest percentage of installed components is preferred.

## Use case for suite inference

As an example, let's say you specify the **Inference percent** as 75% and set the **Mandatory** field to **Always Mandatory** on Microsoft Access. These settings specify that Microsoft Access must be installed, along with three out of four other products \(Microsoft Word, Microsoft Excel, Microsoft PowerPoint, and Microsoft Outlook\), to infer that Microsoft Office Professional is installed on a device.

## Subscription suite inference for Microsoft 365

This section provides details about the inference mechanism used for Microsoft 365, a subscription product.

Microsoft 365 is a subscription, comprising of several distinct products and services such as Office 365, Windows, and Enterprise Mobility and Security \(or EMS\). Office 365 and EMS include many other products and services within it.

There are several subscription plans, and the availability of certain products or services depends on the plan. For example, Power BI is only available with the Office 365 E5 subscription plan, not the E3 plan. Additionally, the Microsoft 365 admin center is where Microsoft 365 administrators can manage Microsoft 365, purchase additional subscriptions, and check usage.

ServiceNow Software Asset Management Professional integrates with Microsoft 365 admin center to help support Software Asset Management managers on many use cases such as license compliance determination and optimization recommendation.

Let's take an example to understand how subscription inference works. If you have a subscription for a component of Microsoft 365, such as EMS or Office 365, it will be inferred in the software model for Microsoft 365. This is because you purchased the Microsoft 365 entitlement and will be using the subscription for its associated components.

## Use cases for Microsoft 365

The following are some common use cases that help in understanding how license compliance helps in different scenarios.

-   Use case 1: An organization has purchased both Microsoft 365 E3 and Office 365 E3 licenses and has corresponding entitlements in ServiceNow Software Asset Management Professional to license these subscriptions.

    This is a valid use case, as there are specific and exact entitlements purchased for each subscription on the Microsoft 365 admin center. As a result, the subscriptions are licensed correctly in ServiceNow Software Asset Management Professional.

-   Use case 2: An organization has purchased individual Microsoft 365 component subscriptions including Office 365 E3, EMS E3, and Windows 10 on Microsoft 365 admin center. The organization wants to license these subscriptions using the Microsoft 365 E3 entitlement in ServiceNow Software Asset Management Professional.

    This is a valid use case, as the organization purchased individual component licenses for Office 365 E3, EMS E3 and the system automatically licenses or infers them to Microsoft 365 E3 license purchased. This is because the organization had previously purchased individual component subscriptions and has now transitioned to Microsoft 365 to gain more benefits.

-   Use case 3: An organization has purchased a Microsoft 365 E3 subscription through the Microsoft 365 admin center and wants to license them using the Microsoft 365 E5 entitlement in ServiceNow Software Asset Management Professional.

    This is an invalid use case, as the subscriptions should be listed at the same level as the entitlement. It appears there’s a misconfiguration in the Microsoft 365 admin center, which must be corrected.


**Parent Topic:**[Software Asset Management software suites](software-suites.md)

