---
title: Execute the scheduled jobs
description: Execute the scheduled jobs required for the main node relationships. After the scheduled jobs are executed, CSDM objects with their configured relationships are imported into Operational Resilience for reporting.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Gathering data aligned with the CSDM setup, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Execute the scheduled jobs

Execute the scheduled jobs required for the main node relationships. After the scheduled jobs are executed, CSDM objects with their configured relationships are imported into Operational Resilience for reporting.

## Before you begin

Role required: sn\_oper\_res.manager

Before executing the scheduled job, ensure that the following pre-requisites are met:

1.  Entity types and pillars have been defined and entities have been generated.
2.  Configuration item \(CI\) relationships have been created as required for the Main node configuration relationships.

Once all these pre-requisites are met, you can execute the scheduled job.

**Note:** All configurations with the source as **OpRes CMDB** run in parallel.

## About this task

**Note:**

The **Update CSDM and other dependencies** and **Calculate red flags for CSDM and dependencies** scheduled jobs create an entity hierarchy and all types of red flags. All CSDM and red flags are rolled up based on their entity hierarchy.

The scheduled jobs are configured to run according to the following schedule:

1.  The **Update CSDM and other dependencies** scheduled job updates CSDM and other dependencies. It is configured to run weekly at midnight local time.
2.  The **Calculate red flags for CSDM and dependencies** scheduled job calculates the red flags for the CSDM and its dependencies. It is configured to run daily at 3:00 AM local time.

Operational Resilience administrators can perform all the functions as the Operational Resilience managers. The Operational Resilience users cannot execute the scheduled job but they can verify the records in the entity and entity hierarchy tables.

Before running the scheduled job, verify that the relationships are set up for an object as shown in the following example.

![CSDM objects.](../image/csdm-objects-rel.png)

## Procedure

1.  Navigate to **All** &gt; **system definition** &gt; **Scheduled Jobs**.

2.  Choose the **Update CSDM and other dependencies** scheduled job.

    The illustration shows the steps executed in the script of the scheduled job.

    1.  When the script is run, it cleans all the records in the staging tables. Staging tables are used in Operational Resilience to save the red flags, which are displayed on the dashboard.
    2.  Next, it updates the CSDM dependencies by calling the relationship API.
    3.  As the final step, it runs the configurations in parallel to ensure that the scheduled job completes quickly and loads the data efficiently.
    ![Scheduled job.](../image/sch-job-csdm.png)

3.  Select **Execute Now**.

    After the scheduled job is executed, all CMDB objects are fetched into Operational Resilience.

4.  Verify that the Main node configuration, node relationship configuration, and node configuration results are displayed correctly.

5.  Verify that staging records are created according to entity hierarchies after running the scheduled job.

    Depending on the installed applications, the staging tables are created in Operational Resilience. For example, when the scheduled job is run, the following staging tables are created.

    -   sn\_oper\_res\_failed\_control
    -   sn\_oper\_res\_risk
    -   sn\_oper\_res\_bcm\_plan
    -   sn\_oper\_res\_vul\_profile
    -   sn\_oper\_res\_third\_party\_risk
    -   sn\_oper\_res\_task
    -   sn\_oper\_res\_change\_request
    -   sn\_oper\_res\_critical\_service\_outage
    -   sn\_oper\_res\_incident
    -   sn\_oper\_res\_issue
    The business views are mapped into the entity hierarchy. Red flags for the entities, such as Failed controls, High risks, Issues, Vulnerability response, are displayed in the reports on the landing page. For more information, see [Business services overview tab](../../grc-operational-res-ws/concept/bs-ov.md).


