---
title: MCP Server Tools reference
description: Reference for the tools available in the HRSD MCP Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/mcp-server-tools-reference.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [HRSD MCP Server, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# MCP Server Tools reference

Reference for the tools available in the HRSD MCP Server.

<table id="table_tqj_j3z_ckc"><thead><tr><th>

Tool name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_hr\_mcp\_server.hrsd\_case\_initiate

</td><td>

Opens an HR case for an employee and returns the case number and state.

</td></tr><tr><td>

sn\_hr\_mcp\_server.hrsd\_service\_lookup

</td><td>

Browses the HR services a given employee is eligible to request and returns for each service: name, description, and Center of Excellence \(COE\).

</td></tr><tr><td>

sn\_hr\_mcp\_server.hrsd\_case\_lookup

</td><td>

Finds and reports on the status of HR cases, including service-level agreement \(SLA\) and last activity. Users can look up cases by number, short description, or see a list of their cases.

</td></tr><tr><td>

sn\_hr\_mcp\_server.hrsd\_case\_comment\_add

</td><td>

Adds a comment or work note to an existing HR case. Comments are visible to employees; work notes are only visible to agents.

</td></tr><tr><td>

sn\_hr\_mcp\_server.hrsd\_case\_advance

</td><td>

Progresses an existing HR case toward resolution or closure. Cases can only be advanced from the Work in progress state. The terminal returns a blocked transaction message if an HR agent attempts to advance a case that is in the following states: Draft, Awaiting Approval, Awaiting User Acceptance, Suspended, or Closed.

</td></tr><tr><td>

sn\_hr\_mcp\_server.hrsd\_knowledge\_search

</td><td>

Finds and cites the official knowledge article that answers an HR policy question. This tool returns only the policy text; it does not compute balances or amounts.

</td></tr><tr><td>

sn\_hr\_mcp\_server.hrsd\_eligibility\_check

</td><td>

Returns a yes or no answer to eligibility questions.

</td></tr></tbody>
</table><table><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

sn\_hr\_mcp\_server.knowledge.search\_profile

</td><td>

Specify the AI Search profile \(`ais_search_profile.name`\) that `hrsd_knowledge_search` queries use. Default: the profile used by Employee Center HR portal search \(`sn_hr_sp_esc_search_result_configuration`\)

Behavior:

-   With valid profile: Queries use the specified profile configuration
-   Unset or invalid: Search is unavailable; an error names this property and describes the issue

**Note:** There is no fallback engine. The tool requires an explicit, valid profile to operate.

</td></tr><tr><td>

sn\_hr\_mcp\_server.knowledge.applicability\_map

</td><td>

Declare which article fields encode applicability dimensions using a JSON mapping. This enables the tool to perform dimension-scoped result narrowing and generate facets beyond the knowledge structure hierarchy.Behavior:

-   With mapping: Result narrowing and faceting use both knowledge structure \(bases, categories, taxonomy\) and the specified applicability fields
-   Without mapping \(default\): Narrowing and faceting use knowledge structure only

**Note:** Invalid or non-existent field references will produce an error that names this property and the offending field.

Example:

```
{
  "region": {
    "field": "u_region"
  }
}
```

</td></tr><tr><td>

sn\_hr\_mcp\_server.knowledge.authority\_tiers

</td><td>

Map knowledge bases to authority tiers \(1–4\) to rank sources by authoritativeness and enable authority-based filtering.1.  Official policy
2.  Process documentation
3.  FAQ
4.  Informal \(community, tips, etc.\)

Behavior:

-   With mapping: Results rank by tier; users can filter by authority level.
-   Without mapping \(default\): Tier-neutral ranking; authority filtering is unavailable.

**Note:** Invalid or non-existent field references will produce an error that names this property and the offending field.

Example:

```
{
  "HR Policies": 1,
  "Onboarding Process": 2,
  "Common Questions": 3,
  "Team Tips": 4
}
```

</td></tr></tbody>
</table>