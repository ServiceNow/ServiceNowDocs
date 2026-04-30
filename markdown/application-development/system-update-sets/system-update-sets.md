---
title: System update sets
description: An update set is a group of configuration changes that can be moved from one instance to another. This feature allows administrators to group a series of changes into a named set and then move them as a unit to other systems for testing or deployment.
locale: en-US
release: yokohama
product: System Update Sets
classification: system-update-sets
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Deploying applications, Building applications]
---

# System update sets

An update set is a group of configuration changes that can be moved from one instance to another. This feature allows administrators to group a series of changes into a named set and then move them as a unit to other systems for testing or deployment.

**Note:** When an update set is backed out, there is an OOB business rule that will delete sys\_upgrade\_state record on customer update deletion. This is an expected behavior.

An update set is an XML file that contains:

-   A set of record details that uniquely identify the update set.
-   A list of configuration changes.
-   A state that determines whether another instance can retrieve and apply configuration changes.

Update sets track changes to applications and system platform features. This allows developers to create new functionality on a non-production instance and promote the changes to another instance.

**Warning:** Update sets allow moving changes between instances that may be running different family release versions and different features. You can always load an update set created on an older family release on an instance running a newer family release. Loading an update set created on a newer family release on an instance running an older family release requires additional testing to determine compatibility. Updates from newer family releases may not produce the same functionality when moved to older family releases. In extreme cases, newer family release updates may cause outages or data loss on an older family release instance. Where possible, avoid moving updates from newer family releases to older family releases. Similar constraints apply to moving updates between instances running different versions of ServiceNow Store apps.

## System properties

Administrators can exclude system properties from update sets by making them private. Keeping system properties private prevents settings in one instance from overwriting values in another instance. For example, you may not want a system property in a production instance to use a particular value from a development instance. See [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## Applications

Application developers have additional options with update sets such as:

-   Create an update set for a specific version of an application.
-   Specify which application tables to track in update sets.

## Update set tables

Each update set is stored in the Update Set `[sys_update_set]` table, and the customizations that are associated with the update set, which are entries in the Customer Update `[sys_update_xml]` table, appear as a related list on the update set record.

When a tracked object is customized, a corresponding record is added or updated in the Customer Update `[sys_update_xml]` table and is associated with the user current update set. The [associated application file properties](../../applications/concept/c_ApplicationFiles.md) are tracked and transferred along with the customized object in a single update record. A corresponding record is also added to the Versions `[sys_update_version]` table.

The Customer Update table contains one record per customized object, per update set. The Versions table contains one record per change to a customized object.

-   Administrators can compare two versions and revert to a specific version of an object.
-   Administrators can suppress versions for specific tables.
-   Administrators can specify fields on tracked tables that you can change without skipping updates to the rest of the record \(exclude the field from the update\).

**Note:** Do not directly modify Customer Updates `[sys_update_xml]` records.

