---
title: Sample end-to-end workflow for services
description: Configure an end-to-end workflow for the service to fetch the CSDM dependencies and red flags data to Operational Resilience. You must ensure that entities are generated and associated with pillars, and that the Main node configurations are set up before fetching the required data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Sample end-to-end workflow for services

Configure an end-to-end workflow for the service to fetch the CSDM dependencies and red flags data to Operational Resilience. You must ensure that entities are generated and associated with pillars, and that the Main node configurations are set up before fetching the required data.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

For the configuration sequence and instructions in Operational Resilience, see [Configuring Operational Resilience](../concept/configure-operational-resilience.md).

For instructions on creating the Main node configuration records, see [Configure the Main node configurations](set-up-main-node.md).

## Procedure

1.  Download the Operational Resilience application in your instance.

    For instructions on downloading the Operational Resilience application, see [Install Operational Resilience application](download-opres.md).

2.  Ensure that you have set up the pillars, entity types, entity filters and entities are generated.

    Refer to the configuration instructions on the [Configuring Operational Resilience](../concept/configure-operational-resilience.md) page.

3.  Navigate to **Operational Resilience Workspace** &gt; **List** &gt; **Service** and select the service.

    You can select a service record as shown in the illustration.

    ![Service record.](../image/service-record.png)

4.  To add the service to Operational Resilience reporting, select the service from the list and select **Add to OpRes reporting**.

    The selected service is added to Operational Resilience reporting.

5.  Verify that the entity is created for the service and it is listed in the Services \(OR\) entity type in the Entity types page.

    ![Entity type.](../image/s-sam-ent-types.png)

    Verify that the entity is listed in the **Entities** tab and it is marked as Active in the **Details** tab.

    ![Entity.](../image/s-sam-ent.png)

    **Note:** The following example illustrates how to use entity filters to generate entities. However, for actual entity creation, you should run the **GRC Profile Generation** scheduled job rather than using entity filters.

    For reference, the **GRC Profile Generation** job details are shown.

    ![GRC Profile Generation.](../image/profile-gen-sch-job.png)

    1.  In the **Entity Filters** tab, verify the filter condition for the service that you want to include and fetch it in Operational Resilience.

    2.  Use either **Build your own conditions** or **Select from predefined queries** option in the Entity filter type and select **Save**.

        Entities are generated for the selected service.

6.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configurations** and select the Main node configuration.

7.  To fetch all these relationships into the entity hierarchies in Operational Resilience, execute the **Update CSDM and other dependencies** scheduled job.

    The following illustration shows all scheduled jobs and their set schedules.

    ![Scheduled jobs.](../image/scheduled-jobs.png)

    The `UpdateCSDMDependencies` function in the **Update CSDM and other dependencies** scheduled job fetches all dependencies of the business service into an entity hierarchy, as part of the Opres with CSDM header Main node configuration.

    When the scheduled job is executed, it creates an entity hierarchy for preconfigured relationships in the Main node configurations.

8.  To calculate the red flags, execute the **Calculate red flags for CSDM and dependencies** scheduled job.

    Red flags, including issues, high risks, failed controls, change requests, tasks, incidents, and outages, are updated in the business service record.

9.  Verify that the corresponding entities are generated in the service record.

10. In the service record, select **Go to entities** and select the **Hierarchy** tab to view how the entities are inherited from each other.

    Based on the node relationship configurations set up in each Main node configuration, the downstream dependencies are pulled from the CSDM or dependency assessment in the BIA.

11. To view the dependencies of the service, select the **Open dependency view** option.

12. To access a comprehensive overview of the service record, select the **360º view** option.


