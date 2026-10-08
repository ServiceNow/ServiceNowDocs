---
title: Determine the owner of a CI
description: Queue CIs for ownership evaluation, then review the proposed assignments. Approve or reject each proposal individually or as a batch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [CI ownership, CI ownership recommender, assignment recommendation, approve, reject, CMDB]
breadcrumb: [CI ownership agentic workflow, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Determine the owner of a CI

Queue CIs for ownership evaluation, then review the proposed assignments. Approve or reject each proposal individually or as a batch.

## Before you begin

Activate the CI ownership recommender, as described in [Activate the CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-ci-ownership.md).

Role required: sn\_cmdb\_editor

## About this task

The CI ownership agentic workflow samples CIs owned by each group to build a profile of that group's ownership. It then evaluates unowned CIs against those profiles to propose an owner.

Proposals with a high enough confidence rating are applied automatically. All other proposals are grouped into an assignment recommendation for a reviewer to approve or reject.

## Procedure

-   Select the ServiceNow Otto icon \[Omitted image "otto-icon-white.svg"\] and, in the ServiceNow Otto panel, ask the CI ownership recommender for help with CI ownership.

    The following options appear:

    -   [Add CIs to the queue for generating ownership recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md).
    -   [Check the status of CIs you personally added to the queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md).
    -   [Review all open recommendations across the organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-use.md).
-   Add CIs to the queue for generating ownership recommendations.

    1.  Select **Add CIs to the queue for generating ownership recommendations**.

        The agent opens the Configuration Items list in the CI Ownership Inference Custom Request view, filtered to the CI classes configured for the workflow.

    2.  Select one or more CIs from the list, then select **Add to queue**.

        A message confirms that the selected CIs were added to the queue and will be processed with the next scheduled run of the inference job.

        **Note:** Queuing CIs manually is optional. The workflow also evaluates unowned CIs on its own schedule.

-   Check the status of CIs you personally added to the queue.

    1.  Select **Check the status of CIs you personally added to the queue**.

        The agent returns a summary of your queued runs, including when each run started and a count of CIs in each state.

-   Review all open recommendations across the organization.

    1.  Select **Review all open recommendations across the organization**.

    2.  On the CI Ownership Assignment Recommendations list, select one or more recommendations, then select **Approve** or **Reject**.

        Approving or rejecting a recommendation acts on every candidate it contains. Each candidate shows its proposed owning group, a confidence rating from Very Low to Very High, and the reasoning behind the proposal.

        The list refreshes so you can check whether any candidate ran into an error. Approving eventually writes the proposed owning group onto each approved CI and marks its candidate approved; this can take a few minutes to complete. Rejecting marks a candidate rejected without changing the CI.


**Related topics**  


[CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-c.md)

[Determining CI ownership](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-using.md)

[Activate the CI ownership agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-ci-ownership.md)

[CI ownership agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-ci-ownership-ref.md)

