---
title: Apply ACL script conditions to reference fields
description: Use the glide.sys\_reference\_row\_check system property to enable scripted conditions for reference fields.
locale: en-US
release: yokohama
product: Access Control
classification: access-control
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Advanced ACL configuration, Access Control List Rules, Access Management]
---

# Apply ACL script conditions to reference fields

Use the **glide.sys\_reference\_row\_check** system property to enable scripted conditions for reference fields.

The default behavior is intended to improve instance performance. If you want to enable script conditions for reference fields, add the following system property.

**Note:** For more information on creating system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

<table id="table_vf1_5ff_2r"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.sys\_reference\_row\_check

</td><td>

Controls whether the script conditions of Access Control Rules apply to a table's reference fields.-   Type: true \| false
-   Default value: **false**
-   Location: [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>**Note:** If the **glide.sys\_reference\_row\_check** system property is not present, or has been set to false, script conditions for Access Control Rules are not applied. This means an ACL containing scripted conditions will pass it's check as long as the other ACL criteria are met \(such as role requirements\).

