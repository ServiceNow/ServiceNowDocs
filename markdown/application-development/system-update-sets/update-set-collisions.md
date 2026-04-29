---
title: Update set collision resolution
description: A collision is an update that has a newer local update.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Compare local update sets, Working with update sets, System update sets, Deploying applications, Building applications]
---

# Update set collision resolution

A collision is an update that has a newer local update.

The platform detects collisions by comparing the values in the Name and Updated fields of the customer update record from each update set. If the name matches but there are different update date values, then there’s a collision.

When a customer update is moved from one instance to another, it may be rewritten to match the target instance. The rewrite can involve changing the update name of the customer update and one or more sys\_id within the update. The rewrites are done when the record or the reference field is for a table that uses a coalesce strategy. This verifies that the customer update will be applied to the correct record. For example, if the sys\_dictionary record for tablename.fieldname has sys\_id `123` on instance A and sys\_id `456` on instance B, when a customer update that refers to that record is retrieved from instance A and recorded in the sys\_update\_xml table on instance B, references to `123` are updated to read `456`.

## Coalesce strategies

Coalescing refers to the process of identifying a record based on one or more fields that are used as unique identifiers during the update process. Update sets can detect collisions between identical records that you independently create on separate instances. To detect such collisions, the record must have a coalesce strategy based on coalescing columns. Because collision detection depends on the uniqueness of tables, the tables must be unique when the coalescing columns are combined. Records that aren’t listed here won’t collide if the same record is created separately on different instances.

|Type|Coalescing Columns|
|----|------------------|
|atf\_input\_variable|name, element|
|atf\_output\_variable|name, element|
|dp\_data\_pattern|source\_sys\_id|
|dynamic\_attribute|namespaced\_name|
|dynamic\_category|namespaced\_name|
|dynamic\_category\_member|category, attribute|
|dynamic\_choice\_override|choice, category, attribute|
|dynamic\_namespace|name|
|sys\_analytics\_bucket|sys\_scope, bucket\_document\_id, bucket\_table\_name|
|sys\_attachment|\(uses custom matching logic\)|
|sys\_choice\_set|name, element|
|sys\_collection|collection, name, join\_field|
|sys\_db\_object|name|
|sys\_df\_data\_dictionary|name, element|
|sys\_dictionary|name, element|
|sys\_documentation|name, element, language|
|sys\_index|logical\_table\_name, col\_name\_string|
|sys\_module|path|
|sys\_notification\_category|name|
|sys\_package|source|
|sys\_package\_dependency\_m2m|dependency, sys\_package|
|sys\_properties|name|
|sys\_report\_chart\_color|name, element, value|
|sys\_scope\_script\_access|source\_scope, target\_scope, script\_name|
|sys\_scope\_table\_access|source\_scope, target\_scope, table\_name|
|sys\_script\_validator|internal\_type, ui\_type|
|sys\_translated|name, element, value, language|
|sys\_translated\_text|tablename, fieldname, documentkey, language|
|sys\_ui\_form|name, view, sys\_domain|
|sys\_ui\_list|name, view, sys\_domain, element, relationship, parent|
|sys\_ui\_message|key, language, code|
|sys\_ui\_related\_list|name, view, related\_list, sys\_domain|
|sys\_ui\_section|name, view, caption, sys\_domain|
|sys\_ui\_view|name|
|sys\_user\_group|name|
|sys\_user\_role|name|
|sys\_wizard|name|
|ua\_table\_licensing\_config|name|

## How customer update record names affect collisions

To understand coalescing, it helps to understand how records that don’t coalesce work. For most record types, when a customer update is moved to a new instance, the system doesn’t detect collisions for the following reason:

-   When you create a record, it receives a unique sys\_id. For most record types, the sys\_id becomes part of the customer update record name. For example: `sysevent_email_template_9e1998c078b71100a92ecacd80df1d39`.
-   Creating an identical record in the same table on another instance produces a customer update record name with a different sys\_id. For example: `sysevent_email_template_10b958c8653311005840134572f8e020`

As a result, even though the records might be otherwise identical, the records have different names so the system doesn’t detect the collision.

Coalescing records, in contrast, use the following approach to naming records and determining collisions: The following customer update record types use some or all of their coalescing columns instead of the sys\_id in their names.

-   sys\_dictionary
-   sys\_documentation
-   sys\_choice\_set
-   sys\_ui\_list
-   sys\_ui\_related\_list

The resulting identical record name in each instance helps the system to identify collisions even if the records have different sys\_ids.

When a customer update is moved from one instance to another, it may be rewritten to match the target instance. The rewrite can involve changing the update name of the customer update and one or more sys\_ids within the update. The rewrites are done when the record or the reference field is for a table that uses a coalesce strategy. This confirms that the customer update will be applied to the correct record. For example, if the sys\_dictionary record for tablename.fieldname has sys\_id "123456789" on instance A and sys\_id "987654321" on instance B, when a customer update that refers to that record is retrieved from instance A and recorded in the sys\_update\_xml table on instance B, references to "123456789" are updated to read "987654321".

## Preventing duplicate records

-   Transfer data with update sets rather than recreating it on separate instances to verify the records have the same sys\_id.
-   Export and import records as XML files to verify the records have the same sys\_id. See [Export and import XML files](https://www.servicenow.com/docs/access?context=c_ExportAndImportXMLFiles&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Enable a unique index for the table from the system dictionary. See [Table administration](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** The default records included in the baseline system will always have the same sys\_id because the instance imports the records as XML files during instance provisioning.

**Parent Topic:**[Compare local update sets](../task/t_CompareLocalUpdateSets.md)

