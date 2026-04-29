---
title: Update set transfers
description: When an update set is completed, you can transfer it between instances to move customizations from development, through testing, and into production.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Update set transfers

When an update set is completed, you can transfer it between instances to move customizations from development, through testing, and into production.

## Transferring via ReleaseOps

ReleaseOps automates deployment of changes across your pipeline, increases predictability and reliability of deployments, and reduces the risk of releasing changes to production. See [ReleaseOps](../../release-ops/concept/releaseops-landing.md).

## Transferring via IP access control

If IP address access control is active on the source instance or a different datacenter from the target, complete these steps before transferring an update set.

1.  Contact Customer Service and Support to find out the IP addresses of all application nodes supporting your instance.
2.  On the source instance, navigate to System SecurityIP Address Access Control, and add the IP address as an exception.

## Transferring via an update source

If IP address access control is enabled on the source instance, set up the target instance as an exception. See [Set up the source instance for an update set](../task/setting-source-for-update-set.md).

## Transferring via an XML file

You can unload an update set as an XML file and then transfer it to another instance, see [Save an update set as a local XML file](../task/t_SaveAnUpdateSetAsAnXMLFile.md#).

**Parent Topic:**[Configuring System Update Sets](../concept/configure-system-update-sets.md)

