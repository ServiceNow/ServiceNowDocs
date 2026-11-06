---
title: Zero Copy Connector for ERP release notes
description: The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Brazil release.The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Brazil release.The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/zero-copy-connector-for-erp-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-20"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, erp data, connect]
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Zero Copy Connector for ERP release notes

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Brazil release.

## About Zero Copy Connector for ERP

-   Retrieve and update data from an ERP system, such as SAP, SuccessFactors, Workday, or Oracle E-Business Suite.
-   Create models that include ERP system data in remote tables and extraction tables.
-   Use extracted and transformed data to build applications that access the models.
-   Accelerate application development with Zero Copy Connector for ERP content packs that contain predefined models and process extensions.

See [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-overview.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    SAP ECC, SAP S/4 HANA, and Oracle E-Business Suite \(12.2 and later\) are the available systems that integrate with Zero Copy Connector for ERP.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/build-automate-rn-landing.md)

## Brazil Early Availability 2 \(10.7.1, October 2026\)

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Brazil release.

### What's new

-   **[Support for Workday RaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/obtain-data-from-workday-using-raas.md)**

    Add Workday RaaS reports to read operations by pasting a sample report response.


## Brazil Early Availability \(10.6.0, September 2026\)

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Brazil release.

### What's new

-   **[Support for Oracle E-Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-oracle-rest-support.md)**

    Select Oracle E-Business Suite \(12.2 or later\) as the ERP software when you configure an ERP system record. Oracle E-Business Suite connects through REST.

-   **[Use Oracle EBS ISG services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-create-an-oracle-ebs-connection.md)**

    Add Oracle E-Business Suite Integrated SOA Gateway \(ISG\) services to a model using their Web Application Description Language \(WADL\) definitions. When you create a model entity for a WADL operation, Zero Copy Connector for ERP generates its fields from the operation's WADL and XSD definitions.

-   **[AI search for WADL service endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-oracle-ebs-wadl-support.md)**

    Search for endpoints of discovered WADL services from the interface using AI Search.

-   **[Row count for the scriptable API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-api-getrowcount.md)**

    Call the `getRowCount()` method on the `API` class to return the total number of rows that a query matches without retrieving the records. Configure the query as you would for `execute()`.


