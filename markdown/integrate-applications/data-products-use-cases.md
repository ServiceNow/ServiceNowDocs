---
title: Data products use cases
description: Explore common scenarios for publishing data products and learn which pattern fits your data and your consumers' needs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 3
breadcrumb: [Explore, Data Products, Workflow Data Fabric]
---

# Data products use cases

Explore common scenarios for publishing data products and learn which pattern fits your data and your consumers' needs.

A data product is built on one or more data interfaces, each of which determines how source data is accessed and combined. The right data interface type depends on where your data lives, how it is structured, and what consumers want to do with it.

A travel company's loyalty analytics team is seeing a clear trend: Gold Star members are flying less. The central question driving the investigation is: on which routes are Gold members booking less, and is it getting worse? The data lives in Snowflake — flight segments, a points ledger, and member profiles. No analyst has direct warehouse access, and the data is too sensitive to export. The team needs a way to query live Snowflake data from within ServiceNow, with access controls they can manage.

The team breaks the investigation into four specific questions, each answered by a dedicated data interface:

-   Which routes generate the most points-earning activity?
-   How many unique Gold members booked each route last quarter?
-   Which routes are seeing declining booking volume over time?
-   How many long-tenured Gold members are currently inactive?

## Tracking booking trends across routes and cabin classes

To track booking volume over time, the team needs route, month, and cabin class. All of this data lives in a single Snowflake table, FLIGHT\_SEGMENTS. A single-table data interface over FLIGHT\_SEGMENTS exposes the raw segment data, and the Platform Analytics dashboard applies date filters and top-route rankings at query time. Keeping the interface general-purpose means the same data can power multiple dashboard widgets without rebuilding it for each one. ![Data interface configuration showing single table connection to flight_segments in Snowflake with 11 columns verified.](../image/wdf-data-product-usecase-01.png)

## Identifying long-tenured members who have gone quiet

Everything needed to answer the inactive member question — loyalty tier, tenure length, active or inactive status — lives in MEMBER\_PROFILE. A single-table interface filters for Gold members with five or more years of tenure and inactive status. That interface powers both the KPI widget showing 10 inactive high-tenure Gold members and the drop-off chart broken down by hub airport.

![Data interface configuration showing single table connection to member_profile in Snowflake with 8 columns verified.](../image/wdf-data-product-usecase-02.png)

## Connecting points earnings to the routes where they happen

Knowing which routes drive the most points-earning activity requires connecting two tables. Points transactions live in POINTS\_LEDGER, but the route information — origin, destination — lives in FLIGHT\_SEGMENTS. The two tables share a booking\_id. A JOIN data interface links them on that key, filters for EARN transactions only, and produces a flat result showing total points earned per route. The analyst querying the dashboard sees one table; the join logic is invisible to them. ![Data interface configuration showing join between flight_segments and points_ledger tables with 18 total columns.](../image/wdf-data-product-usecase-03.png)

## Measuring Gold member engagement route by route

The fourth question — how many Gold members are booking each route — requires connecting flight data to member data. FLIGHT\_SEGMENTS holds the route and booking records; MEMBER\_PROFILE holds the loyalty tier. A JOIN interface links the two tables, filters for tier = GOLD, and returns unique member count and total bookings per route for the previous quarter. ![Data interface configuration showing join between member_profile and flight_segments tables with 18 total columns.](../image/wdf-data-product-usecase-04.png)

## The outcome: Travel Pulse Dashboard

The Data Steward packages all four data interfaces into a single data product. The steward publishes it to the Data Catalog. The loyalty analyst — who has no warehouse access — discovers the product, requests access, and builds the Travel Pulse Dashboard in Platform Analytics. Each widget queries one interface directly against live Snowflake data. No data is copied, extracted, or replicated. ![Travel Pulse Dashboard in Platform Analytics showing booking trends, route rankings, and Gold member analytics.](../image/wdf-data-product-usecase-dashboard.png)

## Extending the pattern: combining data from multiple sources

If the team later needs to include booking data from a partner airline, they can use a UNION data interface. The partner data is stored in a separate Snowflake table with the same schema as FLIGHT\_SEGMENTS. A UNION data interface stacks both tables into a single queryable view. Consumers query one unified dataset. No existing interfaces change.

This pattern fits whenever the same kind of record is tracked in multiple systems. Records such as bookings, orders, transactions, or events may be divided by region, time period, or business unit. The reporting need is to cover all of them at once.

