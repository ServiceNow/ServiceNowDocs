---
title: Admin APIs: Blueprint import and export
description: You can export a blueprint to back it up, or export and import a blueprint to move it from one ServiceNow CPQ environment to another.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-03"
reading_time_minutes: 1
breadcrumb: [API overview and resources, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Admin APIs: Blueprint import and export

You can export a blueprint to back it up, or export and import a blueprint to move it from one ServiceNow CPQ environment to another.

The ServiceNow CPQ blueprint admin APIs provide the import and export API calls for working with blueprints. Common use cases include migrating blueprints across ServiceNow CPQ environments and backing up blueprints. To view the ServiceNow CPQ blueprint admin APIs, see:

[ServiceNow CPQ blueprint admin APIs](https://github.com/logikioopensource/API-Documentation/blob/main/Admin/blueprint.yml)

For a comprehensive list of all ServiceNow CPQ APIs, see the ServiceNow CPQ API Reference:

[https://api-docs.logik.io/\#introduction](https://api-docs.logik.io/#introduction)

You can also view the ServiceNow CPQ open source API documentation on Github:

[https://github.com/logikioopensource/API-Documentation](https://github.com/logikioopensource/API-Documentation)

To learn how to set up admin API keys for calling blueprint APIs, see:

[Intro to admin API keys](cpq-admin-api-keys.md)

## Blueprint export APIs

To export a blueprint via the APIs, the Export blueprint call passes the variable name of the blueprint to start the export job. In response, the call receives a Job ID that can be queried to retrieve the status and to download the blueprint as a ZIP file.

The sequence of API calls to export and download a blueprint is:

1.  Export the blueprint

    Use the blueprint variable in the payload to initiate the export. The Job ID can be polled for the status of the export.

2.  Check the job status

    To check the status, use the Job ID that is returned after the export call. When the status is COMPLETED, proceed to step 3.

3.  Download the export

    Use the same Job ID to download a ZIP file that contains the blueprint.


To view the source code for the Export blueprint call, see:

[Export blueprint call](https://github.com/logikioopensource/API-Documentation/blob/3a6c7259ae1f6bb35f4f80c5ec6f23c86871c342/Admin/blueprint.yml#L32C9-L32C9)

## Blueprint import APIs

To import a blueprint, the Import blueprint call passes a ZIP file of the blueprint to begin an import job.

The sequence of API calls to import a blueprint is:

1.  Import the blueprint

    Select the ZIP file that includes the blueprint. The Job ID can be polled for the status of the import.

2.  Checkthe job status

    To check the status, use the Job ID that is returned after the import call. When the status is SUCCESS, the job is complete.


To view the source code for the Import blueprint call, see:

[Import blueprint call](https://github.com/logikioopensource/API-Documentation/blob/3a6c7259ae1f6bb35f4f80c5ec6f23c86871c342/admin/blueprint.yml#L70)

