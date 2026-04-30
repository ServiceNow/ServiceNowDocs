---
title: Disable recommendation prompts
description: Disable the prompts recommending the use of DevOps Change Workspace from appearing while creating tools and applications using Classic UI, Service Catalog, Service Portal, and Employee Service Center.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Disable recommendation prompts

Disable the prompts recommending the use of DevOps Change Workspace from appearing while creating tools and applications using Classic UI, Service Catalog, Service Portal, and Employee Service Center.

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.
2.  For each of the following 4 DevOps catalog items, you must edit the catalog client scripts to comment out the call to `showWorkspaceAdvertisement`.
    -   Create DevOps Application
    -   Create DevOps tool
    -   DevOps App Onboarding
    -   DevOps Tool Onboarding
3.  Select each DevOps catalog item listed earlier and navigate to the **Catalog Client Scripts** tab under **Related Links**.
4.  Select each script available under **Catalog Client Scripts**.
5.  Search for the method `showWorkspaceAdvertisement`.
6.  If present, comment it out.

    For example, `//showWorkspaceAdvertisement();`.

7.  Save the changes.

**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

