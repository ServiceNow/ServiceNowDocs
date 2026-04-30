---
title: Landing page and dashboard views
description: The landing page in the Operational Resilience Workspace provides a single-pane overview of the services, business services, and pillars in your organization. The dashboard displays resilience metrics, including operational status, completed activities, red flags, and suggestions for improvement.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Operational Resilience, Governance, Risk, and Compliance]
---

# Landing page and dashboard views

The landing page in the Operational Resilience Workspace provides a single-pane overview of the services, business services, and pillars in your organization. The dashboard displays resilience metrics, including operational status, completed activities, red flags, and suggestions for improvement.

The flexible data model introduced with Operational Resilience, Release 21.0.x provides a foundation for the dashboards and tracks the flow of dependent services. The data, including red flags by type, such as failed controls, incidents, and outages, and business service metrics such as number of flags, importance, and impact tolerance, is updated in the dashboard through changes to the flexible data model.

![Dashboard data.](../../grc-operational-res/image/dashboard-data.png)

The data shown in the example is for business services such as business service by number of red flags, business service by importance, business service by impact tolerance. You can change it service offerings, business processes, or application services by configuring the **sn\_oper\_res.top\_class\_name** property. You can then change the top class to another object and the system shows data with respect to that specific top class.

## Calculation and roll up of red flags

The dashboard shown in the earlier example displays a range of 1-30 red flags. Upon selecting, it shows a detailed breakdown, showing a total of 20 red flags, with 3 specifically attributed to the "cards and payments" level. This illustrates the roll-up functionality, which aggregates red flags beneath the selected "Cards and Payments" business service, providing a hierarchical view of the data.

![red flags.](../../grc-operational-res/image/red-flags-breakup.png)

The value "24" shown in the Total red flags count column is the roll-up value of the red flags for all entities under the "Cards and Payments" business service.

The **Calculate red flags for CSDM and dependencies** scheduled job does not create new records in the \[sn\_oper\_res\_profile\] table. Instead, it recomputes the impacted objects for the existing sn\_oper\_res\_profile records using data from the \[sn\_grc\_m2m\_profile\_profile\] table.

The **Calculate red flags for CSDM and dependencies** scheduled job fetches the red flags for the profiles in the \[sn\_oper\_res\_profile\] table only when the following conditions are met:

-   The **sn\_oper\_res\_profile.pillar** is not empty.
-   The **sn\_oper\_res\_profile.applies\_to** field is not empty.

The red flags fetching mechanism can use either the **sn\_oper\_res\_profile.profile** condition, the **sn\_oper\_res\_profile.applies\_to** condition, or a combination of both.

The red flags also inherit the impacted objects and impacted object classes from the \[sn\_oper\_res\_profile\] record. For example if an application service's Operational Resilience profile lists Business service, Offering, and Business process as impacted objects \(shown in the Impacted objects column\), these objects are copied to all associated red flags for the application service and its related entities.

**Note:** The \[sn\_oper\_res\_profile\] record is created for an entity that is created without the **applies\_to** record. When an entity is linked properly to its respective records, integrations with risks, failed controls, incidents, and issues function properly.

## Conditions for calculating the red flags

This section uses the **sn\_oper\_res\_profile.profile** and **sn\_oper\_res\_profile.applies\_to** conditions for reference. The criteria for calculating red flags and the relevant tables are detailed in the Red flags calculation table.

<table id="table_f3j_mbw_bgc"><thead><tr><th>

Red flags

</th><th>

Table

</th><th>

Conditions

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

High risks - Advanced risk

</td><td>

\[sn\_risk\_advanced\_risk\_assessment\_instance\]

</td><td>

Conditions:-   entity\_1=profile
-   status=30
-   summary\_residual\_risk\_score should be greater then the higher than the max criteria defined in risk\_assessment\_methodology
-   Should not have any open assessments linked to sn\_risk\_advanced\_risk\_assessment\_instance

</td><td>

For all these risks, staging records are created in the \[sn\_oper\_res\_risk\] table.

</td></tr><tr><td>

Failed controls: Step 1 \(Optional\)

</td><td>

\[sn\_compliance\_m2m\_control\_entity\] \(sn\_compliance\_control ← → sn\_grc\_profile\)

</td><td>

Conditions:-   entity=profile
-   control.status=non\_compliant
-   control.exempt=false
-   control.state=monitor
-   control.active=true

</td><td>

A list of controls is extracted and are valid red flags.

</td></tr><tr><td>

Failed controls: Step 2

</td><td>

\[sn\_compliance\_control\]

</td><td>

Conditions:-   entity=profile or sys\_id in the list of controls
-   control.status=non\_compliant
-   control.exempt=false
-   control.state=monitor
-   control.active=true

</td><td>

For all these controls, staging records are created in the \[sn\_oper\_res\_failed\_control\] table.

</td></tr><tr><td>

Issues: Step 1 \(Optional\)

</td><td>

\[sn\_grc\_m2m\_issue\_to\_entity\] \(sn\_grc\_issue ←→ sn\_grc\_profile\)

</td><td>

Conditions:-   entity=profile
-   sn\_grc\_issue.active=true

</td><td>

A list of issues is extracted and are valid red flags.

</td></tr><tr><td>

Issues: Step 2 \(Optional\)If one of the following pillars is used, then this step is considered:

-   Service
-   Business service
-   Offering

</td><td>

-   \[sn\_oper\_res\_m2m\_scenario\_event\_issue\] \(scenario\_event ←→ sn\_grc\_issue\)
-   \[sn\_oper\_res\_m2m\_scenario\_event\_service\] \(scenario\_event ←→ service\)

</td><td>

A joint query is performed using the two tables and \[sn\_grc\_issue\] is fetched for the service, business service, and offering.

</td><td>

These are appended in the list of issues from step 1.

</td></tr><tr><td>

Issues: Step 3

</td><td>

\[sn\_grc\_issue\]

</td><td>

Conditions:-   entity=profile or sys\_id in the list of controls
-   active=true
-   In addition, the issues should not have any exception policy.
-   Exception policy can be checked in the \[sn\_compliance\_policy\_exception\] table with two conditions:
    -   validity&gt;now
    -   state=8

</td><td>

For all these issues, staging records are created in the \[sn\_oper\_res\_issue\] table.

</td></tr><tr><td>

Incident: Step 1

</td><td>

incident

</td><td>

Conditions:-   cmdb\_ci=profile.applies\_to
-   state IN \[1,2\]

</td><td rowspan="3">

For all these incidents, staging records are created in the \[sn\_oper\_res\_incident\] table.

</td></tr><tr><td>

Incident: Step 2 \(Optional\)

</td><td>

\[task\_ci\]

</td><td>

Conditions:-   ci\_item=profile.applies\_to
-   task.sys\_class\_name=incident
-   task.state IN \[1,2\]

</td></tr><tr><td>

Incident: Step 3

</td><td>

\[task\_cmdb\_ci\_service\]

</td><td>

Conditions:-   cmdb\_ci\_service=profile.applies\_to
-   task.sys\_class\_name=incident
-   task.state IN \[1,2\]

</td></tr><tr><td>

Change request: Step 1

</td><td>

\[change\_request\]

</td><td>

Conditions:-   cmdb\_ci=profile.applies\_to
-   active=true

</td><td rowspan="3">

For all these change requests, staging records are created in the \[sn\_oper\_res\_change\_request\] table.

</td></tr><tr><td>

Change request: Step 2 \(Optional\)

</td><td>

\[task\_ci\]

</td><td>

Conditions:-   ci\_item=profile.applies\_to
-   task.sys\_class\_name=change\_request
-   task.active=true

</td></tr><tr><td>

Change request: Step 3

</td><td>

\[task\_cmdb\_ci\_service\]

</td><td>

Conditions:-   cmdb\_ci\_service=profile.applies\_to
-   task.sys\_class\_name=change\_request
-   task.state IN \[1,2\]

</td></tr><tr><td>

Outage

</td><td>

-   \[cmdb\_outage\_ci\_mtom\] \(cmdb\_ci ←→ cmdb\_ci\_outage\)
-   \[cmdb\_ci\_outage\] \(cmdb\_ci\)

 For each record in \[cmdb\_ci\_outage\], one record is created in the \[cmdb\_ci\_outage\_ci\_mtom\] table. In \[cmdb\_ci\_outage\], for each affected CIs, a record is inserted in the \[cmdb\_ci\_outage\_ci\_mtom\] table.

</td><td>

Conditions:-   ci\_item=profile.applies\_to
-   outage.type IN \[degradation, outage\]
-   outage.end IS empty OR outage.end &gt; now

</td><td>

For all these outages, staging records are created in the \[sn\_oper\_res\_outage\] table.

</td></tr><tr><td>

Task

</td><td>

\[task\]

</td><td>

Conditions:-   cmdb\_ci=profile.applies\_to
-   active=true
-   sys\_class\_name IN &lt;list of classes fetched from property sn\_oper\_res.allowed\_task\_tables
-   As part of base system, it considers only problem records.

</td><td>

For all these tasks, staging records are created in the \[sn\_oper\_res\_task\] table.

</td></tr><tr><td>

Operational vulnerabilities: Step 1 \(optional\)

</td><td>

\[sn\_grc\_case\_mgmt\_related\_area\]

</td><td>

Conditions:-   related\_area=profile OR related\_area=profile.applies\_to
-   core\_case.sys\_class\_name=sn\_oper\_res\_vulnerability
-   core\_case.active=true

</td><td rowspan="2">

For all these vulnerabilities, staging records are created in the \[sn\_oper\_res\_vulnerability\_profile\] table.

</td></tr><tr><td>

Operational vulnerabilities: Step 2 \(optional\)

</td><td>

\[sn\_grc\_case\_mgmt\_impacted\_area\]

</td><td>

Conditions:-   impacted\_area=profile OR impacted\_area=profile.applies\_to
-   core\_case.sys\_class\_name=sn\_oper\_res\_vulnerability
-   core\_case.active=true

</td></tr><tr><td>

Third party risk assessments

</td><td>

\[sn\_vdr\_risk\_asmt\_assessment\]

</td><td>

Conditions:-   applies\_to IN \[core\_company, sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   state IN \[5, 8, 9\]
-   risk\_rating\_valid\_to &gt; now
-   risk\_rating = highestRiskRating
-   vendor = profile.applies\_to \(Note: This condition is different than the **applies\_to** field in the \[sn\_vdr\_risk\_asmt\_assessment\] table.\)
-   engagement = profile.applies\_to \(Note: This condition is different than the **applies\_to** field in the \[sn\_vdr\_risk\_asmt\_assessment\] table.\)

</td><td>

For all these assessments, staging records are created in the \[sn\_oper\_res\_tprm\] table.

</td></tr></tbody>
</table>**Note:** You can calculate red flags for entities with a pillar; for vulnerable items, the pillar must be Technology. For other red flags, entities must have a pillar, with no restrictions on the type.

## Sample query conditions for Operational Resilience integration

The Operational Resilience application uses entities to integrate with Risk Management, Advanced Risk, and Policy and Compliance Management. Operational Resilience uses the **applies\_to** value of an entity to integrate with other tables. To illustrate how these integrations work, the following table provides examples of query conditions for various integration types, demonstrating the role of Entity and **applies\_to** in facilitating these connections.

<table id="table_qk5_1sw_lgc"><thead><tr><th>

Table

</th><th>

Condition

</th><th>

Function

</th><th>

Integrated Application

</th></tr></thead><tbody><tr><td>

task\_ci

</td><td>

-   task.sys\_class\_name=incident
-   task.state IN New, In progress
-   ci\_item = Applies\_to

</td><td>

\_createIncidentAndChangeRequestsWithImpactedAndAffectedCis

</td><td>

Incident

</td></tr><tr><td>

task\_ci

</td><td>

-   task.sys\_class\_name=change\_request
-   task.active=true
-   ci\_item = Applies\_to

</td><td>

\_createIncidentAndChangeRequestsWithImpactedAndAffectedCis

</td><td>

Change request

</td></tr><tr><td>

task\_cmdb\_ci\_service

</td><td>

-   task.sys\_class\_name=incident
-   cmdb\_ci\_service= Applies\_to

</td><td>

\_createIncidentWithCriticalService

</td><td>

Incident

</td></tr><tr><td>

task\_cmdb\_ci\_service

</td><td>

-   task.sys\_class\_name=change\_request
-   cmdb\_ci\_service= Applies\_to

</td><td>

\_createIncidentWithCriticalService

</td><td>

Change request

</td></tr><tr><td>

cmdb\_outage\_ci\_mtom

</td><td>

-   ci\_item = Applies\_to
-   outage.type = degradation or outage
-   outage.end is empty or after

</td><td>

\_createOpresOutageWithAffectedCis

</td><td>

Outage

</td></tr><tr><td>

sn\_grc\_case\_mgmt\_impacted\_area

</td><td>

-   Impacted\_area=Entity or Applies\_to
-   Core\_case.sys\_class\_name = sn\_oper\_res\_vulnerability
-   Core\_case.active=true

</td><td>

\_createOpresVulProfileForImpactedAreas

</td><td>

Operational Vulnerability

</td></tr><tr><td>

sn\_grc\_case\_mgmt\_related\_area

</td><td>

-   Related\_area=Entity or Applies\_to
-   Core\_case.sys\_class\_name = sn\_oper\_res\_vulnerability
-   Core\_case.active=true

</td><td>

\_createOpresVulProfileForRelatedAreas

</td><td>

Operational Vulnerability

</td></tr><tr><td>

sn\_grc\_m2m\_issue\_to\_entity

</td><td>

-   Issue’s active = true
-   Entity = Entity

</td><td>

\_createServiceWithOpenIssue

</td><td>

Issue

</td></tr><tr><td>

sn\_grc\_issue

</td><td>

-   Issue’s active = true
-   Entity = Entity

</td><td>

\_createServiceWithOpenIssue

</td><td>

Issue

</td></tr><tr><td>

 

</td><td>

-   Cmdb\_ci = Applies\_to
-   Active=true
-   Sys\_class\_name IN property 'sn\_oper\_res.allowed\_task\_tables'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Task

</td><td>

 

</td><td>

 

</td><td>

Task

</td></tr><tr><td>

Sn\_risk\_risk

</td><td>

-   Profile= Entity
-   State=monitor
-   Residual\_score=highest\_residual\_score
-   Content is NOT Empty
-   Active=true

</td><td>

\_\_serviceWithHighRisk

</td><td>

Risk

</td></tr><tr><td>

sn\_risk\_advanced\_risk\_assessment\_instance

</td><td>

-   entity\_1= Entity
-   status=completed
-   summary\_residual\_risk\_score=highest rating

</td><td>

\_advancedServiceWithHighRisk

</td><td>

Advanced risk

</td></tr><tr><td>

sn\_compliance\_m2m\_control\_entity

</td><td>

-   Control.Status=non\_compliant
-   Control.Exempt=false
-   Control.State=monitor
-   Control.active=true
-   Profile= Entity

</td><td>

\_createServiceWithFailedControl

</td><td>

Policy and compliance

</td></tr><tr><td>

sn\_compliance\_control

</td><td>

-   Status=non\_compliant
-   Exempt=false
-   State=monitor
-   Profile= Entity

</td><td>

createServiceWithFailedControl

</td><td>

Policy and compliance

</td></tr><tr><td>

sn\_bcp\_plan\_asset

</td><td>

\#1-   Item=Applies\_to
-   Types ‘contains’ 'primary\_scope'
-   Plan.expires after
-   Plan.state=approved

</td><td>

\_createServiceWithBCMPlan Otherwise, mark the Applies\_to as “No plan”

</td><td>

Business continuity management

</td></tr><tr><td>

sn\_recovery\_activated\_plan

</td><td>

\#2 -   Active=false
-   Plan=one from \#1

</td><td>

Otherwise, mark the Applies\_to as “No exercise”

</td><td>

 

</td></tr><tr><td>

sn\_recovery\_event\_asset

</td><td>

\#3 -   asset\_name= Applies\_to
-   event=one from \#2

</td><td>

If event asset’s state is ‘not recovered’, mark the Applies\_to as “No recovered”. Otherwise, mark the Applies\_to as “Recovered”

</td><td>

 

</td></tr><tr><td>

sn\_vul\_vulnerable\_item

</td><td>

-   risk\_rating=Critical or high
-   state NOT IN ‘closed, resolved, deferred’
-   Joined Query with Profile
-   Profile.pillar contains technology
-   Profile.active=true

</td><td>

\_computeVulnerabilityEntities

</td><td>

Vulnerability response

</td></tr><tr><td>

sn\_oper\_res\_tprm

</td><td>

-   applies\_toIN’vendor, engagement’
-   stateIN’submitted,response
-   received,follow-up’
-   risk\_rating\_valid\_to after
-   risk\_rating = highest rating
-   vendor= Applies\_to or engagement= Applies\_to

</td><td>

\_createServiceWithThirdPartyRiskAsmt

</td><td>

Third-party risk assessment

</td></tr></tbody>
</table>