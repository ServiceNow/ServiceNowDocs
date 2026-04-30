---
title: Problem Management use case
description: The Problem Management use case is described in this section.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Applying CSDM guidelines to Problem Management, Configuring Problem Management, Problem Management, IT Service Management]
---

# Problem Management use case

The Problem Management use case is described in this section.

Problem Management is used to prevent problems and the occurrence of resulting incidents. It also aims at eliminating recurring incidents and minimizing the impact of incidents that cannot be prevented. With Problem Management, you can capture information on affected configuration items \(CIs\), with type as asset, in a problem to keep a record of the updated, repaired, swapped, or retired configuration items. By keeping track of the assets, you can identify the location of the assets, their usage and when the assets were changed. Using Problem Management, you to monitor and manage the assets in your company using a systematic approach.

If a configuration item \(CI\) has resulted in a problem, use the dependency view to identify other configuration items \(CIs\) affected by the CI that caused the problem. You can then associate affected configuration items \(CIs\) with a problem record to find out how the problem affects other CIs with dependent relationships.

## Key features of the Problem Management use case

The CMDB, when used by the CSDM framework, provides value to Problem Management in the following ways:

-   Understand the impact of the problem on services and service offerings.​
-   Dynamically route problems.
-   Identify one or more impacted services to address the problem.​

![CSDM data elements available for use by Problem Management.](../image/pm-use-case-csdm4.0.png)

The CSDM data elements used in Problem Management are:

1.  Subscription: Related lists on service offerings that identify who has access to the offering and thus might be impacted in an outage. A problem can identify impact using the subscribed by tables. The related lists are as follows:
    -   Service Subscriptions by Company \[service\_subscribe\_company\]
    -   Service Subscriptions by Department \[service\_subscribe\_department\]
    -   Service Subscriptions by Group \[service\_subscribe\_sys\_user\_grp\]
    -   Service Subscriptions by Location \[service\_subscribe\_location\]
    -   Service Subscriptions by User \[service\_subscribe\_sys\_user\]
2.  Business service offering might be used by problems to provide the business approver based on approval\_group and business\_criticality. A business service may have multiple offerings, each with a different criticality.
3.  Technical service offerings might be used by problems to provide the technical approver approval\_group and technical assignment group on the attribute assignment\_group.
4.  Service instance may be used to provide prod and non-prod \(DEV, QA, UAT, and so on\) environments. Non-prod environments may be filtered out if desired. The legacy **used\_for** attribute maps to the **environment** attribute. You should use the **environment** attribute.

    **Note:** Some service offerings may identify the environment of the offering as well.


## Results of the Problem Management use case

The CSDM framework provides Problem Management context for problems on what CIs may be involved.

To determine the impact and root cause, compete the following steps:

1.  Populate the **Configuration Item** attribute on the Problem form, configuration\_item, with the CI item or service affected.
2.  \(Optional\) Use the Service and Service Offering attributes on the Problem form to help narrow down the list of configuration items to choose from. This feature is not available with the base system and needs additional configuration.
3.  \(Optional\) Use the Affected CI related list to identify the CIs that may have caused the problem.

**Parent Topic:**[Applying CSDM guidelines to Problem Management](pm-use-case-product-view.md)

