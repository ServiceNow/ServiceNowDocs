---
title: Digital integration form \(easy form\) in EA Workspace
description: The digital integration represents the integration between two business applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-digital-integ-form.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Digital integration form \(easy form\) in EA Workspace

The digital integration represents the integration between two business applications.

## Digital integration form \(easy form\) fields

<table id="table_ptg_nwm_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subscriber Business Application

</td><td>

Name of the business application that uses the provided interface to consume, exchange, or ingest data to support a business capability. The subscriber business application is affected by the changes or an outage, causing connection or data loss.**Note:** The provider and subscriber roles define interface ownership, not data flow direction. The provider owns the digital interface; the subscriber consumes it. Data flow direction—whether incoming, outgoing, or bidirectional—is set separately using the **Data Flow Direction** field and reflects which application initiates the connection. For example, the provider can receive data \(incoming\) if the subscriber initiates the connection. For more information, see [Example: Provider and subscriber with data flow directions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/example-prov-n-subsc-roles-with-data-flow.md).

</td></tr><tr><td>

Subscriber Digital Interface

</td><td>

Name of the digital interface that subscribes for the integration.

</td></tr><tr><td>

Provider Business Application

</td><td>

Name of the business application that provides the digital interface that enables other applications to consume or ingest data. Changes, ownership, and responsibilities of the interface are often connected to the provider.**Note:** The provider and subscriber roles define interface ownership, not data flow direction. The provider owns the digital interface; the subscriber consumes it. Data flow direction—whether incoming, outgoing, or bidirectional—is set separately using the **Data Flow Direction** field and reflects which application initiates the connection. For example, the provider can receive data \(incoming\) if the subscriber initiates the connection. For more information, see [Example: Provider and subscriber with data flow directions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/example-prov-n-subsc-roles-with-data-flow.md).

This field is automatically generated and can't be edited.

</td></tr><tr><td>

New Provider Digital Interface

</td><td>

Option to create a digital interface. This field is a placeholder digital interface that is related to a provider business application.

</td></tr><tr><td>

Provider Digital Interface

</td><td>

Name of the digital interface. As a digital integration between two business applications or services uses a digital interface \(API\), you must select an interface related to the provider business application or service.

</td></tr><tr><td>

IT Owner

</td><td>

The owner within the IT organization who owns the digital integration. It can be the same person who owns the parent subscriber business application.

</td></tr><tr><td>

Business Owner

</td><td>

The owner of the business function who owns the digital integration. It can be the same person who owns the parent subscriber business application.

</td></tr><tr><td>

Digital Integration Name

</td><td>

Name of the digital integration.This field is auto-populated when the **Subscriber Business Application**, **Provider Business Application**, and the **Digital Interface** fields are selected. You can modify the auto-populated name.

</td></tr><tr><td>

Type

</td><td>

Type of the integration. Use the following options:

-   **Data Integration**: Use this option when the integration must mainly focus on the exchange of data such as users, groups, locations, configuration items, and departments.
-   **Process Integration**: Use this option when the integration is about an interaction of transactional data to support a specific process.
-   **User Interface Integration**: Use this option when the integration opens a connection with another application and sends app data via a URL to query the application.

</td></tr><tr><td>

Subtype

</td><td>

Subtype of the integration.This field appears only when **Data Integration** is selected from the **Type** field. Use the following options:

-   Process configuration
-   Foundation data
-   Configuration items
-   Events
-   Reporting
-   Syslog

</td></tr><tr><td>

Trigger

</td><td>

How to trigger the integration.Use the following options:

-   Manual
-   Scheduled
-   Process Driven
-   Event

</td></tr><tr><td>

Interval

</td><td>

Frequency to trigger the integration.Options for the interval are as follows:

-   Seconds
-   Minutes
-   Hours
-   Days
-   Weeks
-   Months
-   Quarters
-   Years
-   On Demand
-   Real Time

</td></tr><tr><td>

Description

</td><td>

Description about the digital integration. Describe in detail why the integration is being created between two business applications or between an external service provided interface and a business application and what business value it adds.

</td></tr></tbody>
</table>Additional fields appear after the digital integration is created. For details on the additional fields, see [Digital integration form in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-digital-integration-form.md).

**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Add or edit a digital integration in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-digital-integ.md)

