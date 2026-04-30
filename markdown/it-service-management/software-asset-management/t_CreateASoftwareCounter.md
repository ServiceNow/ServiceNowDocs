---
title: Create a software counter for the legacy Software Asset Management plugin
description: How to create a software counter for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Create a software counter for the legacy Software Asset Management plugin

How to create a software counter for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## About this task

Depending on the [license type](../reference/r_LicenseCalculationTypes.md) you select for a counter, multiple installations can count as a single license, such as when using the per user license type. This licensing concept is used on occasion by companies like Microsoft and Adobe. It grants users the right to install software on multiple machines if those users already have rights to install the software.

**Note:** You can [create new counters](t_CreatingNewModels.md) from Discovery model records or from the list view.

To manage multiple versions of software from a single licensing perspective for the parent software model:

-   The downgrade child software models that are licensed under the parent software model should all be related to a the single parent software model.
-   The downgrade child software models should not have any software counters associated with them.
-   The software counter should be associated only with the licensed parent software model, otherwise misleading results for the counter will be reported

To create a software counter:

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Software Counters**.

2.  Click **New**.

3.  Fill in the fields on the Software Counter form \(see table\).

4.  Click **Submit**.

5.  Reopen the new counter and click **Count Licenses**.

6.  Reload the form to view the [counter results](t_ViewASoftwareCounterResult.md).

<table id="table_tsm_jmc_zq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Required\] Enter the name of the software counter as it appears in record lists.

</td></tr><tr><td>

Software model

</td><td>

\[Required\] Click the reference lookup icon and select the software model for which the counter will check compliance.

</td></tr><tr><td>

Contract

</td><td>

Select the contract that you want to use to limit the license. Used for enterprise and subscription-based licenses. Also restricts how counters retrieve licenses for the given counter. If left empty, all licenses for the model are counted.

</td></tr><tr><td>

Active

</td><td>

Select the check box to have the scheduler run the counter.

</td></tr><tr><td>

Rights Owned

</td><td>

\[Read-Only\] Displays a summation if a contract is specified. The total sum is the license rights provided by all the licenses for the software model \(of the counter\) under the specified contract. If no contract is specified, this field is a count of all licenses of this model.

</td></tr><tr><td>

Rights Used

</td><td>

\[Read-Only\] Displays the number of rights used by all installs, whether a contract is specified or not.

</td></tr><tr><td>

Immediate compliance

</td><td>

\[Read-Only\] Displays the number of additional rights needed to achieve compliance based on installations.

</td></tr><tr><td class="sub-head" colspan="2">

Parameters

</td></tr><tr><td>

Grouping

</td><td>

Select the field for grouping data:

-   Location: group by the geographic location set in the license record.
-   Company: group by the company set in the license record.
-   Department: group by the department set in the license record.
-   Cost Center: group by the cost center set in the license record.
-   Entitlement \(CPU\): group by the condition defined in the Allocated condition field of the license record.
-   Entitlement \(User\): group by the condition defined in the Assigned condition field of the license record.
 The software counter results also displays counts for licenses that do not match the grouping parameter.

</td></tr><tr><td>

Enforce to

</td><td>

\[Required\] Select the level of adherence to the license:-   License: counts all existing entitlements for the installations or usage you are analyzing regardless of the grouping parameter selected.
-   Strict: counts the license and entitlement as valid only if the license also matches the grouping category. For example, a license is assigned to a specific location, such as Americas. With strict enforcement enabled, the user and the machine on which the license is installed must be in the Americas group. If the person and their license assigned to the Americas group moves to the United Kingdom, the license is still valid, but strict enforcement flags the user as unauthorized to use that license. The license will be counted as valid, but will also show up as not entitled in the summary.


</td></tr><tr><td>

Verify entitlements

</td><td>

Select the check box to view the software entitlement details for the software counter. Results include the number of installations of all types: not entitled, entitled in use, entitled not in use, and not allocated. For more information, see [Setting Up Quick Counters](../concept/c_SetUpQuickCounters.md).

</td></tr><tr><td>

Generate details

</td><td>

Select the check box to generate the details of the entitlement records. For more information, see [Setting Up Quick Counters](../concept/c_SetUpQuickCounters.md).

</td></tr><tr><td>

License type

</td><td>

\[Required\] Select the method for counting licenses. For example, Per named user or Per workstation.

 For more information, see [License Calculation Types](../reference/r_LicenseCalculationTypes.md).

</td></tr><tr><td>

Installs per license

</td><td>

Enter the number of installations allowed \(one or more\) per license for each user if the License type is set to By number of users. You can allow more than two installations per license.

 For all other license types this field is set to 1 install per license.

</td></tr><tr><td>

Cached

</td><td>

\[Read-Only\] Shows whether this option is selected. If selected, only changed information is counted, reducing the amount of time it takes to count the licenses.

</td></tr><tr><td>

License condition

</td><td>

Specify the condition a license should satisfy in order to be counted.

</td></tr><tr><td>

Software install condition

</td><td>

Specify the condition an install record should satisfy in order to be counted. This field appears depending on the value of the License type field.

</td></tr><tr><td>

Software usage condition

</td><td>

Specify the condition a usage record should satisfy in order to be counted. This field appears depending on the value of the License type field.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Software Counter Results

</td><td>

Displays all [results](t_ViewASoftwareCounterResult.md) for this software counter.

</td></tr><tr><td>

Software Counter Compliance Violations

</td><td>

Displays all records of compliance violations for this software counter.

</td></tr><tr><td>

Software Counter Histories

</td><td>

Displays all software counter history records for this software counter. Each time a count is completed, the system automatically generates a software counter history record, which is a read-only copy of the software counter record.

</td></tr></tbody>
</table>    **Note:** A message is displayed at top of the software counter form indicating if a license count is in progress. Reload the form to view the counter results.


**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

