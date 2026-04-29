---
title: Consumer Profile Location table
description: The Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table stores the relationship between the consumer profiles and locations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating multiple consumer profiles for a user, Configure consumers, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Consumer Profile Location table

The Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table stores the relationship between the consumer profiles and locations.

Starting with the Vancouver release, the Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table was introduced. By using this table, you can enhance your consumer profiles to support multiple addresses. Adding this functionality enables the relationship between the consumer profiles and locations, which enables various industries to manage multiple addresses for the individual profiles.

If you are a user with one of the sn\_crm\_foundation\_admin, sn\_crm\_foundation\_data\_manager, sn\_crm\_consumer\_relationship\_data\_manager, or sn\_crm\_consumer\_data\_manager roles, you can create, update, view, and delete the relationship between the consumer profiles and locations in the Consumer Profile Location table. If you are a user with one of the sn\_crm\_consumer\_viewer, sn\_crm\_household\_viewer, or sn\_crm\_foundation\_data\_viewer roles, you can view the records in the Consumer Profile Location table.

<table id="table_k51_hpt_zxb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Consumer profile

</td><td>

Reference

</td><td>

Profile that is associated with a consumer.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

Locations detail that is associated with the consumer.

</td></tr><tr><td>

Location type

</td><td>

List

</td><td>

Type of location that this record represents such as billing, shipping, and mailing.

 **Note:** You can associate a consumer profile location record with one or multiple location types.

</td></tr><tr><td>

Active

</td><td>

True/False

</td><td>

Status of the consumer profile-address mapping.

**Note:** By default, the active field is set to **True**, but you can disable the Consumer Profile Location linkage by setting it to **False**.

</td></tr></tbody>
</table>