---
title: CI ownership agentic workflow reference
description: The CI ownership agentic workflow uses a set of tables, properties, and a role to propose and apply CI ownership assignments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-ref.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 4
keywords: [CI ownership, reference, tables, system properties, roles, CMDB, ServiceNow Otto for CMDB]
breadcrumb: [CI ownership agentic workflow, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI ownership agentic workflow reference

The CI ownership agentic workflow uses a set of tables, properties, and a role to propose and apply CI ownership assignments.

## Stages

The CI ownership agentic workflow runs in three stages.

-   **Group profile builder**

    Runs on a schedule \(**CMDBCIOwnershipBuildGroupProfile**\), inactive by default. For each group that owns or could own CIs, the workflow samples a set of that group's CIs and consolidates the sample.

    It then writes a plain-language profile of what the group owns. Profiles refresh only after they age past the configured refresh interval.

-   **CI ownership inference**

    Runs hourly \(**CMDBCIOwnershipInference**\), inactive by default. Finds unowned, in-scope CIs and retrieves the most relevant group profiles for each CI.

    It proposes an owning group and a confidence rating for each CI. Proposals with a high enough confidence rating are applied to the CI automatically. All other proposals are queued for review.

-   **Assignment review**

    Queued proposals are grouped into an assignment recommendation per owning group. A reviewer approves or rejects an entire recommendation from its list, or opens a recommendation and approves or rejects individual candidates from its related list.

    Approving a candidate writes the proposed owning group onto its CI and marks the candidate approved. Rejecting marks a candidate rejected without changing the CI.


## AI agent

The CI ownership recommender guides you through the same actions in a conversation, from the ServiceNow Otto panel. It doesn't trigger automatically on a record. Example trigger phrases include `Help me with missing CI owners` and `Review CI ownership recommendations`.

|Tool|Description|
|----|-----------|
|Activation Manager|Reports whether the workflow is activated and its scheduled jobs are running.|
|Activate Jobs|Activates the scheduled jobs if they're inactive. Requires your confirmation because it changes system state.|
|Add CIs for recommendation|Returns a link to a filtered list of CIs that you can add to the inference queue.|
|Get queued items|Summarizes the status of CIs that you personally queued for inference.|
|Get Open Recommendations|Summarizes open assignment recommendations across the organization.|

## Tables

The CI ownership agentic workflow uses the following tables.

|Table|Purpose|
|-----|-------|
|CI Ownership Group Profile \[sn\_cmdb\_gen\_ai\_ci\_ownership\_group\_profile\]|One row per group. Stores the plain-language profile of what CIs a group owns.|
|CI Ownership Group Profile Sampling \[sn\_cmdb\_gen\_ai\_ci\_ownership\_group\_profile\_sampling\]|Working table. The CIs selected as a group's sample for one profiling run.|
|CI Ownership Group Profile Processing \[sn\_cmdb\_gen\_ai\_ci\_ownership\_group\_profile\_processing\]|Working table. The consolidated sample data sent to the profile builder skill for one group and run.|
|CI Ownership Job Context \[sn\_cmdb\_gen\_ai\_ci\_ownership\_job\_context\]|Shared state for the scheduled jobs, such as the mutual-exclusion lock between profile building and inference.|
|CI Ownership Candidate \[sn\_cmdb\_gen\_ai\_ci\_ownership\_candidate\]|One proposed owner assignment for one CI, with a confidence rating and an explanation. The record a reviewer approves or rejects.|
|CI Ownership Assignment Recommendation \[sn\_cmdb\_gen\_ai\_ci\_ownership\_assignment\_recommendation\]|A batch of candidates for the same owning group, reviewed together. Extends the Task \[task\] table.|
|CI Ownership Assignment Recommendation Processing \[sn\_cmdb\_gen\_ai\_ci\_ownership\_assignment\_recommendation\_processing\]|Progress tracker for applying a reviewed recommendation's decision to its candidates.|
|CI Ownership Inference Queue \[sn\_cmdb\_gen\_ai\_ci\_ownership\_inference\_queue\]|CIs waiting to be evaluated by the inference stage.|
|CI Ownership User Issuing Inference \[sn\_cmdb\_gen\_ai\_ci\_ownership\_user\_issuing\_inference\]|Records which user queued a batch of CIs for inference, and when.|

## System properties

All of these properties exist as System Properties \[sys\_properties\] records that an admin can edit.

**Note:** To access the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

|Property|Default|Description|
|--------|-------|-----------|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_type**|managed\_by\_group|The Configuration Item \[cmdb\_ci\] field that the workflow evaluates and assigns. Must be a field that references the Group \[sys\_user\_group\] table.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_sample\_size**|100|Total number of CIs sampled per group in one profiling run.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_sample\_hq\_percentage**|0.6|Fraction of the sample reserved for CIs from already-approved ownership assignments.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_sample\_recency\_days**|180|Lookback window, in days, for CIs eligible for sampling.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_user\_group\_batch\_size**|20|Maximum number of groups profiled in one profile-builder run.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_profile\_refresh\_days**|7|Minimum age, in days, before a group's profile is eligible to be rebuilt.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_group\_candidate\_followup\_hours**|4|Hours until the profile-builder job runs again when groups still need profiling.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_semantic\_sample\_cap**|100|Maximum number of values collected per free-text field when consolidating a sample.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_class\_min\_ownership\_rate**|0.1|Minimum ratio of owned to total CIs a CI class needs to be included in profiling and inference.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_fallback\_target\_classes**|cmdb\_ci\_computer, cmdb\_ci\_server, cmdb\_ci\_database, cmdb\_ci\_cloud\_database, cmdb\_ci\_vm\_instance, cmdb\_ci\_ip\_router|CI classes added when no class meets the minimum ownership rate.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_target\_classes\_count**|5|Maximum number of CI classes retained for profiling and inference.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_predefined\_target\_classes**|Empty|CI classes the Configuration Items list restricts to on the CI Ownership Inference Custom Request view. Empty by default, which applies no class restriction.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_auto\_accept\_confidence\_minimum\_rating**|Empty|Minimum confidence rating required for a proposal to be applied automatically without review. Empty by default, which disables automatic approval.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_ci\_input\_fields**|sys\_class\_name, environment, vendor.name, business\_unit.name, cost\_center.name, company.name, department.name, location.name, manufacturer.name, support\_group, managed\_by\_group, assignment\_group, name, short\_description|CI fields the workflow reads when building profiles and running inference.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_inference\_batch\_size**|1000|Maximum number of CIs evaluated per inference run. Capped at 1000.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_inference\_max\_retries**|3|Number of times a failed inference queue entry is retried before it's marked skipped.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_max\_retrieved\_ai\_search\_result**|10|Number of group profiles the AI Search retrieval step returns per CI before inference narrows the list down to the most relevant group profiles.|
|**sn\_cmdb\_gen\_ai.ci\_ownership\_assignment\_rec\_batch\_size**|1000|Number of candidates processed per batch when a reviewed recommendation's decision is applied to its candidates.|

**Related topics**  


[CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-c.md)

[Activate the CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-ci-ownership.md)

[Determine the owner of a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md)

