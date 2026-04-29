---
title: Process Mining release notes
description: The ServiceNow Process Mining application enables analysts and process owners to view their business processes, analyze them, and make decisions that improve their processes. Process Mining was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Process Mining release notes

The ServiceNow® Process Mining application enables analysts and process owners to view their business processes, analyze them, and make decisions that improve their processes. Process Mining was enhanced and updated in the Australia release.

## Process Mining highlights for the Australia release

-   Use parallel processing for playbook data.
-   Benefit from the new use cases through the enhanced process step filter and rule-based findings.
-   Mine Agentic AI logs.
-   Easily identify your improvement opportunities through four new automated findings.
-   Take advantage of Process Mining and Task Mining integration.
-   Filter the data from the parent and child tables in the multidimensional projects.

See [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Parallel processing for playbook data introduced](https://www.servicenow.com/docs/access?context=export-to-playbook&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Analyze ServiceNow Playbooks, including their stages and individual activities using Process Mining. This capability enables Playbook authors and business process owners to do performance evaluations and optimize Playbooks.


-   **[Process Step filter \(Previously Transition filter\) &amp; Rule-based Findings enhanced](https://www.servicenow.com/docs/access?context=rule-based-builder&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Unlock new use cases and drive better process optimization outcomes through the enhanced process step filter and rule-based findings.

-   **[Intent and Activity analysis available with Now Assist](https://www.servicenow.com/docs/access?context=now-assist&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Efficiently summarize \(human\) agent tasks and their sequence in relation to problem types so you can pinpoint areas for improvement and take concrete actions to optimize your processes.

-   **[Mine Agentic AI logs](https://www.servicenow.com/docs/access?context=set-objectives&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Create a Process Mining project on Agentic AI data logs by selecting the designated source from a readily available template.

-   **[Integration with Task Mining](https://www.servicenow.com/docs/access?context=task-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Gain insights on the time the workstation users spend and how they accomplish tasks by analyzing their activities. Uncover inefficiencies, standardize best practices, and identify automation opportunities. You can create a Task Mining project from Opportunity details page and Analyst workbench of Process Mining.

-   **[New automated findings introduced](https://www.servicenow.com/docs/access?context=automated-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Use the following automated findings to identify improvement opportunities where records follow specific patterns:

    -   Extreme duration \(Node\): Identifies patterns where records stay in a step for a significantly longer duration than usual
    -   High touchpoints \(Node\): Identifies patterns where a group of records in a step gets updated more often compared to another group to progress to any next step.
    -   Extreme touchpoints \(Node\): Identifies patterns where a step requires unusually large number of record updates than the normal range to progress to any next step.
    -   Slow duration \(Node\): Identifies patterns where a group of records stays longer in a step than the average duration of another group.
-   **[Multidimensional projects filters](https://www.servicenow.com/docs/access?context=filter-project&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Make analysis easier by filtering multidimensional projects based on child breakdowns and variants as a substitute for filtering on child attributes.

-   **[Evaluation project for security operations available](https://www.servicenow.com/docs/access?context=evaluation-security&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Try out an evaluation project for security incidents, which can provide improvement opportunities based on assignment group changes, time analysis, priority escalations, and automated indicators such as repeated states and assignment groups. You can target a maximum of 3.6K records that have been closed in the last seven days.

-   **[Introduced views to the Platform Analytics workspace for Process Mining](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Display specific activity definitions within the Platform Analytics workspace for Process Mining using views. When working with graphs that contain multiple activity definitions, views help filter the map to show only activities relevant to the problem being analyzed.

-   **[Multidimensional maps are supported on the Opportunity details page and Platform Analytics components](https://www.servicenow.com/docs/access?context=opportunity-details&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Quickly analyze process maps with multiple tables through multidimensional maps on the Opportunity details page and Platform Analytics component of Process Mining.


## Changed in this release

-   **[Automated finding names updated](https://www.servicenow.com/docs/access?context=automated-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    The following automated finding names have been updated to include "Transition" in the name:

    -   Slow duration \(Transition\)
    -   Extreme duration \(Transition\)
-   **[Role names changed](https://www.servicenow.com/docs/access?context=components-installed&version=australia&pubname=australia-now-intelligence&section=po-roles&ft:locale=en-US)**

    Role names in Process Mining that previously included "optimization" have been updated to use the term "mining" instead. For example, the sn\_process\_optimization\_admin role has been renamed sn\_process\_mining\_admin.


## Removed in this release

You no longer require the now.assist.creator role to access Now Assist features in the Creator Pro Plus package. However, you must enable the relevant Process Mining skill, which serves as the necessary prerequisite. Additionally, you should have appropriate access to the project.

## Deprecated features

Automation Discovery is deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in the Australia release.

## Activation information

Process Mining is available by default. For details, see [Activating Process Mining](https://www.servicenow.com/docs/access?context=activating-process-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.

-   **[Task Mining](https://www.servicenow.com/docs/access?context=task-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Task Mining enables process owners to collect and analyze workstation activities to understand how tasks are performed, identify inefficiencies, and make data-driven decisions.


**Parent Topic:**[Platform Analytics release notes](../analytics-intelligence-reporting/analytics-intel-report-rn-landing.md)

