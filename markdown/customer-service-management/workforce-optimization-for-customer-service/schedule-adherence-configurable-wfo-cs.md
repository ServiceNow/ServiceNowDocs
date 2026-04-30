---
title: Schedule Adherence in Workforce Optimization for Customer Service
description: You can use schedule adherence to monitor whether your team members are adhering and conforming to the schedules and to improve the operational efficiency of your organization.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Workforce Optimization for Customer Service, Customer Service Management]
---

# Schedule Adherence in Workforce Optimization for Customer Service

You can use schedule adherence to monitor whether your team members are adhering and conforming to the schedules and to improve the operational efficiency of your organization.

Clock-in and clock-out events are generated as agents change their availability status. The time between the clock-in and clock out events are aggregated to create schedule adherence and conformance reports.

Adherence measures how closely agents follow their schedule to complete their assigned work. Conformance measures the agents’ total time at work compared to the total scheduled time period, regardless of adherence.

Schedule adherence helps your organization to do the following actions:

-   Measure whether the effort spent on [demand forecasting](explore-demand-forecast-configurable-wfo-cs.md#) and scheduling team members is used in an optimal manner.
-   Plan for more effective staffing needs in the future based on your insights into the historical use of agent resources.
-   Discover coaching opportunities for your agents when there are gaps in their adherence. For more information, see [Coaching in Workforce Optimization for Customer Service](coaching-configurable-wfo-cs.md#).

As a manager, you can do the following actions:

-   Access the schedule of all of your teams from one location and gain insights on whether your team is complying with published schedules.
-   Increase your team's performance by setting expected adherence targets.
-   View the time attendance of your agents by looking at such details as clock-in and clock-out times.
-   Analyze the historical time attendance of your team members.
-   View planned versus actual historical data for your team and individual agents.
-   Modify the clock-in and clock-out times of your agents.

As an administrator, you can set the threshold percentages and change the formulas for calculating schedule adherence and conformance.

## Schedule Adherence for Customer Service in action

Watch this short video to understand how managers and agents use Schedule Adherence in Workforce Optimization for Customer Service

Schedule Adherence for Customer Service![Schedule Adherence for Customer Service]()

Consider the following steps to determine the schedule adherence and conformance:

1.  The administrator sets the **Agent Time Work Event Trigger** business rule as active to record the clock-in and clock-out times of customer service agents.
2.  An agent works for the Customer Service operations team and reports to a manager. Let's assume this scenario is a typical work day​:
    1.  The agent logs in to CSM Agent Workspace​.
    2.  The agent changes the presence status to **Available** and starts work. The clock-in event gets generated.
    3.  The agent changes the presence status to **Break** and goes for lunch. The clock-out event gets generated.
    4.  When the agent comes back from lunch and answers ​a phone call, the presence state becomes **Busy** and the clock-in event gets generated.
    5.  The agent then logs out from CSM ​Agent Workspace or changes the presence status to **Offline**​. The clock-out event gets generated.
    6.  At the end-of-the-day, the agent's time worked summary is generated with key performance indicators \(KPIs\), such as Start Time, End Time, Planned Work, Time Not Worked, Available Non Planned Time, Time Worked, and Adherence%, Conformance %​.
3.  The agent's manager logs in to Manager Workspace to view the agent's time worked in the **Team Calendar**. The manager can also view the agent's actual time worked and working pattern for all historical days. If required, the manager can coach the agent to a desired performance that fits in with the team culture.

**Related topics**  


[Configure properties for schedule adherence and conformance](setup-scheduling-configurable-wfo-cs.md#)

[Monitor schedule adherence of your agents](../task/view-schedule-adherence-configurable-wfo.md)

[Analyze adherence and conformance from the time worked summary](../task/analyze-time-worked-summary-configurable-wfo-cs.md)

