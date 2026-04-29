---
title: Choosing between record producers and catalog items
description: Both the record producer and standard catalog item in App Engine Studio \(AES\) create experiences where users can submit requests through a service portal. However, record producers are more extensible, and enable users to create a record in any table.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add an experience, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Choosing between record producers and catalog items

Both the record producer and standard catalog item in App Engine Studio \(AES\) create experiences where users can submit requests through a service portal. However, record producers are more extensible, and enable users to create a record in any table.

## Consider the level of customization

Record producers allow for more customization, making the most of the App Engine tools to build experiences from scratch.

Catalog items represent services or items a user can request. The catalog of all items is called the Service Catalog, and is part of Service Catalog Management.

## Comparison of record producers and standard catalog items

<table id="table_zrs_qq3_kxb"><thead><tr><th>

Functional area

</th><th>

Record producer

</th><th>

Catalog item

</th></tr></thead><tbody><tr><td>

Purpose

</td><td>

Create custom fulfillment experiences using App Engine automation tools.

</td><td>

Support simple request management applications for which a predefined approval and qualification process exists, such as requesting IT hardware and software.

</td></tr><tr><td>

Extensibility

</td><td>

Customizable.

</td><td>

Pre-defined.

</td></tr><tr><td>

Example

</td><td>

Password reset form that creates a password reset request.

</td><td>

Form to request a parking permit.

</td></tr><tr><td>

Development model

</td><td>

Process is as follows:1.  Set up a business-focused data model.
2.  Define the kind of experience your users will leverage.
3.  Define the automation or business logic.
4.  Define the user roles that will use the app.

</td><td>

Catalog items heavily rely on the request fulfillment process for fulfilling items defined in Service Catalog, a central, accurate, and consistent source of data.

</td></tr><tr><td>

Reporting

</td><td>

Easier to create dashboards with a purpose-built data model.

</td><td>

Requires creating database views and scripting to gather variables into other tables to configure specific reports.

</td></tr><tr><td>

Scalability

</td><td>

Business-focused app makes it easier to find resources and make app changes in a low-code environment.

</td><td>

Typically part of a Service Catalog Management operation with a dedicated team managing each catalog.

</td></tr><tr><td>

Security

</td><td>

Scoped apps allow flexibility to manage permissions without being an administrator.

</td><td>

Catalog items are typically built in a specific scope, and less flexible.

</td></tr></tbody>
</table>## Help topics on record producers and standard catalog items

For more information, see the following topics:

-   Record producers:
    -   [Add a record producer](../task/add-a-record-producer.md)
    -   [Sample record producer](record-producers-example.md)
-   Standard catalog items:
    -   [Add a standard catalog item](../task/add-standard-catalog-item.md)
    -   [Sample standard catalog item](standard-catalog-item-examples.md)

**Parent Topic:**[Add an application experience](add-experience.md)

