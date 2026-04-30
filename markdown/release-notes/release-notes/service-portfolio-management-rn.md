---
title: Service Portfolio Management release notes
description: The ServiceNow Service Portfolio Management application enables you to plan, design, build, and implement your service portfolios. Service Portfolio Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Service Portfolio Management release notes

The ServiceNow® Service Portfolio Management application enables you to plan, design, build, and implement your service portfolios. Service Portfolio Management was enhanced and updated in the Xanadu release.

## Service Portfolio Management highlights for the Xanadu release

-   Updated the availability system property \[com.sn.availability.v2\] so you can set the time zone for service availability records.
    -   Added the ability to change the global time zone for all availability results to reflect that time zone.
    -   Added the ability to set the time zone for availability results to reflect a service offering commitment.
    -   Updated the availability recalculations to reflect the time zone that you set.
    -   Added a read-only time zone field on service availability records.
-   Added a **Teams** related link tab to the service offering records so you can assign more than one team to support a service offering \(one-to-many relationship\).

See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Set the time zone for availability results in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-set-timezone&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Set the availability system property \[com.snc.availability.v2\] to true so you can set the time zone that you want to calculate availability results. The Availability calculations settings page provides you with the choice to calculate availability using the service offering commitment time zone \(yes or no\). It also provides you with the option to set the global availability time zone by selecting a time zone from a provided list. After you select **Yes** to calculate availability with the commitment time zone, the **Time zone** field on the commitment record is used to calculate the availability results. The **Time zone** field on the availability record is read only. After you opt to set the global time zone, all the availability results will use the time zone that you set as global.

    **Note:** The underlying system properties that govern the global time zone and the commitment time zone are exclusive. You can set the global time zone or set the time zone to reflect a service offering commitment but you can't set both at the same time.

-   **[Assign multiple teams to support a service offering in Service Portfolio Management](https://www.servicenow.com/docs/access?context=spm2-assign-teams&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use the added Teams related list in service offerings to assign different group types to support a service offering. The related list functionality is an existing platform feature that was added to the Service Portfolio Management application so you can see the related support teams in the Digital Portfolio Management view. For more information on the platform feature, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


## Activation information

The Service Portfolio Management Core plugin \[com.snc.service\_portfolio\_core\] is available by default for IT Service Management licensed customers. For more information, see [Activate Service Portfolio Management](https://www.servicenow.com/docs/access?context=activate-SPM2-plugin&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Service Portfolio Management — Core adds the Service Offering table \[service\_offering\] to the CSDM.

-   **[Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Service Portfolio Management integrates with the ServiceNow® Service Catalog at the service offering level of the application. You can choose services from an existing catalog as well as initiating service catalog additions.

-   **[Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Service Level Agreement \(SLA\) commitment support functionality is added to Service Portfolio Management by integrating with ServiceNow® Service Level Management.

-   **[Service Builder](https://www.servicenow.com/docs/access?context=service-builder&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    ServiceNow® Service Builder provides a guided walk-through to help service and portfolio owners create and edit services and service offerings.

-   **[Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Add ServiceNow® Digital Portfolio Management \(DPM\) from the ServiceNow Store to view all your Service Portfolio Management data in one centralized place. If you transition to the standard service portfolio structure as described in [Service Portfolio Management portfolios](https://www.servicenow.com/docs/access?context=SPM2-service-portfolios&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US), then you can use key performance indicator \(KPI\) groups in DPM to report on services, nodes, and portfolio performance.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

