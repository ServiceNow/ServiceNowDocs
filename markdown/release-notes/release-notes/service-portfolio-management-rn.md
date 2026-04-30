---
title: Service Portfolio Management release notes
description: The ServiceNow Service Portfolio Management application enables you to plan, design, build, and implement your services, service offerings, and service portfolios. Service Portfolio Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Service Portfolio Management release notes

The ServiceNow® Service Portfolio Management application enables you to plan, design, build, and implement your services, service offerings, and service portfolios. Service Portfolio Management was enhanced and updated in the Yokohama release.

## Service Portfolio Management highlights for the Yokohama release

-   Use the added options to edit and manage your service portfolios.
    -   Add life cycle fields to the taxonomy node records of your portfolios to align with the Common Service Data Model \(CSDM\).
    -   Added more flexibility to remap taxonomy nodes. You can move an entire branch of a taxonomy from one portfolio to another, including the automatic move of its child nodes.
    -   Reparent taxonomy nodes when you move them to a new location in a portfolio. You can also add a new taxonomy node in the middle of an existing portfolio, either between two nodes or between a node and a service.
-   Recognize the updated label for technical services.

See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Edit and manage service portfolios in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-edit-manage-portfolios&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use the updated options to edit and manage your service portfolios:

    -   [Manage the CSDM life cycle fields in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-lifecycle-fields&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
    -   [Remap service portfolio taxonomy nodes in Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-remap-taxo-nodes&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
-   **[Use Service Portfolio Management services](https://www.servicenow.com/docs/access?context=SPM2-services&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Recognize the updated label for technical services. The updated label aligns with the CSDM, version 5.0. Even though the table name hasn't changed, the services label is updated in the Service Portfolio Management application and in all ServiceNow applications or workspace environments that display services. The label for service offerings remains the same for all releases: Service offering in the \[service\_offering\] table.

    |Table name|Label in Xanadu and prior releases|Label in Yokohama and later releases|
    |----------|----------------------------------|------------------------------------|
    |\[cmdb\_ci\_service\_technical\]|Technical Service|Technology Management Service|


## Activation information

The Service Portfolio Management Core plugin \[com.snc.service\_portfolio\_core\] is available by default for IT Service Management licensed customers. For more information, see [Activate Service Portfolio Management](https://www.servicenow.com/docs/access?context=activate-SPM2-plugin&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Service Portfolio Management — Core adds the Service Offering table \[service\_offering\] to the CSDM.

-   **[Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Service Portfolio Management integrates with the ServiceNow® Service Catalog at the service offering level of the application. You can choose services from an existing catalog as well as initiating service catalog additions.

-   **[Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Service Level Agreement \(SLA\) commitment support functionality is added to Service Portfolio Management by integrating with ServiceNow® Service Level Management.

-   **[Service Builder](https://www.servicenow.com/docs/access?context=service-builder&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    ServiceNow® Service Builder provides a guided walk-through to help service and portfolio owners create and edit services and service offerings.

-   **[Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Add ServiceNow® Digital Portfolio Management \(DPM\) from the ServiceNow Store to view all your Service Portfolio Management data in one centralized place. If you transition to the standard service portfolio structure as described in [Service Portfolio Management portfolios](https://www.servicenow.com/docs/access?context=SPM2-service-portfolios&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US), then you can use key performance indicator \(KPI\) groups in DPM to report on services, nodes, and portfolio performance.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

