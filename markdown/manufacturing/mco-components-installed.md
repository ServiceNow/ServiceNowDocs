---
title: Components installed
description: Several types of components are installed with installation of the Manufacturing Commercial Operations application. These components include user roles, tables, plugins, ServiceNow Store applications, and business rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-components-installed.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Manufacturing Commercial Operations]
---

# Components installed

Several types of components are installed with installation of the Manufacturing Commercial Operations application. These components include user roles, tables, plugins, ServiceNow Store applications, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed

User roles are assigned by the use case that is being supported. For each feature, there are both roles with view-only access and roles with various levels of interactive access.

<table id="table_h1g_24n_lfc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_mfg\_cmn.manufacturing\_operations\_admin

</td><td>

Administers who can access sensitive data by restricting how user acquire roles in the Manufacturing Commercial Operations applications.

</td><td>

-   sn\_sls\_prm\_clm\_mgt.bulk\_upload\_admin
-   sn\_sales\_prm\_mgmt.sales\_promotion\_manager
-   sn\_mfg\_cmn.input\_set\_writer
-   sn\_labr\_cmn.labr\_admin
-   sn\_repr\_claim\_mgmt.claim\_admin
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim
-   sn\_rcl\_claim\_mgmt.adminsn\_prd\_pm.product\_catalog\_admin
-   sn\_sales\_prm\_mgmt.sales\_promotion\_admin
-   sn\_prm.enterprise\_partner\_admin
-   sn\_dealer\_mgmt.dealer\_admin
-   sn\_customerservice\_manager
-   sn\_claim\_cmn.claims\_agent
-   sn\_prm.partner\_ui
-   sn\_repair\_claim\_mgmt.repair\_pre\_auth\_admin

</td></tr><tr><td>

sn\_claim\_cmn.claims\_agent

</td><td>

View, approve, recall, and reject claims.

</td><td>

-   sn\_sales\_prm\_mgmt.sales\_promotion\_viewer
-   sn\_prm.enterprise\_partner\_agent
-   sn\_rcl\_claim\_mgmt.campaign.viewer
-   sn\_customerservice\_agent
-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_repr\_claim\_mgmt.navigation\_menu
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_repr\_claim\_mgmt.claim\_writer
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim\_writer
-   sn\_mfg\_cmn.navigation\_menu
-   sn\_repr\_claim\_mgmt.charge\_creator
-   financial\_mgmt\_user
-   sn\_repair\_claim\_mgmt.repair\_pre\_auth\_viewer
-   sn\_repr\_claim\_mgmt.pre\_auth\_navigation\_menu

</td></tr><tr><td>

sn\_dealer\_mgmt.dealer\_service\_advisor

</td><td>

Create, view, update, and cancel repair claim cases.

</td><td>

-   sn\_repr\_claim\_mgmt.claim\_creator
-   sn\_rcl\_claim\_mgmt.campaign.viewer
-   sn\_customerservice.customer\_case\_manager
-   sn\_prd\_pm.external\_product\_viewer
-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_customerservice.requester
-   sn\_prm.external\_partner\_associate
-   sn\_repair\_claim\_mgmt.repair\_pre\_auth\_admin
-   sn\_repr\_claim\_mgmt.pre\_auth\_navigation\_menu

</td></tr><tr><td>

sn\_dealer\_mgmt.dealer\_sales\_agent

</td><td>

Create, view, update, and cancel a sales promotion claim case.

</td><td>

-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_prm.external\_partner\_associate
-   sn\_sls\_prm\_clm\_mgt.bulk\_upload\_creator
-   sn\_sales\_prm\_mgmt.sales\_promotion\_viewer
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim\_creator
-   sn\_customerservice.case\_contributor\_creator
-   sn\_customerservice.requester

</td></tr><tr><td>

sn\_rcl\_claim\_mgmt.recall\_manager

</td><td>

Create, read, and update a recall campaign claim.

</td><td>

sn\_rcl\_claim\_mgmt.campaign.creator

</td></tr><tr><td>

sn\_sales\_prm\_mgmt.sales\_promotion\_manager

</td><td>

Create, read, update, and cancel a sales promotion.

</td><td>

-   sn\_sales\_prm\_mgmt.sales\_promotion\_creator
-   sn\_sls\_prm\_clm\_mgt.sales\_promotion\_claim\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_mfg\_cmn.navigation\_menu

</td></tr><tr><td>

sn\_dealer\_mgmt.dealer\_operations\_admin

</td><td>

Create, read, update, or cancel all claims.

</td><td>

-   sn\_prm.external\_partner\_manager
-   sn\_sls\_prm\_clm\_mgt.bulk\_upload\_admin
-   sn\_dealer\_mgmt.dealer\_sales\_agent
-   sn\_dealer\_mgmt.dealer\_service\_advisor

</td></tr><tr><td>

sn\_rcl\_claim\_mgmt.recall\_phase\_owner

</td><td>

Update, publish, close, and cancel a recall campaign phase or sub-phase.

</td><td>

sn\_rcl\_claim\_mgmt.campaign\_phase.writer

</td></tr><tr><td>

sn\_claim\_cmn.warranty\_specialist

</td><td>

View, approve, return, or reject pre-authorization requests.

</td><td>

-   sn\_customerservice\_agentsn\_dealer\_mgmt.dealer\_viewer
-   sn\_repr\_claim\_mgmt.navigation\_menu
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_mfg\_cmn.navigation\_menu
-   financial\_mgmt\_user
-   sn\_repair\_claim\_mgmt.repair\_pre\_auth\_writer
-   sn\_repair\_claim\_mgmt.repair\_pre\_auth\_charge\_creator
-   sn\_repair\_claim\_mgmt.claim\_viewer
-   sn\_repr\_claim\_mgmt.pre\_auth\_navigation\_menu

</td></tr><tr><td>

sn\_mfg\_qm.admin

</td><td>

Full access to all Quality Issue Management \(QIM\) features, tables, and configuration.

</td><td>

-   sn\_mfg\_qm.product\_quality\_investigation\_lead sla\_admin
-   sn\_mfg\_qm.finance\_approver
-   sn\_mfg\_qm.product\_non\_conformance\_case\_resolver

</td></tr><tr><td>

sn\_mfg\_qm.triager

</td><td>

Review new submissions, check completeness, determine priority and severity, assign to resolvers, and update triage information.

</td><td>

-   sn\_mfg\_qm.prd\_qi\_viewer
-   sn\_mfg\_qm.product\_non\_conformance\_submitter
-   sn\_mfg\_qm.prd\_ncc\_task\_creator

</td></tr><tr><td>

sn\_mfg\_qm.resolver

</td><td>

Work the full PNCC playbook: correction, impacted assets, containment, and closure. Create Quality Investigations.

</td><td>

-   sn\_mfg\_qm.prd\_qi\_creator
-   sn\_rm\_core.cause\_action\_creator
-   sn\_rm\_core.rca\_task\_creator
-   sn\_customerservice.case\_contributor\_viewer
-   sn\_rm\_core.issue\_cause\_creator
-   sn\_mfg\_qm.impacted\_asset\_creator
-   sn\_rm\_core.copq\_fin\_req\_creator
-   sn\_align\_core.apw\_user sn\_rm\_core.rem\_action\_creator
-   sn\_mfg\_qm.product\_non\_conformance\_case\_triager
-   sn\_rm\_core.copq\_planned\_line\_charge\_creator
-   sn\_rm\_core.copq\_exp\_line\_creator
-   sn\_rm\_core.correction\_action\_creator
-   sn\_rm\_core.containment\_action\_creator
-   sn\_rm\_core.rem\_action\_plan\_creator personalize\_choices
-   sn\_rm\_core.task\_cause\_association\_creator
-   sn\_rm\_core.cause\_action\_plan\_creator
-   sn\_mfg\_qm.impacted\_asset\_action\_creator

</td></tr><tr><td>

sn\_mfg\_qm.investigation\_member

</td><td>

Create, view, update, and cancel a quality investigation and related records. Sign off the investigation and move it to closure.

</td><td>

-   sn\_rm\_core.copq\_exp\_line\_creator
-   sn\_mfg\_qm.impacted\_asset\_creator
-   sn\_mfg\_qm.impacted\_asset\_action\_creator
-   sn\_rm\_core.corrective\_action\_creator
-   sn\_rm\_core.correction\_action\_viewer
-   sn\_rm\_core.rca\_task\_creator
-   sn\_rm\_core.issue\_cause\_creator
-   sn\_customerservice.csm\_workspace\_user
-   sn\_rm\_core.preventive\_action\_creator knowledge
-   sn\_mfg\_qm.prd\_qi\_writer sn\_mfg\_qm.prd\_qi\_task\_writer
-   sn\_rm\_core.rem\_action\_creator
-   sn\_rm\_core.cause\_action\_plan\_creator
-   sn\_mfg\_qm.prd\_ncc\_viewer
-   sn\_mfg\_qm.prd\_ncc\_task\_viewer
-   sn\_rm\_core.copq\_planned\_line\_charge\_creator
-   sn\_align\_core.apw\_user
-   sn\_rm\_core.task\_cause\_association\_creator
-   sn\_mfg\_qm.stakeholder\_viewer
-   sn\_rm\_core.rem\_action\_plan\_creator
-   sn\_rm\_core.cause\_action\_creator
-   sn\_customerservice.case\_contributor\_viewer
-   sn\_rm\_core.containment\_action\_creator
-   sn\_rm\_core.copq\_fin\_req\_creator

</td></tr><tr><td>

sn\_mfg\_qm.remediation\_plan\_approver

</td><td>

Approve or reject remediation action plans before they are enacted.

</td><td>

-   sn\_rm\_core.copq\_exp\_line\_creator
-   sn\_customerservice.csm\_workspace\_user
-   sn\_mfg\_qm.prd\_ncc\_viewer
-   sn\_rm\_core.cause\_action\_plan\_viewer
-   sn\_mfg\_qm.stakeholder\_viewer
-   sn\_mfg\_qm.prd\_qi\_task\_viewer
-   sn\_install\_base.install\_base\_viewer
-   sn\_rm\_core.cause\_action\_viewer
-   sn\_rm\_core.rca\_task\_viewer
-   sn\_rm\_core.rem\_action\_plan\_viewer
-   sn\_rm\_core.copq\_fin\_req\_viewer
-   sn\_rm\_core.issue\_cause\_viewer
-   sn\_mfg\_qm.prd\_ncc\_task\_viewer
-   sn\_mfg\_qm.prd\_qi\_viewer
-   sn\_mfg\_qm.impacted\_asset\_action\_viewer
-   sn\_rm\_core.copq\_planned\_line\_charge\_viewer
-   sn\_mfg\_qm.impacted\_asset\_viewer
-   sn\_rm\_core.task\_cause\_association\_viewer

</td></tr><tr><td>

sn\_mfg\_qm.finance\_approver

</td><td>

Approve Cost of Poor Quality \(COPQ\) financial requests and expense lines.

</td><td>

-   sn\_rm\_core.containment\_action\_viewer
-   sn\_rm\_core.preventive\_action\_viewer
-   sn\_mfg\_qm.impacted\_asset\_viewer
-   sn\_rm\_core.copq\_fin\_req\_viewer
-   sn\_rm\_core.rem\_action\_viewer
-   sn\_rm\_core.copq\_planned\_line\_charge\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_mfg\_qm.prd\_ncc\_task\_viewer
-   sn\_rm\_core.corrective\_action\_viewer
-   sn\_mfg\_qm.prd\_qi\_task\_viewer
-   sn\_rm\_core.issue\_cause\_viewer
-   sn\_rm\_core.rem\_action\_plan\_viewer
-   sn\_rm\_core.cause\_action\_plan\_viewer
-   sn\_mfg\_qm.impacted\_asset\_action\_viewer
-   sn\_mfg\_qm.prd\_qi\_viewer
-   sn\_rm\_core.correction\_action\_viewer
-   sn\_mfg\_qm.stakeholder\_viewer
-   sn\_mfg\_qm.prd\_ncc\_viewer
-   sn\_install\_base.install\_base\_viewer
-   sn\_rm\_core.copq\_exp\_line\_viewer
-   sn\_rm\_core.task\_cause\_association\_viewer
-   sn\_rm\_core.rca\_task\_viewer
-   sn\_rm\_core.cause\_action\_viewer

</td></tr><tr><td>

sn\_mfg\_qm.submitter

</td><td>

Create, view, update, and cancel a non-conformance case. Create a correction action and add expense lines to it.

</td><td>

-   sn\_customerservice.case\_contributor\_creator
-   sn\_dealer\_mgmt.dealer\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_mfg\_qm.prd\_ncc\_creator
-   sn\_customerservice.service\_organization\_contributor
-   sn\_rm\_core.correction\_action\_creator
-   playbook.agentic\_workflow\_user
-   sn\_customerservice.requester knowledge
-   n\_customerservice.customer\_data\_viewer
-   sn\_prm.external\_partner\_associate
-   sn\_mfg\_ai\_agents.submitter\_ai\_playbooks
-   sn\_rm\_core.copq\_exp\_line\_creator

</td></tr></tbody>
</table>-   **[Components installed with additional plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-components-installed-with-other-product-workflows.md)**  
Several types of components are installed when you activate the Customer Service Management and Cash to lead, applications.

**Parent Topic:**[Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-reference.md)

**Related topics**  


[Explore Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-explore.md)

