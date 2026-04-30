---
title: Exploring Problem Management
description: Problem Management supports the ITIL process used to find and fix the root cause of issues that result in incidents. You can record problems, associate incidents, and assign them to the appropriate groups. You can document and communicate known errors and initiate actions to resolve the situation.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Problem Management, IT Service Management]
---

# Exploring Problem Management

Problem Management supports the ITIL process used to find and fix the root cause of issues that result in incidents. You can record problems, associate incidents, and assign them to the appropriate groups. You can document and communicate known errors and initiate actions to resolve the situation.

Problem Management is responsible for managing the life cycle of all problems and preventing problems and resulting incidents from happening. It also aims to eliminate recurring incidents and minimize the impact of incidents that can’t be prevented. Resolving a problem includes the activities required to diagnose the root cause of incidents and determine the resolution for the problem. Problem resolution and elimination of the root cause often calls for applying a change to the configuration item in the existing IT environment.

Problem Management also maintains information about problems and the appropriate workarounds and resolutions, enabling an organization to reduce the number and impact of incidents over time. Problem Management interfaces with Knowledge Management, which is used to document known error articles thoroughly for future reference.

## Problem Management workflow

The Problem Management workflow includes the following:

1.  Problem Creation: You can create a problem to identify and permanently fix the underlying root cause when:
    -   You've resolved a major incident.
    -   You have recurring incidents.
2.  Assign the problem: You can now assign the problem to be assessed.
3.  Assess the problem: You can now assess the problem:
    -   Find and relate any additional incidents that the problem represents.
    -   If the problem was created from an incident, it has inherited fields from the incident that may not provide a specific description of the issue. In this case, update the **Problem Statement** and other fields to specifically describe this issue to help the team performing the root cause analysis during the later stages.
    -   Do any of the following:
        -   Confirm that you plan to work on this problem. This confirmation moves the problem to the Root Cause Analysis state.
        -   Mark this problem as a duplicate of an existing problem to close the problem.
        -   Cancel this problem if it's not a valid problem. Canceling it closes the problem.
4.  Analyze the root cause of the problem:
    -   If you're the subject matter expert, analyze the problem to uncover the root cause and identify a fix.
    -   If you're not the subject matter expert, create a Root Cause Analysis Problem task to assign to the relevant team. Coordinate with that team as they analyze and uncover the root cause and fix.
    -   If there's no permanent fix for the problem, or you don't have the sufficient budget to fix the problem at this time, accept the risk that it can't be fixed at this time. The problem enters the Closed state. It's a good idea to review risk-accepted problems periodically.
5.  Communicate the outcome of the problem:
    -   After you identify the fix or workaround of the problem, update the workaround or fix for the problem. Communicate updates to the related incidents.
    -   If the problem is a known error, create a known error article that is primarily available to help others find information and deflect additional incidents. The known error article can also be referred to by agents who are facing similar problems and incidents.
6.  Fix the underlying root cause if possible. If you can fix the root cause, create a change request and assign it to the relevant team. When the change request is completed, resolve the problem. If no new incidents come in, close the problem.
7.  Reanalyze the problem if it resurfaces. If you're the problem manager and you're not satisfied with the analysis after resolving or closing the problem, or the problem resurfaces, you can decide to reanalyze the problem. The problem is reopened and the state is changed to  Root Cause Analysis.

## Problem Management benefits

<table id="table_vtm_tf3_nxb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Create a problem to identify the root cause of the incident.

</td><td>

[Create a problem](../task/create-a-problem-v2.md)

</td><td>

Agent and Problem write users

</td></tr><tr><td>

Add multiple incidents to a problem to avoid creating multiple problems for incidents that have the same issue.

</td><td>

[Add multiple incidents to a problem](../task/add-multiple-incidents-to-problem.md)

</td><td>

Agent

</td></tr><tr><td>

Create a problem task to initiate the root cause analysis.

</td><td>

[Create a problem task](../task/create-problem-task.md)

</td><td>

Agent, Problem write users, and Problem task analyst

</td></tr><tr><td>

Document and communicate a workaround to restore service failures and lessen the impact of a problem that an actual resolution is not yet available.

</td><td>

[Communicate workaround for Problem](../task/communicate-workaround.md#)

</td><td>

Problem Coordinator

</td></tr><tr><td>

Create known error articles as reference material.

</td><td>

[Create a known error article](../task/create-known-error-from-problem.md)

</td><td>

Problem Coordinator

</td></tr><tr><td>

Implement a resolution to a problem by applying a standard change procedure and testing it to confirm service recovery. 

</td><td>

[Create change request from a problem](../task/fix-a-change.md)

</td><td>

Problem Coordinator

</td></tr><tr><td>

Resolve the issue and add detailed notes for the resolution for future reference.

</td><td>

[Resolve and complete a problem](../task/resolve-and-complete-problem.md)

</td><td>

Problem Coordinator

</td></tr></tbody>
</table>-   **[Problem Management process](c_ProblemManagementProcess.md)**  
Within the platform, problems are handled using the task record system. Each problem is generated as a task record through various means, and is populated with the pertinent information. These tasks are assigned to Problem Management team members to resolve and then close.
-   **[Problem Management models](problem-mgmt-models.md)**  
You can use Problem Management models to tailor processes for specific use cases.

**Parent Topic:**[Problem Management](c_ProblemManagement.md)

