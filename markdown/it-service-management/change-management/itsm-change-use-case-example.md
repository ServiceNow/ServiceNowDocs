---
title: Change Management use case
description: For ITSM, specifically incident and change, identifying the location of critical data can help reduce mean time to resolve incidents and eliminate outages caused by change.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Applying CSDM guidelines to Change Management, Configure, Change Management, IT Service Management]
---

# Change Management use case

For ITSM, specifically incident and change, identifying the location of critical data can help reduce mean time to resolve incidents and eliminate outages caused by change.

## Key features of the Change Management use case

Applying the CSDM framework provides value to Change Management in the following ways:

-   Enables users to understand the impact of a change on services and service offerings.
-   Changes are dynamically routed.
-   Change Management identifies and notifies all affected services to support the approval decision.

![Data elements available for use by Change Management.](../image/change-mgmt-elements-use-case.png)

1.  Subscription: Related lists on service offerings that identify who has access to the offering and thus may be impacted in an outage. An incident or change can identify impact using the subscribed by tables. The related lists are as follows:
    -   Service Subscriptions by Company \[service\_subscribe\_company\]
    -   Service Subscriptions by Department \[service\_subscribe\_department\]
    -   Service Subscriptions by Group \[service\_subscribe\_sys\_user\_grp\]
    -   Service Subscriptions by Location \[service\_subscribe\_location\]
    -   Service Subscriptions by User \[service\_subscribe\_sys\_user\]
2.  Business service offering may be used to provide the business approver based on approval\_group and business\_criticality. A business service may have multiple offerings, each with a different criticality.
3.  Technical service offering may be used to provide the technical approver approval\_group and technical assignment group on the attribute assignment\_group. May be used by change for routing of change and change tasks. May be synchronized onto the CI’s that the offerings manage thus reducing the manual overhead of maintaining manual data on thousands/millions of CI’s.
4.  Application service may be used to provide prod and non-prod \(DEV, QA, UAT, etc.\) environments. Non-prod environments may be filtered out if desired. The legacy **used\_for** attribute maps to the **environment** attribute. You should use the **environment** attribute.

    **Note:** Some service offerings may identify the **environment** of the offering as well.


## Results of the Change Management use case

The CSDM framework provides context for the changes. The context includes the CIs involved in the change and the services affected.

Use the Change Request form to see the impact of the change. Complete the following steps:

1.  Populate the Configuration Item attribute \[configuration\_item\] with the target CI for the change activity. You can then use this CI to identify details for change routing. For example, you can use the CI data, such as “Assignment Group” or "Approval Group," and provide information about the service impact by using dependency relationships.
2.  Populate the Impacted Services related list \[task\_cmdb\_ci\_service\] with the services that are related to the populated CI. These may include services and service offerings.
3.  \(Optional\) Use the Service and Service Offering attributes to identify the provider services responsible for managing the selected CIs.
4.  \(Optional\) Use the Affected CI related list \[task\_ci\] to identify the CIs that may have caused the change. These CIs are in addition to the CIs previously populated. The \[task\_ci\] table can be populated dynamically or manually.

    **Note:** Dynamic population is not part of the base system. To use dynamic population, you need to configure the Change Request form.


## For more information

[See the video: How Change Management leverages the CSDM](https://www.youtube.com/watch?v=3iCxTeU4ZTA&list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK&index=43)

**Parent Topic:**[Applying CSDM guidelines to Change Management](itsm-change-use-case-product-view.md)

