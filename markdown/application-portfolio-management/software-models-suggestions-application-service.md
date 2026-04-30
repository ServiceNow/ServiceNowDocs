---
title: Suggestions to relate technology models to an application service
description: Use the software models that the suggestions engine identifies and relate them to your application service, instead of manually searching and mapping them.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Management of business applications, Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Suggestions to relate technology models to an application service

Use the software models that the suggestions engine identifies and relate them to your application service, instead of manually searching and mapping them.

The business applications used in your organization consume application services to fulfill a business capability for the business enterprise.

-   Various application instances of a business application run on hardware that require necessary software models to provide the business capability.
-   A cmdb relationship establishes an association between the business application and the application service. But then, an application owner is required to manually associate an application service to a software model.
-   For the association to be precise, your software model data for the business application must be maintained up-to-the-minute.

To avoid manual intervention and prevent association to a software model that has non-current data, the software model suggestion engine suggests possible software models to an application service. You can use the suggested software models, select those models that are appropriate, and associate them to your application services. This suggestion helps you to configure and maintain software model data for your business applications.

## Working model of the software model suggestions engine

The software model suggestions engine:

-   Scans hardware configuration items consumed by Application Services. A CMDB API retrieves all hardware CIs for an application service, and a Service Mapping API retrieves the hardware CIs for application service.
-   Retrieves the new software models installed on the hardware since the last run of the scheduled job.
-   Populates the Retrieved Software Models \[sn\_apm\_service\_software\_model\_suggestion\] table with the discovered software models.
-   Evaluates and compares the current software model suggestions status with the previous extracted suggestion results from the last run in the Technology Models Retrieval Logs \[sn\_apm\_suggestion\_engine\_run\_log\] association table.

    The Technology Models Retrieval Logs \[sn\_apm\_suggestion\_engine\_run\_log\] table also stores the count of hardware models on which the application service is running.

-   Updates status accordingly as **New**, **Associated**, **Ignored**, or **Deleted**.

**Related topics**  


[Associate suggested technology models to an application service](../task/associate-application-service-software-models.md)

