---
title: Use tags to populate application services
description: Use tags that help categorize and organize configuration items \(CIs\) in your organization to populate an service instance. Tag-based mapping doesn't require configuring credentials or providing users with elevated rights. Tag-based population method requires the Service Mapping feature of ITOM Visibility.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create an application service, Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use tags to populate application services

Use tags that help categorize and organize configuration items \(CIs\) in your organization to populate an service instance. Tag-based mapping doesn't require configuring credentials or providing users with elevated rights. Tag-based population method requires the Service Mapping feature of ITOM Visibility.

## Before you begin

1.  Tags is one of several methods for populating an application service with CIs. Choosing a method for populating an application service, is only one step of the generic procedure for creating an application service. Ensure that you have completed the initial steps as described in [Create an application service](../../service-mapping/task/create-it-services.md). The procedure described here is incomplete by itself as it complements that generic procedure.

2.  Analyze the tag usage in your organization and make a list of all tags and their purposes. Use the Key Value \[cmdb\_key\_value\] table to see the tags in the CMDB.
3.  If necessary, assign tags to CIs that you want to include in an service instance.

Role required: sm\_admin

## About this task

A tag is a label that consists of a key-value pair. Your organization may use tags to categorize its assets, to enhance query and reporting capabilities. Discovery and Cloud Provisioning and Governance can discover tags used by all major cloud providers and container ecosystems. Once the tags are discovered, Service Mapping can create service instances based on these tags. For example, you can use tags to map all application services your organization uses in the production environment in the Europe, the Middle East and Africa \(EMEA\) region.

If you have [configured tag-based service families and tag categories](https://www.servicenow.com/docs/access?context=tag-based-mapping&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), you can use these tag definitions for populating an application service. Part of defining a tag-based service family is defining a tag category, which contains tag keys. If necessary, you can also define tag values to narrow the criteria used for populating application services. Based on the tag definitions for the tag-based service family, Service Mapping creates service candidates - suggested application services. When you use the tag-based service families to populate an application service, you must select the relevant service candidate.

Alternatively, you can define tag keys and their values while choosing the tag-based population method for a new application service. Define up to three tag keys and tag values for the population criteria. CIs that have discovered tag keys and tag values, become part of an service instance.

For information about the different types of application services and the different methods you can use to populate application services, including using tags, see [Application services](../concept/application-services.md).

**Note:** Service Mapping includes CIs that are part of CI relationships even if these CIs do not have tags assigned to them. For more information, see [Tag-based discovery in Service Mapping](https://www.servicenow.com/docs/access?context=tag-based-mapping&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Procedure

1.  From the **Service Population Method** list in the Choose a Method window, select **Tags**.

2.  To define new tag criteria, perform the following steps:

    1.  Select **Use a list of tags**.

    2.  Enter the tag key and its respective tag value.

        Matching tag keys that exist in the system, appear in the auto-fill options.

        **Important:** Tag-based mapping is not case-sensitive; same key names and key values spelled with upper and lower case are identified as the same.

    3.  Click the plus icon and add another tag key and tag value.

    4.  Click **Preview Result** to see the list of CIs that match the defined criteria.

        **Note:** If necessary, refine the tag definitions. You can add no more than three tag key-value pairs for one application service.

3.  To use tag definitions from a preconfigured tag-based service family, perform the following steps:

    1.  Select **Use a candidate from a tag-based service family**.

    2.  To see the tag definitions for this tag-based service family, select the **Preview** button.

    3.  From the **Tag-Based Service Family** list, select the relevant family.

    4.  Review the tag categories and values assigned to the service family.

    5.  From the **Service Candidate** list, select the relevant candidate.

    6.  To review the service candidate form, select the **Preview** button .

4.  Add free-text comment that may provide useful information for handling this application service later.

5.  Click **Save**.


## What to do next

Complete the generic procedure [Create an application service](../../service-mapping/task/create-it-services.md).

