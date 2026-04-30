---
title: Create a COE security policy
description: Use COE Security Configuration to define group restrictions for a COE and for all or specific HR services under it.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create a COE security policy

Use **COE Security Configuration** to define group restrictions for a COE and for all or specific HR services under it.

## Before you begin

Role required: sn\_hr\_core.admin

Certain users will be able to access a COE even it is restricted. For example, Opened for, Opened by, Watch List and Collaborators get access to a restricted COE irrespective of its security policies.

COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are [ServiceNow ACLs](https://www.servicenow.com/docs/access?context=access-control-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Note:** When COE Security Policies restrict an agent's access to a limited number of cases, list pages with broad filters such as All Cases, Open Cases may yield many pages with empty results with a message indicating that rows are hidden due to security constraints. As a result, agents may struggle to locate the cases they have access to, as these cases might be scattered across multiple pages. This behavior is expected, as COE Security Policies are essentially Access Control Lists \(ACLs\) that filter data accordingly. To overcome this issue, agents can create custom lists with more targeted filters, such as My Group Cases, to easily find the cases they are authorized to access.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **COE Security Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_sph_pjf_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Name that you want to give to the security policy that is created for the Center of Excellence \(COE\).

</td></tr><tr><td>

COE

</td><td>

Center of Excellence \(COE\) that you want to create a security policy for.**Note:** The COEs that appear depend on the Application selected.

</td></tr><tr><td>

Applies to all services

</td><td>

Option to apply all HR services for the COE security policy.

</td></tr><tr><td>

Applies to all child COEs

</td><td>

Option to apply the security policy on child COEs of the parent COE.

</td></tr><tr><td>

Short description

</td><td>

More information about the security policy that is created for the Center of Excellence \(COE\).

</td></tr><tr><td>

Services

</td><td>

HR service that the COE security policy applies to.This field appears only if the **Applies to all services** check box is not selected.

</td></tr><tr><td>

Application

</td><td>

Application that the COE security policy applies to.

</td></tr><tr><td>

Active

</td><td>

Option to indicate the active status of the COE security policy. Only active security policies are applied.

</td></tr><tr><td>

Type

</td><td>

Access that you want your HR agents to have for the cases that fall under the COE or HR services.Valid values:

 -   **Read**
-   **Write**


</td></tr><tr><td>

Applies when

</td><td>

Condition statement that filters an HR case.If the HR case matches the conditions, the COE security policy applies to it.

 You can create conditions based on key words or fields from the HR case.

 When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

**Note:** An empty filter condition matches all records for the selected COE.

</td></tr></tbody>
</table>4.  Click **Save** or **Submit**.

5.  Add the groups that you want the COE security policy to grant access to.

    **Note:** Leave this list blank to ensure no groups have access through the COE security policy.

6.  Click **Update**.


