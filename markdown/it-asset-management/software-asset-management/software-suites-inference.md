---
title: Software suites inference
description: Suite inference identifies whether an installed or subscribed software product is part of a suite and applies the most efficient suite license during reconciliation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/software-suites-inference.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Software Asset Management software suites, Exploring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Software suites inference

Suite inference identifies whether an installed or subscribed software product is part of a suite and applies the most efficient suite license during reconciliation.

\[Omitted video\] Description: This video explains the software suite inference feature and how the Software Asset Management application works with this feature.

## Suite inference flow

The process of suite inference runs in two stages:

1.  Building the suite structure: The suite engine builds the suite structure based on entitlements, software models, and suite relationships.
2.  Inferring the optimal suite: The suite engine processes install and subscription records to identify the most optimal suite parent for each record.

After the suite engine runs, the **Inferred suite** column is updated for all install and subscription records that are part of a suite. The column displays a reference to the software model of the most optimal suite parent, and the corresponding entitlements are applied to each stamped record. For more information about how the suite engine selects the optimal suite, see the [Suite inference rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-suites-inference.md).

**Note:** Users with the model\_manager role can navigate to **Product Catalog** &gt; **Product Model** &gt; **Software Models**, but can’t administer all aspects of software models.

## Automated suite inference logic

The Software Asset Management application calculates the inference percentage in automated mode based on your software install footprint and current entitlements. For example, you have only Windows Server installations, no System Centre installations, and hold entitlements only for Core Infrastructure Server \(CIS\). The inference percentage will be set to 0%. This value is calculated during reconciliation so you don't have to manually configure it.

With the automated suite inference logic, there's no longer a need to create product install conditions for common applications such as Visual Studio. The automated suite inference logic makes sure that the inference is done correctly.

Consider an environment with three clusters, each containing two physical hosts with 16 cores per host. Because virtual machines can migrate between hosts in a cluster, all 32 cores in each cluster are included in the licensing requirement.

|Cluster|Installed software|Core requirement|
|-------|------------------|----------------|
|Cluster A|Windows Server only|32 cores|
|Cluster B|Windows Server and System Center|32 cores|
|Cluster C|Windows Server and System Center|32 cores|

|Entitlements|Available rights|Coverage|
|------------|----------------|--------|
|CIS|32 core rights|Windows Server and System Center|
|Windows Server|64 core rights|Windows Server|
|System Center|32 core rights|System Center|

Only enough CIS rights are available to cover one 32-core cluster. During reconciliation, the Software Asset Management application evaluates the installed software and available license rights for each cluster and applies licenses as follows:

-   **Cluster A**

    Only Windows Server is installed. Applying a CIS entitlement would include unused System Center rights. The Software Asset Management application consumes 32 Windows Server core rights.

-   **Cluster B or C**

    Both Windows Server and System Center are installed. CIS covers both products with the same 32 core rights. The Software Asset Management application consumes the 32 available CIS core rights.

-   **Remaining cluster**

    Both products are installed, but CIS rights are already consumed. The Software Asset Management application applies individual entitlements, consuming 32 Windows Server and 32 System Center core rights.


|Cluster|License|
|-------|-------|
|Cluster A|32 Windows Server core rights|
|Cluster B or C|32 CIS core rights|
|Remaining cluster|32 Windows Server + 32 System Center core rights|

The Software Asset Management application automatically determines when a suite license provides the most efficient coverage and when component licenses must be used. No manual inference threshold or product install condition is required.

If you prefer to calculate the inference percentage manually and revert to the default 75%, you must override the automated option. To override, clear the **Automatic determination of inference** option after navigating to **Product Catalog** &gt; **Product Model** &gt; **Software Models** &gt; **Suite Components**.

## Inference options

**Note:** If the system property **com.snc.sam.auto\_suite\_inference** is set to true, the Inference number and percent is automatically determined and the **Inference option** isn't visible. Additionally, the parent software model suite is automatically inferred for a software model based on its child software models.

Use the **Mandatory** and **Inference option** fields when the suite parent isn’t defined in the install table.

The following table describes the available values for the **Inference option** and **Mandatory** fields.

<table id="table_jv1_nwz_yjc"><thead><tr><th>

Field

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mandatory

</td><td>

-   Optional
-   Always Mandatory
-   Mandatory Group

</td><td>

Enforces whether a component must be installed to infer that the suite is installed.

</td></tr><tr><td>

Inference option

</td><td>

-   Number
-   Percent

</td><td>

The **Inference Number** specifies the number of components installed for the suite. The number can be any non-negative number.

**Note:** For any new software models being created with suite components, the **Number** option is selected by default.

 The **Inference Percent** specifies what percentage of the components must be installed for the suite.

**Note:** For existing software models with suite components that were using the inference percent, the **Percent** option is selected by default. If preferred, you can switch to the **Number** option.

</td></tr></tbody>
</table>## Suite inference rules

The suite engine applies the following rules to select the most optimal suite for a software installation:

1.  If one of the software installations belongs to the suite software model, the suite is inferred directly without the need to meet the Inference percentage or Inference number.
2.  If rule 1 isn’t met, then any suite that meets the Inference percentage or Inference number on that device can be considered an Inferred suite candidate.
3.  The candidate with the highest number of installed components is selected.
4.  If there’s a tie, the suite with the lower downgrade is selected. For example, if Office 2016 and Office 2013 are both candidates with the same number of installed components, Office 2013 is selected because it's the downgrade of Office 2016.
5.  If there’s still a tie, the one with the highest percentage of installed components is selected.

## Suite inference rules for Microsoft license metrics

Based on the system property **com.snc.sam.auto\_suite\_inference**, the Software Asset Management application uses suite or component licenses. For example, if you have both CIS suites and Windows Server installations, both have their individual licenses. If Windows Server installations are discovered, then the Software Asset Management application first licenses using the available Windows Server licenses. CIS licenses are used only after all the Windows Server licenses have been used.

When the system property **com.snc.sam.auto\_suite\_inference** is set to true, the rules ranking for Microsoft license metrics are as follows:

1.  If there are multiple suites that can be inferred for the component, then the suite which meets the inference number or percent is preferred.
2.  The suite candidate with the highest number of installed components is preferred.
3.  If there’s a tie, the suite with the lower downgrade rights is chosen. For example, CIS 2019 and CIS 2016 are both candidates and have the same number of installed components. However, since CIS 2016 is the downgrade of CIS 2019 and it has fewer downgrade rights, CIS 2016 is chosen.
4.  The parent suite that meets the inference number or percent is preferred over the child suite. If the parent suite doesn't meet the inference percent, the child suite is preferred.
5.  If there’s still a tie, the one with the highest percentage of installed components is preferred.

## Examples for suite inference

The following examples show how inference options and rules work in practice in case of manual calculation.

1.  Inference percent with an always mandatory component

    You set the **Inference percent** to 75% and the **Mandatory** field to **Always Mandatory** for Microsoft Access. For Microsoft Office Professional to be inferred on a device, Microsoft Access must be installed along with at least three of the following four components: Microsoft Word, Microsoft Excel, Microsoft PowerPoint, and Microsoft Outlook.

2.  Inference number

    You set the **Inference number** to 2 for Microsoft Office. If Microsoft Word and Microsoft Excel are both installed on a device, the inference number condition is met. Also, the Microsoft Office suite license is applied instead of the individual component licenses.

3.  Inference percent with a threshold

    You set the **Inference percent** to 50% for CIS, which has two components: Windows Server and System Center. If more than 50% of the components are installed, the CIS suite license is applied. If fewer than 50% are installed, the individual component licenses are used.


**Parent Topic:**[Software Asset Management software suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-suites.md)

**Related topics**  


[Managing software suites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/Manage-software-suites.md)

