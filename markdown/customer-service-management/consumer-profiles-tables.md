---
title: Tables used by consumer profiles
description: Customer Service Management \(CSM\) introduced consumer profile \(sn\_csm\_consumer\_profile\) column on Case, Sold Product, Install Base Item, and Interaction tables to identify and differentiate profile-specific data to be used by industries for different use-cases.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating multiple consumer profiles for a user, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Tables used by consumer profiles

Customer Service Management \(CSM\) introduced consumer profile \(sn\_csm\_consumer\_profile\) column on Case, Sold Product, Install Base Item, and Interaction tables to identify and differentiate profile-specific data to be used by industries for different use-cases.

<table id="table_zl3_thz_cwb"><thead><tr><th>

Plugin

</th><th>

Tables

</th><th>

Column added

</th></tr></thead><tbody><tr><td rowspan="5">

Customer Service Base Entities \[com.snc.cs\_base\]

</td><td>

Case \[sn\_customerservice\_case\]

</td><td>

Consumer Profile\[consumer\_profile\]

</td></tr><tr><td>

Sold Product\[sn\_install\_base\_sold\_product\]​

</td><td>

Consumer Profile\[consumer\_profile\]

</td></tr><tr><td>

Install Base Item\[sn\_install\_base\_item\]

</td><td>

Consumer Profile\[consumer\_profile\]

</td></tr><tr><td>

Interaction\[interaction\]

</td><td>

Consumer Profile\[consumer\_profile\]

</td></tr><tr><td>

Task\[sn\_customerservice\_task\]

</td><td>

Consumer Profile\[consumer\_profile\]

</td></tr></tbody>
</table>**Note:** Consumer Profile \(sn\_csm\_consumer\_profile\) table is an extension-only table to be used for supporting multiple profiles for consumer both within and across different industries.

