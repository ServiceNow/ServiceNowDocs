---
title: Federal plugin
description: The ServiceNow, Inc. Federal plugin provides additional data elements for public sector customers that align with the Human Capital Information Model \(HCIM\). The HCIM is a set of data standards for Federal human capital management developed by the Human Resources Line of Business \(HRLOB\) at the Office of Personnel Management \(OPM\).
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery, Employee Service Management]
---

# Federal plugin

The ServiceNow, Inc. Federal plugin provides additional data elements for public sector customers that align with the Human Capital Information Model \(HCIM\). The HCIM is a set of data standards for Federal human capital management developed by the Human Resources Line of Business \(HRLOB\) at the Office of Personnel Management \(OPM\).

This plugin is intended for the use of extending the tables such as HR Profile, Location, Position with additional fields and tables relevant to the Federal, State, and Local public sectors.

## Federal plugin overview

The following are some key benefits of the Federal plugin:

-   Promotes interoperability by providing data structures that makes data flow seamlessly to and from agencies, or shared service providers.
-   Provides additional data elements that are commonly used in services agencies provide to the government employees they service.
-   Augments the delivered HR Service Delivery and ServiceNow AI Platform tables.

    For example, the default Locations table \(cmn\_locations\) can be configured to include reference fields from the Duty Station table \(sn\_fedtables\_duty\_station\), or the Duty Location can be added as a field to the HR Profile to display the GeoLoc of the employee’s duty station.

-   Offers prebuilt capability that allows for easier configuration of services and workflows and minimizes customization needs.

**Important:** The tables installed with the Federal plugin are standalone. There are no dependencies between the HR Service Delivery tables and the Federal plugin tables, until the Federal plugin tables are included in the work stream.

## Get started

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Set up Federal plugin](../task/set-up-fed.md#) ![Configure the plugin to get started](../../../common/image/icon-set-up.png) Configure the plugin to get started

</td><td>

[Using Federal plugin](../task/using-fed-app.md) ![Use the plugin to promote interoperability between agencies or shared service providers.](../../../common/image/icon-workspace.png) Use the plugin to promote interoperability between agencies or shared service providers.

</td><td>

[Federal plugin reference](../reference/refer-fed.md#) ![Get details about tables in Federal plugin](../../../common/image/icon-reference.png) Get details about tables in the plugin

</td></tr></tbody>
</table>