---
title: List of Shared cost allocation policy fields
description: Fields on the Shared cost allocation policy creation form help you create a shared cost allocation policy.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Cloud Cost Management, IT Asset Management]
---

# List of Shared cost allocation policy fields

Fields on the Shared cost allocation policy creation form help you create a shared cost allocation policy.

<table id="table_wdg_wfw_fzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select shared cost policy to edit

</td><td>

The shared cost policy that you want to edit.

</td></tr><tr><td>

Active

</td><td>

The option to apply the policy. Selecting the **Active** check box enables shared cost allocation whenever billing data is updated.

</td></tr><tr><td>

Name

</td><td>

A unique name that describes the policy for other users.

</td></tr><tr><td>

Description

</td><td>

A brief description of the policy.

</td></tr><tr><td>

Run order

</td><td>

The order in which to apply policies. Each policy must have a unique value. The system applies policies in low-to-high run order and performs the actions for the first policy that matches. After a match, no other policy is applied to the resource.

</td></tr><tr><td>

Start month

</td><td>

The start month from when the monthly spend records are processed. This field is automatically set to the current month.**Note:** The Start month must be before the End month.

</td></tr><tr><td>

End month

</td><td>

The month till when the monthly spend records are processed.**Note:** The End month must be after the Start month.

</td></tr><tr><td>

Start year

</td><td>

The start year from when the monthly spend records are processed. This field is automatically set to the current year.**Note:** The Start year must be before the End year.

</td></tr><tr><td>

End year

</td><td>

The year till when the monthly spend records are processed. **Note:** The End year must be after the Start year.

</td></tr><tr><td>

Provider

</td><td>

The cloud provider to apply the policy to. **Note:** You can’t change the provider while editing an existing policy.

</td></tr><tr><td>

Service category

</td><td>

List of all service categories that the policy applies to.

</td></tr><tr><td>

Service accounts

</td><td>

The service accounts to apply the policy to.For Google Cloud only, this field is called Projects.

</td></tr><tr><td>

Cloud service

</td><td>

Cloud service that the policy applies to.-   All
-   Specific

</td></tr><tr><td>

Select cloud service

</td><td>

The cloud service that the policy you want to apply to.This field appears only when **Specific** is selected from **Cloud Service**.

</td></tr><tr><td>

Resource type

</td><td>

Resource type of the Kubernetes service category.-   Cloud resource
-   Kubernetes cluster

This field appears only when **Kubernetes Service** is selected from **Service category**.

</td></tr><tr><td>

Region

</td><td>

Region of the resource that the policy applies to.-   All
-   Specific

</td></tr><tr><td>

Select region

</td><td>

The region of the resource that the policy you want to apply to.This field appears only when **Specific** is selected from **Region**.

</td></tr><tr><td>

Purchase option

</td><td>

Purchasing options for your cloud resources.-   On demand
-   Reserved
-   Savings plans
-   Tax
-   Unknown

</td></tr><tr class="sub-head"><td>

Select the tag

</td><td>

 

</td></tr><tr><td>

Business unit

</td><td>

Business unit of the resource to which the policy applies to.-   All
-   Specific

</td></tr><tr><td>

Select business unit

</td><td>

The business unit of the resource that the policy you want to apply to.This field appears only when **Specific** is selected from **Business unit**.

</td></tr><tr><td>

Department

</td><td>

The department of the resource that the policy you want to apply to.-   All
-   Specific

</td></tr><tr><td>

Select department

</td><td>

The department of the resource that the policy you want to apply to.This field appears only when **Specific** is selected from **Department**.

</td></tr><tr><td>

Division

</td><td>

The department division of the resource that the policy you want to apply to.-   All
-   Specific

</td></tr><tr><td>

Select division

</td><td>

The department division of the resource that the policy you want to apply to.This field appears only when **Specific** is selected from **Division**.

</td></tr><tr><td>

Cost center

</td><td>

Cost center of the resource that the policy is applied to.-   All
-   Specific

</td></tr><tr><td>

Select cost center

</td><td>

The cost center of the resource that the policy you want to apply to.This field appears only when **Specific** is selected from **Cost center**.

</td></tr><tr><td>

Allocation type

</td><td>

Allocation type to be used while defining the shared cost allocation policy.-   **Fixed**: The allocation percentage is specified in the Cost distribution section for each group.  For example, if the cost of a cloud service is shared with two other groups, specify the allocation percentage for each group. 
-   **Even**: The allocation is split across the allocation groups evenly.  For example,if the cost of a cloud service is shared with two other groups, the allocation percentage is automatically populated evenly among these groups. 
-   **Proportional**: Policy for cloud services and service categories, or both, is defined.  The combination of these attributes is considered for shared cost allocation.  For example,​ if a policy is defined for the following combination, then all costs associated with this combination would be considered for shared cost. ​

    -   Service category: Database and Cloud service: Amazon DocumentDB 
    -   Service category: Database and Cloud service: Empty

Here, all Database category cloud services are considered as shared cost.​

The allocation percentage is automatically populated based on the direct cost of the resources.


**Note:**

-   The sum of allocation percentages across the groups must be 100%​.
-   The allocation percentage can’t be negative.
-   The combination of groups must be unique.​

</td></tr><tr class="sub-head"><td>

Cost distribution

</td><td>

Add Business unit, Division, Department, Cost center, and Allocation percentage to distribute the resource costs among various business lines by selecting **Add**.

</td></tr><tr class="sub-head"><td>

Namespace Distribution

</td><td>

For Kubernetes, add Namespace and Allocation percentage to distribute the resource costs among various business lines by selecting **Add**.This field appears only when **Kubernetes Service** is selected from **Service category** and **Kubernetes cluster** is selected from **Resource type**.

**Note:** The allocation type that you can define can be only Fixed and Even.

</td></tr><tr><td>

Allocation percentage

</td><td>

Percentage of the shared cost allocation for each cloud resource.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

