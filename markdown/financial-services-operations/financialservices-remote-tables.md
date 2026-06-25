---
title: Financial Services Remote Tables
description: Integrate your core systems using the ServiceNow Financial Services Remote Tables. This feature streamlines development by eliminating the need to recreate the ServiceNow data model for integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financialservices-remote-tables.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data Models, Explore, Financial Services Operations \(FSO\)]
---

# Financial Services Remote Tables

Integrate your core systems using the ServiceNow Financial Services Remote Tables. This feature streamlines development by eliminating the need to recreate the ServiceNow data model for integrations.

## About Financial Services Remote Tables

Financial institutions manage a large volume of account and transaction data through external core applications. To address the challenge of synchronizing this data within the Financial Services Operations application, the Financial Services Remote Tables application has been introduced. This solution enables real-time record lookup into external financial applications without the need to store the data permanently.

Remote tables are a ServiceNow AI Platform functionality that has been integrated with the Financial Services Operations banking applications. For more details on working with remote tables, see [Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables.md).

## Key features

-   Incorporate Financial Services Remote Tables into the Financial Services Operations data model, featuring financial account and transaction tables.
-   Enable on-demand synchronization of lookup records with ServiceNow tables to maintain data accuracy and timeliness.

## Integration architecture

Using Financial Services Remote Tables, you can retrieve data from external sources or another instance through REST or SOAP services. To retrieve data from external sources or another instance, you must create and associate a script definition with a remote table. For more information on script definitions and an example of using a REST API call to look up financial transaction details, see [Lookup remote information in the system of record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-int_guide-agt_table_lookup.md)

\[Omitted image "fso-remote-table-look-up.png"\] Alt text: Relationship diagram illustrating the FSO Remote table look up.

## Setting up FSO Lookup client action

The **Lookup UXF Client action**, included in the Financial Services Remote Tables plugin, is essential for setting up the FSO Lookup Client action. This action integrates the **Action Payload Definition** and is used within a field decorator as a UXF Client action. It is available as part of the Remote table lookup application but requires integration with a field decorator or a declarative action.

The remote tables integration use case includes a step that walks through setting up the FSO Lookup client action. For more information, see [Setting up a remote table integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/setting-up-a-remote-table-integration.md).

## Developer resources

To learn more about remote data options for remote tables, choosing an integration approach, or following a remote table integration walkthrough use case, refer to the following topics for more information:

-   [Remote Data Options for Remote Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-int_guide-remote-data-options-for-remote-tables.md)
-   [Choosing an Integration Approach](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-int_guide-choosing-an-integration-approach.md)
-   [Setting up a remote table integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/setting-up-a-remote-table-integration.md)

-   **[FSO Look Up Client action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-look-up-client-action.md)**  
Look up a record from any table based on defined conditions.
-   **[Components installed with Financial Services Remote Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/components-installed-with-remote-tables.md)**  
Several types of components are installed with the installation of the Financial Services Remote Tables application, including tables and user roles.

**Parent Topic:**[Data Models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/data-models.md)

**Related topics**  


[Create script definitions for a remote table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-remote-table-script.md)

[Create a form action button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-a-new-form-action.md)

[FSO Look Up Client action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-look-up-client-action.md)

[Create a field decorator action button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-a-new-field-decorator-action.md)

