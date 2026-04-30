---
title: Update set transfers
description: When an update set is completed, you can transfer it between instances to move customizations from development, through testing, and into production.
locale: en-US
release: yokohama
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Update set transfers

When an update set is completed, you can transfer it between instances to move customizations from development, through testing, and into production.

**Warning:** Update sets allow moving changes between instances that may be running different family release versions and different features. You can always load an update set created on an older family release on an instance running a newer family release. Loading an update set created on a newer family release on an instance running an older family release requires additional testing to determine compatibility. Updates from newer family releases may not produce the same functionality when moved to older family releases. In extreme cases, newer family release updates may cause outages or data loss on an older family release instance. Where possible, avoid moving updates from newer family releases to older family releases. Similar constraints apply to moving updates between instances running different versions of ServiceNow Store apps.

## Transferring with IP access control

If IP address access control is enabled on the source instance or the source instance resides in a different datacenter than the target instance, complete these tasks before transferring an update set:

1.  Contact Customer Service and Support to find out the IP addresses of all application nodes supporting your instance.
2.  On the source instance, navigate to System SecurityIP Address Access Control.Add the IP address from step one as an exception.

## Transferring with basic authentication

If the source instance has basic authentication turned on for SOAP requests, you must use valid credentials to retrieve update sets.

## Transferring with an XML file

You can unload an update set as an XML file and then transfer it to another instance. See [Save an update set as a local XML file](../task/t_SaveAnUpdateSetAsAnXMLFile.md#) for details.

