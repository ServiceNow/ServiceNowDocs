---
title: List of Budget policy creation fields
description: Fields on the Budget policy creation form help you create a budget policy to specify a budgeted amount, cost type, reset period, and other aspects of the budget.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud Cost Management reference, Cloud Cost Management, IT Asset Management]
---

# List of Budget policy creation fields

Fields on the Budget policy creation form help you create a budget policy to specify a budgeted amount, cost type, reset period, and other aspects of the budget.

<table id="table_xfh_rcv_ywb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Budget policy

</td><td>

List of created budget policies.If you want to update a budget policy, search and select a created budget policy from the drop-down list. After you select a budget, all the relevant fields get automatically populated.

</td></tr><tr><td>

Active

</td><td>

Option to apply the policy, which executes Budget Forecast analysis whenever billing data is updated.

</td></tr><tr><td>

Name

</td><td>

A unique name that describes the policy for other users.

</td></tr><tr><td>

Description

</td><td>

A unique description that describes the policy for other users.

</td></tr><tr><td>

Cost type

</td><td>

Contractual payment agreement with the provider.-   Amortized: Your organization pays the effective cost of the upfront and monthly reservation fees spread across the billing period. The amortized cost type is described in detail on the provider site.
-   Actual: Each billing period, your organization pays for direct cloud services.

</td></tr><tr><td>

Start month

</td><td>

Month from which the plan applies.

</td></tr><tr><td>

End month

</td><td>

Month until when the plan applies.

</td></tr><tr><td>

Start day

</td><td>

Date from which the plan applies.

</td></tr><tr><td>

End day

</td><td>

Date until when the plan applies.

</td></tr><tr><td>

Start year

</td><td>

Year from which the plan applies.

</td></tr><tr><td>

End year

</td><td>

Year until when the plan applies.

</td></tr><tr><td>

Currency

</td><td>

Currency type of the policy.

</td></tr><tr><td>

Amount

</td><td>

Total spend that is budgeted for the time period that is specified by the Granularity value.**Calculated**

Behaves in the same way as the default currency field type. Whenever conversions are performed, the system uses the latest currency conversion rates. The amount appears in the session currency for the user.

**Fixed**The amount displays in the currency code that you used when you entered the Amount value. Conversions use the latest currency conversion rates.

**Multiple**Enables you to enter multiple amounts using a different currency for each amount. The field value is the value entered in the user’s session currency. Otherwise, the first value entered converts to the user’s session currency. Conversions use the latest currency rates.

**Note:** The first amount entered is used during display. The other values aren’t used to perform calculations.

The session currency for the instance determines the numbers that a user sees on budget reports. If the currency you specify in the Budget plan differs from the session currency, then the amount displays in the reports in two fields:

-   **Budgeted amount**: The money amount expressed in the currency used in the plan.
-   **Converted budget amount**: The same money amount, expressed in the session currency.

</td></tr><tr><td>

Granularity

</td><td>

Reset period for the budget.-   **Annual**: The Amount value applies to a one-year period.
-   **Monthly**: The Amount value applies to a one-month period.

</td></tr><tr><td class="sub-head" colspan="2">

Account and Resource criteria

</td></tr><tr><td>

Parent account

</td><td>

The primary account with which the service accounts are associated.**Note:** While editing a policy, changing the parent account can change the provider.

</td></tr><tr><td>

Service accounts

</td><td>

The service accounts to apply the plan to. Move all appropriate service accounts to the **Selected** list.For Google Cloud only, this field is called Projects.

</td></tr><tr class="sub-head"><td>

Tag category condition

</td><td>

Add tag category by selecting a tag category from the drop-down list and by adding tag values separated by comma.

</td></tr><tr><td class="sub-head" colspan="2">

Budget Viewer and Notifications

</td></tr><tr><td>

Viewer \(user\)

</td><td>

User that can view this Budget policy.**Note:** Regardless of this selection, only users that also have the Cloud Budget Viewer \[sn\_clin\_core.budget\_viewer\] role have viewing access.

</td></tr><tr><td>

Viewer \(group\)

</td><td>

User group that can view this Budget policy.

</td></tr><tr><td>

Notification frequency

</td><td>

The recurrence of email to users as described in Users to notify.

</td></tr><tr><td>

User to be notified

</td><td>

Users to notify by email when the following conditions occur:-   Budget is forecast to be exceeded.
-   Budget is exceeded.
-   Budget is invalid.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

