---
title: Landing page and dashboard views
description: The landing page in the Operational Resilience Workspace provides a single-pane overview of the services, business services, and pillars in your organization. The dashboard displays resilience metrics, including operational status, completed activities, red flags, and suggestions for improvement.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
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
-   The **sn\_oper\_res\_profile.applies**\_to field is not empty.

The red flags fetching mechanism can use either the **sn\_oper\_res\_profile.profile** condition, the **sn\_oper\_res\_profile.applies\_to** condition, or a combination of both.

The red flags also inherit the impacted objects and impacted object classes from the \[sn\_oper\_res\_profile\] record. For example if an application service's Operational Resilience profile lists Business service, Offering, and Business process as impacted objects \(shown in the Impacted objects column\), these objects are copied to all associated red flags for the application service and its related entities.

**Note:** Beginning with Operational Resilience release 22.x.x, the **Calculate red flags for CSDM and dependencies** and **Update CSDM and other dependencies** scheduled jobs are deactivated by default for new installations. For existing installations, these jobs retain their current state \(active or inactive\).

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
</table>