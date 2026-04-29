---
title: Manage certification policies
description: You can configure certification policies to keep your business applications inventory up to date. Keeping your business application data current helps you to assess your business applications precisely as there are indicators that are dependent on these business applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring the Setup page in the Enterprise Architecture Workspace, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage certification policies

You can configure certification policies to keep your business applications inventory up to date. Keeping your business application data current helps you to assess your business applications precisely as there are indicators that are dependent on these business applications.

If you have directly installed version 4.0.0 of the EA Workspace store application, the certifications data is saved to and fetched from the CMDB Data Management Task \(cmdb\_data\_management\_task\) table.

If you upgraded your EA Workspace from a previous version to version 4.0.0, you may see that your certification data is still fetched from the Certification Schedules \(cert\_schedule\) table, In this case, you must migrate your certification policies to the CMDB Data Management Certification Policies \(sn\_cmdb\_ws\_dm\_certification\_policy\) table.

## Convert certification schedules to certification policies

To convert the existing certification schedules to certification policies, you must import the certification schedules into Data Manager. This process converts the certification schedules into draft certification policies and you can then publish these policies to activate them. For more information, see [Import certification schedules in to Data Manager](../../task/eaw-task/eaw-convert-cert-schedules-to-cert-policies.md) and [Publish a draft Data Manager policy](../../task/eaw-task/eaw-publish-a-draft-policy.md).

**Parent Topic:**[Exploring the Setup page in the Enterprise Architecture Workspace](eaw-setup.md)

**Related topics**  


[Import certification schedules in to Data Manager](../../task/eaw-task/eaw-convert-cert-schedules-to-cert-policies.md)

[Publish a draft Data Manager policy](../../task/eaw-task/eaw-publish-a-draft-policy.md)

[View all certification policies](../../task/eaw-task/eaw-view-all-cert-schedules.md)

[Add or edit a certification policy](../../task/eaw-task/eaw-manage-cert-schedules.md)

