---
title: Granular roles and entities
description: Module-level granular roles have been added to facilitate defining and configuring the responsibility framework. These roles enable tasks to be performed without creating custom access control lists \(ACLs\) on the target table when a responsibility ACL exists. This update aims to provide a more direct and declarative migration process.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
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
|Product Non-conformance Submitter \[sn\_mfg\_qm.product\_non\_conformance\_submitter\]|Create, view, update, and cancel a non-conformance case. They can also create a correction action and add expense lines to it.|
|Product Non-conformance Case Resolver \[sn\_mfg\_qm.product\_non\_conformance\_case\_resolver\]|Create, view, update across all non conformance related tables.|
|Quality Investigation Member \[sn\_mfg\_qm.product\_quality\_investigation\_member\]|Ability to edit product quality investigation and product quality investigation tasks. Can create remediation action plan, actions, and financial requests.​|
|Quality Investigation Lead \[sn\_mfg\_qm.product\_quality\_investigation\_lead\]|Create, view, update, and cancel quality investigation and all its related tables. This user also will sign off the investigation and move it to closure.​|
|Product Non-conformance Case Triager \[sn\_mfg\_qm.product\_non\_conformance\_case\_triager\]|New non-conformance submissions, validates completeness, sets priority/severity, and routes to the right resolver. Limited to triage updates; does not execute remediation.​|
|Finance Approver \[sn\_mfg\_qm.finance\_approver\]|Approve, Reject, Send Back Financial Request, Planned Line Charge, and Expense Line records.​|
|Remediation Plan Approver \[sn\_mfg\_qm.remediation\_plan\_approver\]|Review the proposed action plan and can record approval decisions and comments on the plan.​|
|Quality Issue Management Admin \[sn\_mfg\_qm.quality\_issue\_mgmt\_admin\]|Default access to all quality management features and tables.​|

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

</td></tr><tr><td>

Product Non-conformance

</td><td>

sn\_mfg\_qm.product\_non\_conformance\_submittersn\_mfg\_qm.product\_non\_conformance\_case\_resolver

sn\_mfg\_qm.product\_non\_conformance\_case\_triager

</td><td>

sn\_customerservice.case\_contributor\_creator

 sn\_dealer\_mgmt.dealer\_viewer

 sn\_customerservice.csm\_workspace\_user

 sn\_mfg\_qm.prd\_ncc\_creator

 sn\_customerservice.service\_organization\_contributor

 sn\_rm\_core.correction\_action\_creator

 playbook.agentic\_workflow\_user

 sn\_customerservice.requester

 knowledge

 sn\_customerservice.customer\_data\_viewer

 sn\_prm.external\_partner\_associate

 sn\_mfg\_ai\_agents.submitter\_ai\_playbook

 sn\_rm\_core.copq\_exp\_line\_creator

 sn\_rm\_core.issue\_cause\_creator

 sn\_mfg\_qm.impacted\_asset\_creator

 sn\_align\_core.apw\_user

 sn\_rm\_core.rem\_action\_creator

 sn\_mfg\_qm.product\_non\_conformance\_case\_triager

 sn\_rm\_core.copq\_planned\_line\_charge\_creator

 sn\_rm\_core.copq\_exp\_line\_creator

 sn\_rm\_core.containment\_action\_creator

 sn\_rm\_core.rem\_action\_plan\_creator

 personalize\_choices

 sn\_rm\_core.task\_cause\_association\_creator

 sn\_rm\_core.cause\_action\_plan\_creator

 sn\_mfg\_qm.impacted\_asset\_action\_creator

 sn\_mfg\_qm.prd\_qi\_viewer

</td></tr><tr><td>

Quality Issue Management

</td><td>

sn\_mfg\_qm.product\_quality\_investigation\_membersn\_mfg\_qm.product\_quality\_investigation\_lead

sn\_mfg\_qm.quality\_issue\_mgmt\_admin

</td><td>

sn\_rm\_core.copq\_exp\_line\_creator

 sn\_mfg\_qm.impacted\_asset\_creator

 sn\_mfg\_qm.impacted\_asset\_action\_creator

 sn\_rm\_core.corrective\_action\_creator

 sn\_rm\_core.correction\_action\_viewer

 sn\_rm\_core.rca\_task\_creator

 sn\_rm\_core.issue\_cause\_creator

 sn\_customerservice.csm\_workspace\_user

 sn\_rm\_core.preventive\_action\_creator

 knowledge

 sn\_mfg\_qm.prd\_qi\_writer

 sn\_mfg\_qm.prd\_qi\_task\_writer

 sn\_rm\_core.rem\_action\_creator

 sn\_rm\_core.cause\_action\_plan\_creator

 sn\_mfg\_qm.prd\_ncc\_viewer

 sn\_mfg\_qm.prd\_ncc\_task\_viewer

 sn\_rm\_core.copq\_planned\_line\_charge\_creator

 sn\_align\_core.apw\_user

 sn\_rm\_core.task\_cause\_association\_creator

 sn\_mfg\_qm.stakeholder\_viewer

 sn\_rm\_core.rem\_action\_plan\_creator

 sn\_rm\_core.cause\_action\_creator

 sn\_customerservice.case\_contributor\_viewer

 sn\_rm\_core.containment\_action\_creator

 sn\_rm\_core.copq\_fin\_req\_creator

 sn\_mfg\_qm.prd\_qi\_task\_creator

 sn\_mfg\_qm.stakeholder\_creator

 sn\_mfg\_qm.prd\_qi\_creator

 sn\_mfg\_qm.product\_quality\_investigation\_member

 sn\_mfg\_qm.remediation\_plan\_approver

 sn\_mfg\_qm.product\_quality\_investigation\_lead

 sla\_admin

 sn\_mfg\_qm.finance\_approver

 sn\_mfg\_qm.product\_non\_conformance\_case\_resolver

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