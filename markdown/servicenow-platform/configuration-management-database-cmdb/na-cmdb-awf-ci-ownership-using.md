---
title: Determining CI ownership
description: The CI ownership agentic workflow builds a profile of what each group in your organization owns. It then identifies configuration items with no owning group and proposes an owner for each one. A reviewer approves or rejects each proposal before it's applied.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-using.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 4
keywords: [CI ownership, CI ownership recommender, group profile, assignment recommendation, CMDB, ServiceNow Otto for CMDB, AI reasoning]
breadcrumb: [CI ownership agentic workflow, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Determining CI ownership

The CI ownership agentic workflow builds a profile of what each group in your organization owns. It then identifies configuration items with no owning group and proposes an owner for each one. A reviewer approves or rejects each proposal before it's applied.

**Important:**

Generative AI might produce inaccurate or incomplete information. Ownership proposals depend on the quality and consistency of your organization's existing CI data. Always review a proposal's confidence rating and reasoning before approving it.

Many organizations have configuration items with no value in an owning-group field, such as **managed\_by\_group**. Unowned CIs are harder to route during incident and change processes, and harder to hold accountable during audits. Tracing the right owner by hand doesn't scale once an organization has more than a handful of groups and CI classes.

**Note:** The CI ownership agentic workflow is part of the Feature Preview Program and is inactive by default. For steps to activate it, see [Activate the CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-ci-ownership.md).

## Key benefits

The workflow provides the following benefits:

-   Reduces manual tracing of group-to-CI ownership patterns.
-   Applies high-confidence proposals automatically, and queues lower-confidence proposals for a reviewer.
-   Explains its reasoning with a confidence rating for every proposal, so a reviewer can judge how much to trust it.
-   Is invoked directly from the ServiceNow Otto panel, or runs on its own schedule in the background.

## Workflow steps

The workflow runs in three stages:

-   **Step 1: Build group profiles**

    On a schedule, the workflow samples a set of CIs for each group that owns or could own CIs. It then consolidates the sample into a plain-language profile of what that group owns. A group's profile refreshes only after it ages past the configured refresh interval.

-   **Step 2: Infer ownership**

    Hourly, the workflow finds unowned, in-scope CIs and retrieves the most relevant group profiles for each one. It proposes an owning group and a confidence rating for each CI.

    Proposals with a high enough confidence rating are applied to the CI automatically. All other proposals are queued for review.

-   **Step 3: Review assignments**

    Queued proposals are grouped into an assignment recommendation per owning group. A reviewer approves or rejects an entire recommendation, or opens it and approves or rejects individual candidates. Approving writes the proposed owning group onto the CI. Rejecting leaves the CI unchanged.


## Invocation mode

Ask the CI ownership recommender for a link to CIs you can queue for ownership evaluation, or a summary of your queued items or open recommendations. Example trigger phrases include `Help me with missing CI owners` and `Review CI ownership recommendations`.

You can also queue CIs and review recommendations directly from their lists, without the agent. See [Determine the owner of a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md) for the full steps.

## Agent responses

The agent guides you through the same actions in a conversation, from the ServiceNow Otto panel. If the workflow isn't activated, it tells you to contact Support to enable it. Once activated, its first response depends on what it finds, in this order:

-   If open recommendations exist, it offers to review them.
-   If the jobs are inactive, it explains that and links to the job list. An admin can activate them from that link; anyone else is directed to their system administrator.
-   If the jobs are active and no recommendations exist yet, it offers to add CIs to the queue.

After its first response, and after each check you ask it to run, the agent offers the same three follow-up actions:

1.  Add CIs to the queue for generating ownership recommendations.
2.  Check the status of CIs you personally added to the queue.
3.  Review all open recommendations across the organization.

\[Omitted image "na-cmdb-ci-ownership-options.png"\] Alt text: The CI ownership recommender's chat response offering to add CIs to the queue, check the status of queued CIs, or review open recommendations.

For more information, see [Determine the owner of a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md).

For example, selecting **Review all open recommendations across the organization** returns the response as shown in the following image.

\[Omitted image "na-cmdb-ci-ownership-assignment-list.png"\] Alt text: The CI ownership recommender's chat response listing open recommendations by task number, candidate count, and confidence rating.

A recommendation whose candidates were already reviewed individually shows Manually Modified instead of a confidence rating.

To review individual candidates instead of a whole recommendation, enter `sn_cmdb_gen_ai_ci_ownership_candidate.list` in the navigation filter. Each candidate shows its proposed owning group, a confidence rating from Very Low to Very High, and the reasoning behind the proposal.

## Constraints and limitations

-   Maximum CIs evaluated per inference run: 1000, configurable by the **sn\_cmdb\_gen\_ai.ci\_ownership\_inference\_batch\_size** system property.
-   Maximum CIs sampled per group profile: 100 by default, configurable by the **sn\_cmdb\_gen\_ai.ci\_ownership\_sample\_size** system property.
-   Automatic approval is off by default. An admin must set a minimum confidence rating in the **sn\_cmdb\_gen\_ai.ci\_ownership\_auto\_accept\_confidence\_minimum\_rating** system property before any proposal is applied without review.

## Required role

The `sn_cmdb_editor` role is required to view or act on group profiles, candidates, and assignment recommendations.

**Related topics**  


[CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-c.md)

[Determine the owner of a CI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md)

[CI ownership agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-ref.md)

