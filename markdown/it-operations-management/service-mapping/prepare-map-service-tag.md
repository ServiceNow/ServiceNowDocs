---
title: Prepare for mapping application services based on tags
description: Analyze, review, and define tags in your organization for successful mapping.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Map application services using tags with classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Prepare for mapping application services based on tags

Analyze, review, and define tags in your organization for successful mapping.

## Before you begin

Role required: service\_mapping\_admin

## About this task

As a preparation for tag-based mapping, create tag categories that contain tags with similar use.

**Note:** Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map your application services. .

Define a tag-based service family and define tags that you want Service Mapping to use for mapping. Based on the tag definitions for the tag-based service family, Service Mapping creates service candidates - suggested service instances. You review the candidates and decide which ones you want to use to create the actual tag-based service instances. For details on the tag-based mapping process, see [Tag-based discovery in Service Mapping](../concept/tag-based-mapping.md).

CIs that have discovered tag values for the tag categories you selected become part of application services. Service Mapping creates a separate service candidate for each tag value combination. If you narrow the criteria down by defining the tag values in addition to tag categories, Service Mapping maps only CIs that have the matching values. CIs that have more than one tag assigned to them, can be part of multiple services. You may want to create a tag category for tags related to different types of environments, if your organization uses "production" and "staging" tag values. Tag-based mapping is not case-sensitive; same key names and key values spelled with upper and lower case are identified as the same.

**Note:** Service Mapping includes CIs that are part of CI relationships even if these CIs do not have tags assigned to them. For more information, see [Tag-based discovery in Service Mapping](../concept/tag-based-mapping.md).

## Procedure

1.  Analyze the tag usage in your organization and make a list of all tags and their purposes. Use the Key Value \[cmdb\_key\_value\] table to see the tags in the CMDB.

    Use Tag Governance to analyze and optimize tag application in your organization. See [Tag Governance](../../it-operations-management/reference/landing-page-tag-governance.md).

2.  If necessary, assign tags to CIs that you want to include in application services.

    Avoid creating very large application services containing more than 5000 CI relations. Such large services may cause performance issues.

3.  Create and define tag categories that you want Service Mapping to use for mapping service instances.

    For example, to map all service instances your organization uses in the production environment in the EMEA region, create the following tag categories: Applications, EMEA region, and Production.

    1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **CI Tag Categories**.
    2.  Select a **CI tag category** to modify or select **New**.
    3.  Define the tag category name, for example, **Environment**.
    4.  Under **CI tag keys**, double-click the row and type the tag key, for example **Env**.

        Since tag-based mapping is not case-sensitive, tag key variants using different capitalization, like **Env**, **env** or **ENV**, are also assigned to this same tag category.

        Repeat this step until you add all tag key variants that your organization uses for the same purpose, for example **Env** and **Environment**.

    **Note:** To see detailed examples of defining tag-based mapping criteria for service families, see [Example definitions for service families in tag-based mapping](../reference/examples-tag-based-criteria-service-families.md).

4.  Run Discovery to horizontally discover CIs. Discovery populates the CMDB with the CI data, including tags.

    If your ServiceNow instance uses domain separation and you have access to the global domain, log in to the relevant domain. The selected domain must be a domain without any child domains.


**Parent Topic:**[Map application services using tags with classic Service Mapping](map-service-tag.md)

