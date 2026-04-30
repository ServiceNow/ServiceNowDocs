---
title: Analyzing your current infrastructure
description: Consider aspects of the current IT infrastructure and anticipate the consequences to prepare for the cloud migration. Decide on the migration scope: What IT resources need to migrate, in what capacity and how soon. In addition, you can use migration to optimize the use of IT resources. Analyze the resource use to identify redundant, underutilized or overutilized resources.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Planning the migration process, Using Cloud Migration Assessment in Configurable Workspace, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Analyzing your current infrastructure

Consider aspects of the current IT infrastructure and anticipate the consequences to prepare for the cloud migration. Decide on the migration scope: What IT resources need to migrate, in what capacity and how soon. In addition, you can use migration to optimize the use of IT resources. Analyze the resource use to identify redundant, underutilized or overutilized resources.

Use the following questions to decide on the approach and plan the migration process, including scope, timeframe and resources:

-   What does the current IT infrastructure consist of?
    -   How many servers are there?
    -   Are there any servers that can’t be migrated permanently or temporarily?
    -   How many IT resources are already in the cloud?
    -   What are the hardware requirements, for example CPU throughput, uptime, latency?
    -   What are the software requirements?
    -   Are all servers, applications, and services fully discovered? What are the consequences of migrating these resources and services? What are the potential pitfalls?
-   What teams might the migration affect?
    -   Are all the teams aware of the upcoming changes?
    -   Have all service owners been identified?
    -   Are there any services dependent on other teams' services?
-   What are the pros and cons of migration?
    -   What would be the cost of migration to different cloud providers?
    -   What cloud provider offers the best cost and value?
    -   Is it possible to use more than one provider based on the pricing models?
-   Are there opportunities for optimizing the current IT infrastructure prior to migration?

    There are ways to assess the resource usage. In environments deploying VMware, Cloud Migration Assessment can collect VMware statistics. Alternatively, you can deploy Cloud Cost Management that provides usage metrics.

    -   Are there any applications, servers, or services that are no longer in use? Is it possible to merge, remove, or retire such resources?
    -   Are there any services that are currently oversubscribed or overutilized \(approximately 90% of licenses used up\)?
    -   Are there any services that are currently undersubscribed or underutilized \(approximately 30% of licenses used up\)?
    -   Is it possible to balance and adjust the current use of resources?
    -   Is it possible to consolidate the number of services?
    -   Are there any servers or services that are using the end-of-life software and must be upgraded or replaced?

**Parent Topic:**[Planning the migration process](cloud-migration-planning.md)

**Previous topic:**[Planning the migration process](cloud-migration-planning.md)

**Next topic:**[Review your current infrastructure with Cloud Migration Assessment](../task/migration-review-infrastructure.md)

