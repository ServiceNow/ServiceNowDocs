---
title: Create remote choice definitions in Service Exchange for Providers
description: As a provider, define remote choice fields that allow consumers to retrieve choice data from their instances in real time.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Create remote choice definitions in Service Exchange for Providers

As a provider, define remote choice fields that allow consumers to retrieve choice data from their instances in real time.

## Before you begin

-   Role required for creating a Remote Choice Definition: security\_admin
-   Role required for creating Remote Choice fields: admin

## Procedure

1.  Elevate your role to security\_admin.

2.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Remote Choice Definitions**.

3.  Click **New**.

4.  On the form, fill in the fields.

<table id="table_r2f_zkw_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table that's available to your consumers to query for while they are selecting a catalog item on their service portal.

</td></tr><tr><td>

Name

</td><td>

Auto-assigned name that can be changed by an user with the `security_admin` role.

</td></tr><tr><td>

GlideRecordSecure

</td><td>

When this option is selected, all queries for this table follow the access control list \(ACL\) restrictions. When this option isn’t selected:-   Queries for this table ignore all ACL restrictions.
-   Reference qualifier conditions must be specified for each remote choice variable to limit data access.


</td></tr><tr><td>

AccountSecure

</td><td>

When this option is selected, all queries for this table limit the results that are based on the querying service account's **Company** field and the table's **Company** or **Account** field. **Note:** This flag is available only on the tables with references to the company or account where the field is named account, u\_account, company, or u\_company.

</td></tr><tr><td>

Short description

</td><td>

Additional information about the table.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions that define the base conditions on the table.

</td></tr></tbody>
</table>5.  Click **Save**.

6.  Navigate to **Service Exchange Providers** &gt; **Administration** &gt; **Remote Catalog Items**.

7.  Select a remote record producer and click **Edit**.

8.  In the Variables related list, click **New**.

9.  On the form, fill in the fields.

<table id="table_b2w_2dk_dvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record producer table

</td><td>

Auto-selected table that appears when you select the field. This table can be selected manually if it isn't mapped to a field.

</td></tr><tr><td>

Type

</td><td>

Reference type.

</td></tr><tr><td>

Remote choice enabled

</td><td>

Option that you can select for a remote choice.

</td></tr><tr><td>

Catalog item

</td><td>

Name of the remote record producer.

</td></tr><tr><td>

Question

</td><td>

Questions that appear in a catalog record on your consumer's service portal.

</td></tr><tr><td>

Type Specifications

</td><td>

-   **Remote choice reference** that includes the remote choice definition that you use for consumer queries for this variable.
-   **Remote choice display** field that includes the primary data value that appears to your consumers in their querying results.
-   **Remote choice additional info** field that includes the secondary data value that appears to your consumers in their querying results.
-   **Reference qualifier condition** that includes the filter options that you define to limit the data that is returned by the definition.


</td></tr></tbody>
</table>10. Click **Submit**.


## Result

A remote choice variable is created.

