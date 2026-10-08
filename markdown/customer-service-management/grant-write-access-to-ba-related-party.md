---
title: Grant write access to a billing account related party
description: Create a responsibility access configuration to give a billing account related party more than read access, such as write or create access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/grant-write-access-to-ba-related-party.html
release: zurich
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 2
breadcrumb: [Creating a responsibility access configuration, Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Grant write access to a billing account related party

Create a responsibility access configuration to give a billing account related party more than read access, such as write or create access.

## Before you begin

Role required: admin

## About this task

The responsibility access configurations provided with the base system for billing accounts grant read access only. A responsibility access configuration record answers three questions, one on each tab of the form: which data is accessed and with what permissions, which relationship drives the access, and how the two tables are joined. All three tabs are required.

**Note:** Responsibility access configurations grant table-level access. Configure field-level access separately for the roles that you select.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.

2.  Select a responsibility definition record.

3.  From the Responsibility Access Configuration related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Responsibility|Responsibility that the related party holds. The base system provides Billing Authorized Account, Billing Authorized Contact, and Billing Authorized Consumer.|
    |Roles required|Role that the related party's user must hold, such as `sn_billing_account.authorized_contact` or `sn_billing_account.authorized_consumer`. You can select the edit icon to add roles.|
    |Active|Enables the configuration. It is selected by default.|

5.  Fill in the fields on each of the three tabs.

<table id="table_rac_tabs"><thead><tr><th>

Tab

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grant access to

</td><td>

Access levels

</td><td>

Levels of access for the accessible entities. Read is set by default. Add Write or Create to grant more than read access.

</td></tr><tr><td>

Grant access to

</td><td>

Accessible table

</td><td>

Table to grant access to, such as Billing Account, Billing Account Address, Billing Account Payment Profile, or Location.

</td></tr><tr><td>

Grant access to

</td><td>

Accessible table filter

</td><td>

Optional conditions that limit the records that the access applies to.

</td></tr><tr><td>

Through relationship

</td><td>

Relationship table

</td><td>

Table that holds the relationship driving the access. Select **Billing Account Related Party**.

</td></tr><tr><td>

Through relationship

</td><td>

Relationship filter

</td><td>

Optional conditions, for example to limit the access to related parties of a specific type.

</td></tr><tr><td>

Using relationship association

</td><td>

Type

</td><td>

How the accessible table and the relationship table are joined. The available values are: -   Simple: The accessible table and the relationship table have a direct connection.
-   Dependent: The accessible table and the relationship table are connected indirectly through another table.
-   Advanced: For all other scenarios.


</td></tr><tr><td>

Using relationship association

</td><td>

Relationship field

</td><td>

Field on the relationship table that identifies the record.

</td></tr><tr><td>

Using relationship association

</td><td>

Accessible table field

</td><td>

Matching field on the accessible table.

</td></tr></tbody>
</table>6.  Select **Submit**.


## Result

The related party's user gets this access only if a related party record exists on the billing account with the matching responsibility.

**Related topics**  


[Add related parties to a billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/add-related-parties-to-a-billing-account.md)

[List of related party configurations provided with the base system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/list-of-related-party-configurations.md)

