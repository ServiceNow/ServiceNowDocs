---
title: Choice list security
description: You can use the personalize\_choices security role to enable non-administrators modify Choice elements options on all tables.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Choice list field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Choice list security

You can use the personalize\_choices security role to enable non-administrators modify Choice elements options on all tables.

If more granular control is desired, you can also create a custom ACL \(security rule\) governing the personalize\_choices operation either for a particular field or for all fields \(.\*\) on a particular table. However, access to the personalize\_choices operation on a particular field does not confer the ability to add new choices for that field.

To be able to create new choices for a particular field, an ACL that grants personalize\_choices access for that field is required. For example, to give the hris\_admin role the ability to personalize only the Category field for Human Resources KB articles, you need an ACL granting personalize\_choices access to the hris\_admin role on the Category field of the Knowledge \(kb\_knowledge\) table.

There are predefined ACLs granting both types of access to the personalize\_choices security role, for all fields on all tables. The personalize\_choices security role also has read, write, and delete access to the sys\_choices table. However, this additional access is not required when making just the Personalize Choices functionality available on a granular basis.

