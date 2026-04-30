---
title: Services overview tab
description: The Services overview tab in the Operational Resilience Workspace provides a comprehensive summary of active services, highlighting any red flags or urgent issues, status of resilience activities like assessments, scenario analysis, self-attestations. It also offers suggestions for mitigating top risks or vulnerabilities and strengthening top controls.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Monitor, Operational Resilience, Governance, Risk, and Compliance]
---

# Services overview tab

The **Services overview** tab in the Operational Resilience Workspace provides a comprehensive summary of active services, highlighting any red flags or urgent issues, status of resilience activities like assessments, scenario analysis, self-attestations. It also offers suggestions for mitigating top risks or vulnerabilities and strengthening top controls.

## Services overview section on the landing page

Existing customers typically use the Service \(CMDB\) Main node configuration, while new customers use the Opres with CSDM header Main node configuration. Administrators can show the **Services overview** tab and hide the **Business services overview** tab from the Operational Resilience Workspace view based on your organizational needs.

![Services overview.](../../grc-operational-res/image/s-ov-hp.png)

## Tables associated with the Services overview tab

The following table lists all the tables that are associated with each section of the **Services overview** tab report.

<table id="table_rfd_rfm_cfc"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Services

</td></tr><tr><td>

Active services

</td><td>

Number of critical services delivered to your customers. Source table for this report: Active services \[sn\_grc\_m2m\_profile\_profile\_type\]

</td></tr><tr><td>

Services by number of red flags

</td><td>

Description for services by number of red flagsSource table for this report: Services by number of red flags \[sn\_oper\_res\_service\_summary\]

</td></tr><tr><td>

Services by importance

</td><td>

Description for services by importance.Source table for this report: Services by importance \[sn\_oper\_res\_service\_related\_info\]

</td></tr><tr><td>

Services by impact tolerance

</td><td>

Description for services by impact tolerance.Source table for this report: Services by impact tolerance \[sn\_oper\_res\_service\_related\_info\]

</td></tr><tr><td class="sub-head" colspan="2">

Red flags

</td></tr><tr><td>

Total red flags

</td><td>

Total red flags count for the affected service.

</td></tr><tr><td>

Red flags by type

</td><td>

Red flags by type. Source table for issues: Issue \[sn\_oper\_res\_issue\]

Source table for failed controls: Failed Controls \[sn\_oper\_res\_failed\_control\]

Source table for risks: Risks \[sn\_oper\_res\_risk\]

Source table for outages: Outages \[sn\_oper\_res\_critical\_service\_outage\]

Source table for incidents: Incidents \[sn\_oper\_res\_incident\]

Source table for change requests: Change requests \[sn\_oper\_res\_change\_request\]

Source table for Operational vulnerabilities: Operational vulnerabilities \[sn\_oper\_res\_vulnerability\_profile\]

Source table for Crisis events: Crisis events \[sn\_oper\_res\_bcm\_plan\]

Source table for vulnerabilities: Vulnerabilities \[sn\_oper\_res\_vul\_profile\]

</td></tr><tr><td>

Assets impacted by red flags

</td><td>

Assets that are impacted by the red flags shown for the pillars. For assets associated with the Process pillar are affected and shown in the red flags report. The source table is Assets impacted by red flags \[sn\_oper\_res\_service\_process\_pillar\]

</td></tr><tr><td class="sub-head" colspan="2">

Activities

</td></tr><tr><td>

Tasks

</td><td>

Tasks associated with the services.

</td></tr><tr><td>

Importance and impact assessments

</td><td>

Importance and impact assessments associated with the services. Source table is Importance and impact tolerance assessment \[sn\_oper\_res\_importance\_impact\_tolerance\_assessment\]

</td></tr><tr><td>

Scenario analysis

</td><td>

Scenario analysis associated with the services. Source table is Scenario analysis \[sn\_oper\_res\_scenario\_analysis\]

</td></tr><tr><td>

Self attestations

</td><td>

Self-attestations associated with the services. Source table is Self attestations \[sn\_oper\_res\_self\_attestation\]

</td></tr><tr><td class="sub-head" colspan="2">

Suggestions

</td></tr><tr><td>

Top Controls to be Strengthened

</td><td>

Failing controls that impact the most critical services. Source tables for this report are: Services with failed controls \[sn\_oper\_res\_failed\_control\]

</td></tr><tr><td>

Top Risks to be Mitigated

</td><td>

Top risks threatening your organization compared with your impacted services. This report can be useful for determining where to start your mitigation efforts and in what areas you should devote the most resources around implementing controls.Source table for this report: Services with high risks \[sn\_oper\_res\_risk\]

</td></tr><tr><td>

Top vulnerabilities to be fixed

</td><td>

Top vulnerabilities to be fixed for the services. Source table for this report: Services with operational vulnerabilities \[sn\_oper\_res\_vulnerability\_profile\]

</td></tr></tbody>
</table>## Summarized report on the services

The Services report on the **Services overview** tab provides a quick summary with precise metrics on the types of services and their current status.

![Services overview.](../../grc-operational-res/image/s-ov.png)

-   Active services
-   Services by number of red flags
-   Services by importance
-   Services by impact tolerance

## Report on the red flags

The Red flags report on the **Services overview** tab shows the total number of red flags that require immediate attention for the associated assets, controls, issues, and risks related to the selected service. It breaks down details of the red flags based on the integrations with the Operational Resilience application. For example, if you have installed the Policy and Compliance Management application, services data for the failed controls is pulled from that application and displayed in this report.

A sample Red flags report for the services is shown in the example.

![Red flags.](../../grc-operational-res/image/s-red-flags.png)

The following data is displayed for the services in the report:

-   Total red flags: Number of total red flags for the services is shown in this report. You can select the count in the report and view the actual status of the services.
-   Red flags by type: The counts for incidents, outages, change requests, operational vulnerabilities, risks, failed controls, and issues are updated on the service's overview page. Selecting the count takes you to a detailed red flags table. Child services are consolidated under their parent services for all services and dependencies. Depending on the applications integrated with Operational Resilience, services data is pulled from them and displayed in the report as shown in the example. The following data is displayed in the Red flags report:
    -   Issues
    -   Failed controls
    -   Risks
    -   Outages
    -   Incidents
    -   Change requests
    -   Operational vulnerabilities
    -   Crisis events
    -   Vulnerabilities
-   Assets impacted by red flags: Any service, child service, business process, or their dependencies are flagged as red flags under various pillars.

## Report on the Operational Resilience activities

The Activities report on the **Services overview** tab displays tasks and status for the following Operational Resilience activities for the services.

![Activities.](../../grc-operational-res/image/s-activities.png)

-   Tasks
-   Importance and impact assessments
-   Scenario analysis
-   Self attestations

## Suggestions for mitigating the issues

The Suggestions report on the **Services overview** tab offers recommendations and workarounds to mitigate issues and risks for various resilience metrics for the services.

![Suggestions.](../../grc-operational-res/image/s-suggestions.png)

Depending on the applications integrated with Operational Resilience, suggestions are displayed in the report. For example, if you have installed the Policy and Compliance Management, Risk Management, and Vulnerability Response applications, the following suggestions are displayed in the report.

-   Top controls to be strengthened
-   Top risks to be mitigated
-   Top vulnerabilities to be fixed

