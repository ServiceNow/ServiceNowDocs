---
title: Evidence request workflow and users
description: Evidence request helps customers to electronically request the information that they need from the first and second line of defense. The individuals being audited can then immediately upload their documents to the system, significantly reducing manual processing time.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit Evidence Request, Audit Management Overview, Audit Management, Governance, Risk, and Compliance]
---

# Evidence request workflow and users

Evidence request helps customers to electronically request the information that they need from the first and second line of defense. The individuals being audited can then immediately upload their documents to the system, significantly reducing manual processing time.

The evidence request workflow is as follows:

1.  An audit user with the sn\_audit.user role requests evidence and assigns the request to another user. This requester can either request the evidence for themselves or raise a request on behalf of another audit user or GRC user. If the requester determines that an evidence task has been created erroneously, then the requester can cancel that particular evidence task. The ability to cancel the evidence request is available when the request is in **Draft** state. A requester can cancel the evidence request tasks any time until the tasks reach the **Review** state.
2.  After you create an evidence request, you must create evidence collection records and then the requester must request evidence. Evidence Collection records contain the evidence collection instructions, assigned to, and assignment group. On clicking **Request Evidence**, evidence request tasks are generated and they are assigned to a group or user.
3.  The assignee then receives an email with the link to provide the requested evidence.

    **Note:** If the requester changes the assignee after requesting evidence, then the original assignee can no longer view the request. Only the person who is assigned the request can view the request. This feature ensures confidentiality.

4.  The assignee can either attach the requested evidence or provide a URL or location that contains the required evidence.
5.  The assignee can also add an approver for verifying and approving the evidence. Adding approvers is necessary if the evidence is sensitive and confidential in nature.
6.  The approver can then review the evidence and either approve it, request revision, or request further details about the evidence.
7.  If the approver approves the evidence, the requester receives the evidence and can process it further.
8.  The requester can then review the evidence and do one of the following:
    -   accept the evidence.
    -   request for its review.
    -   request further details about the evidence.
    -   cancel the evidence request if it is not required anymore.
    -   delete the request.
9.  If the requester accepts all the evidence tasks, the request is closed.

The evidence request workflow is shown in the following figure:![Workflow of evidence request](../image/evidence-request-workflow.png)

The following table describes the roles and their responsibilities during the evidence request workflow:

<table id="table_sqs_lmf_nmb"><thead><tr><th>

User

</th><th>

Responsibilities

</th><th>

Requirements

</th></tr></thead><tbody><tr><td>

Internal auditor

</td><td>

-   Perform audit testing.
-   Request audit testing.
-   Review all audit findings and the evidence collected.

</td><td>

-   Visibility into compliance and risk activity.
-   A job queue \(pending, current, upcoming\) to plan their team efforts.
-   Track and monitor audit findings.
-   Track and monitor audit activities.

</td></tr><tr><td>

Compliance manager, Audit manager

</td><td>

-   Can request evidence.
-   Request compliance test evidence.
-   Review all findings and evidence collected.

</td><td>

-   Visibility into compliance activities.
-   A job queue \(pending, current, upcoming\) to plan their team efforts.
-   Track and monitor compliance findings.

</td></tr><tr><td>

Compliance user, Control owner

</td><td>

-   Ensure that the controls are implemented.
-   Attest to the controls.
-   Test the controls.
-   Provide audit evidence requested by the auditor.

</td><td>

-   A job queue to direct their day-to-day activities.
-   Track the time spent and performance of activities and tasks they own.
-   Ensures the task they own and additional request from the auditor is fulfilled.

</td></tr></tbody>
</table>