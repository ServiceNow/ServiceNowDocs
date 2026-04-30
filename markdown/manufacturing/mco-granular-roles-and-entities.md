---
title: Granular roles and entities
description: Module-level granular roles have been added to facilitate defining and configuring the responsibility framework. These roles enable tasks to be performed without creating custom access control lists \(ACLs\) on the target table when a responsibility ACL exists. This update aims to provide a more direct and declarative migration process.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-22"
reading_time_minutes: 1
breadcrumb: [Configure responsibility access, Set up your environment, Configure, Manufacturing Commercial Operations]
---

# Granular roles and entities

Module-level granular roles have been added to facilitate defining and configuring the responsibility framework. These roles enable tasks to be performed without creating custom access control lists \(ACLs\) on the target table when a responsibility ACL exists. This update aims to provide a more direct and declarative migration process.

|Granular roles|Description|
|--------------|-----------|
|Recall Claim Management Creator \[sn\_rcl\_claim\_mgmt.campaign.creator\]|View, write, and create Recall Campaign tables.|
|Recall Claim Management Viewer \[sn\_rcl\_claim\_mgmt.campaign.viewer\]|View all Recall Campaign tables.|
|Recall Claim Management Writer \[sn\_rcl\_claim\_mgmt.campaign.writer\]|View and write all Recall Campaign tables.|
|Campaign Phase Writer \[feature role\] \[sn\_rcl\_claim\_mgmt.campaign\_phase.writer\]|Read access on all Recall Campaign related tables. It has write access on Recall Campaign Phase, Impacted Finished Good &amp; Phase Task tables. It has create access on Phase Task and Impacted Finished.|
|Pre-authorization admin \[sn\_repair\_claim\_mgmt.repair\_pre\_auth\_admin\]|Create, update, and delete the pre-authorization request.|
|Repair Claim Management Viewer \[sn\_repair\_claim\_mgmt.repair\_pre\_auth\_viewer\]|View all Repair Claim Pre-authorization tables.|
|Pre-authorization navigator \[sn\_repr\_claim\_mgmt.pre\_auth\_navigation\_menu\]|Access to related list menu for pre-authorization in workspace.|
|Warranty specialist \[sn\_claim\_cmn.warranty\_specialist\]|View and update pre-authorization request. Also, can view Repair claim. This role is for user who can approve/reject/send-back pre-authorization request.|

<table id="table_gcj_mk2_bhc"><thead><tr><th>

Feature set

</th><th>

Granular roles

</th><th>

Supported entities

</th></tr></thead><tbody><tr><td>

Recall campaign

</td><td>

sn\_rcl\_claim\_mgmt.campaign.creatorsn\_rcl\_claim\_mgmt.campaign.viewer

sn\_rcl\_claim\_mgmt.campaign.writer

sn\_rcl\_claim\_mgmt.campaign\_phase.writer

</td><td>

sn\_rcl\_claim\_mgmt\_ca

 Corrective action charges

 sn\_rcl\_claim\_mgmt\_ca\_charges

 sn\_rcl\_claim\_mgmt\_rcp

 sn\_rcl\_claim\_mgmt\_phase\_task

 sn\_rcl\_claim\_mgmt\_rcp\_phase

</td></tr><tr><td>

Recall campaign phase

</td><td>

sn\_rcl\_claim\_mgmt.campaign\_phase.writersn\_rcl\_claim\_mgmt.campaign.viewer

</td><td>

sn\_rcl\_claim\_mgmt\_rcp\_phase

 sn\_rcl\_claim\_mgmt\_phase\_task

</td></tr></tbody>
</table>## System roles containing granular responsibility roles

<table id="table_afj_5k2_bhc"><thead><tr><th>

System roles

</th><th>

Granular roles

</th></tr></thead><tbody><tr><td>

Recall Manager \[sn\_rcal\_claim\_mgmt.recall\_manager\]

</td><td>

sn\_rcl\_claim\_mgmt.campaign.creatorsn\_rcl\_claim\_mgmt.campaign.viewer

sn\_rcl\_claim\_mgmt.campaign.writer

sn\_rcl\_claim\_mgmt.campaign\_phase.writer

</td></tr><tr><td>

Recall Phase Owner \[sn\_rcl\_claim\_mgmt.recall\_phase\_owner\]

</td><td>

sn\_rcl\_claim\_mgmt.campaign\_phase.writersn\_rcl\_claim\_mgmt.campaign.viewer

</td></tr><tr><td>

Warranty Specialist \[sn\_claim\_cmn.warranty\_specialist\]

</td><td>

financial\_mgmt\_user sn\_customerservice\_agent

sn\_dealer\_mgmt.dealer\_viewer sn\_mfg\_cmn.navigation\_menu

sn\_prd\_pm.product\_catalog\_viewer

sn\_prm.enterprise\_partner\_agent

sn\_repr\_claim\_mgmt.claim\_viewer

sn\_repr\_claim\_mgmt.navigation\_menu

sn\_repr\_claim\_mgmt.pre\_auth\_navigation\_menu

sn\_repr\_claim\_mgmt.repair\_pre\_auth\_charge\_creator

sn\_repr\_claim\_mgmt.repair\_pre\_auth\_writer

</td></tr></tbody>
</table>