---
title: Consumer Profile Location table
description: The Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table stores the relationship between the consumer profiles and locations.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating multiple consumer profiles for a user, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Consumer Profile Location table

The Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table stores the relationship between the consumer profiles and locations.

Starting with the Vancouver release, the Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\] table was introduced. By using this table, you can enhance your consumer profiles to support multiple addresses. Adding this functionality enables the relationship between the consumer profiles and locations, which enables various industries to manage multiple addresses for the individual profiles.

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