---
title: Sample end-to-end workflow for business services
description: Configure an end-to-end workflow for the business service to fetch the CSDM dependencies and red flags data to Operational Resilience. You must ensure that entities are generated and associated with pillars, and that the Main node configurations are set up before fetching the required data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/configure-end-to-end-wf-bs.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Sample end-to-end workflow for business services

Configure an end-to-end workflow for the business service to fetch the CSDM dependencies and red flags data to Operational Resilience. You must ensure that entities are generated and associated with pillars, and that the Main node configurations are set up before fetching the required data.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

For the configuration sequence and instructions in Operational Resilience, see [Configuring Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-operational-resilience.md).

For instructions on creating the Main node configuration records, see [Configure the Main node configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/set-up-main-node.md).

## Procedure

1.  Download the Operational Resilience application in your instance.

    For instructions on downloading the Operational Resilience application, see [Install Operational Resilience application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/download-opres.md).

2.  Ensure that you have set up the pillars, entity types, entity filters and entities are generated.

    Refer to the configuration instructions on the [Configuring Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-operational-resilience.md) page.

3.  Navigate to **Operational Resilience Workspace** &gt; **List** &gt; **Business service** and select the business service.

    You can select a business service, for example, BS1-VM as shown in the illustration.

    \[Omitted image "business-service-new.png"\] Alt text: Business service.

4.  To add the business service to Operational Resilience reporting, select the service from the list and select **Add to OpRes reporting**.

    The selected service is added to Operational Resilience reporting.

5.  Verify that the entity is created for the business service, it is listed in the Business Services entity type on the Entity types page, and it is set to active on that page.

    You can verify that the value of the Active column for the Business Services is set to **True**. Verify that the entity is listed in the **Entities** tab and it is marked as Active in the **Details** tab.\[Omitted image "bs-sample-ent-ty-pg.png"\] Alt text: Business Services.\[Omitted image "bs-sample-ent-listed.png"\] Alt text: Entity listed.

    **Note:** The following example illustrates how to use entity filters to generate entities. However, for actual entity creation, you should run the **GRC Profile Generation** scheduled job rather than using entity filters.

    For reference, the **GRC Profile Generation** job details are shown.

    \[Omitted image "profile-gen-sch-job.png"\] Alt text: GRC Profile Generation.

    1.  In the **Entity Filters** tab, verify the filter condition for the business service that you want to include and fetch it in Operational Resilience.

    2.  Use either **Build your own conditions** or **Select from predefined queries** option in the **Entity filter type** field and select **Save**.

        You can build your own conditions or use predefined queries as shown in the examples.

        \[Omitted image "ent-filter-build-condition.png"\] Alt text: Condition.\[Omitted image "ent-filter-predefined-query.png"\] Alt text: Predefined query.

    Once the filter condition or query is used, the entities are generated for the selected business service.

6.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configurations** and select the Main node configuration.

    The following example shows the Main node configurations that are provided with the base system for the OpRes CMDB source.\[Omitted image "main-node-configs.png"\] Alt text: Main node configurations.

7.  To fetch all these relationships into the entity hierarchies in Operational Resilience, execute the **Update CSDM and other dependencies** scheduled job.

    The following illustration shows all scheduled jobs.

    \[Omitted image "scheduled-jobs.png"\] Alt text: Scheduled jobs.

    The `UpdateCSDMDependencies` function in the **Update CSDM and other dependencies** scheduled job fetches all dependencies of the business service into an entity hierarchy, as part of the Opres with CSDM header Main node configuration.

    \[Omitted image "csdm-sch-job.png"\] Alt text: Update CSDM.

    When the scheduled job is executed, it creates an entity hierarchy for preconfigured relationships in the Main node configurations.

8.  Verify that the corresponding entities are generated in the business service record.

    \[Omitted image "bs-sample-entities.png"\] Alt text: Entities.

9.  In the business service record, select **Go to entities** and select the **Hierarchy** tab to view how the entities are inherited from each other.

    Based on the node relationship configurations set up in each Main node configuration, the downstream dependencies are pulled from CSDM or dependency assessment in the BIA.\[Omitted image "hierarchy.png"\] Alt text: Hierarchy.

10. To calculate the red flags, execute the **Calculate red flags for CSDM and dependencies** scheduled job.

    When the **Calculate red flags for CSDM and dependencies** scheduled job is triggered, it cleans up all the staging records and then it starts calculating the red flags.

    \[Omitted image "bs-red-flag-data.png"\] Alt text: Red flags.

    The red flags data, including issues, high risks, failed controls, change requests, tasks, incidents, and outages, are listed for each dependency and also in the separate Red flags tabs in the business service record.

11. To view dependencies of the business service from the CMDB, select the **Open dependency view** option in the business service record.

    The dependency view shows how the relationships of the selected business service are configured in the CMDB.

    \[Omitted image "bs1-vm-dependency-view.png"\] Alt text: Dependency view.

12. To access a comprehensive overview of the business service record, select the **360º view** option.

    The 360º view of the business service record is displayed.

    \[Omitted image "bs-360-view.png"\] Alt text: 360-degree view.


