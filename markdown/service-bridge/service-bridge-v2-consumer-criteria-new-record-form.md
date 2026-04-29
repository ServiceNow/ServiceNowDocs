---
title: Consumer criteria new record form
description: Field descriptions for the consumer criteria new record form contains information on consumer criteria new record form field values.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Service Exchange]
---

# Consumer criteria new record form

Field descriptions for the consumer criteria new record form contains information on consumer criteria new record form field values.

<table id="table_u2k_mpp_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the consumer condition.

</td></tr><tr><td>

Active

</td><td>

Select this check box to enable the consumer condition.

</td></tr><tr><td>

Condition for

</td><td>

Allows you to specify the Company or Account can be used to match the records on the table being queried. Select the corresponding option based on which field \(Company or Account\) is available on the table being queried. For example, this field can be used on the Sold Product table as the Account field is used to query the table.

</td></tr><tr><td>

Condition on

</td><td>

Field indicates which table is to be queried to find matching records.**Note:** Tables where Customer Field cannot be selected should not be used.

</td></tr><tr><td>

Customer field

</td><td>

Select the field on the table being queried that matches the Company or Account defined on the Service Exchange connection. If the consumer connected through Service Exchange is an Account, you can use either a Company or Account field to match against it. If the consumer connected is only a Company, you will be restricted to Company.

</td></tr><tr><td>

Condition

</td><td>

Details of the filter. For example, Active is True.

</td></tr></tbody>
</table>## Useful references

[Create a consumer criteria](../concept/service-bridge-v2-create-consumer-criteria.md).

