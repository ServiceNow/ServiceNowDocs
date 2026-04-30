---
title: Create a campus to appear on the Safe Workplace Dashboard
description: You can create a campus from existing locations to appear on the Safe Workplace Dashboard.
locale: en-US
release: yokohama
product: Safe Workplace Dashboard
classification: safe-workplace-dashboard
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Safe Workplace Dashboard, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a campus to appear on the Safe Workplace Dashboard

You can create a campus from existing locations to appear on the Safe Workplace Dashboard.

Route the following information to the Safe Workplace Dashboard and display this information by campus:

-   User health and willingness to return to work.
-   Building readiness.
-   Personal protective equipment inventory.
-   Active contact tracing cases.
-   Potentially exposed contacts under investigation.

Ensure that you install and use the following applications for the Safe Workplace Dashboard. Each application has a reference to a location.

-   ServiceNow® Emergency Self Report references the location in the user's profile.
-   ServiceNow® Emergency Outreach with Employee Readiness Surveys installed. These applications reference the location in the user's profile.
-   ServiceNow® Workplace PPE Inventory Management has defined stockrooms, and the location is a required field for a stockroom.
-   ServiceNow® Employee Health Screening has a form for selecting a location and a user to submit the compliance values.
-   The Space Administration module of ServiceNow Workplace Core is where organization facilities are defined. Within a building, floors, areas, and workspaces are defined. These definitions provide for proximity screening, cleaning assignments, and workspace reservations.

    One or more buildings are assigned to a campus. The location icons displayed on the Safe Workplace Dashboard overview show the campus and any associated buildings when you point to an icon.

-   ServiceNow Contact Tracing references the affected person's campus from a case. If the campus information is not available, then Contact Tracing references the location in the affected person's user profile.

**Note:** When selecting locations for users, stockrooms, and entry requests, select a company location that existed before you installed Workplace Core. Don't select a site, campus, or building created in the Workplace Core application.

For Workplace PPE Inventory Management, Employee Health Screening, and others, the location must be tied to a Workplace Core campus or building for the location to appear on the Safe Workplace Dashboard.

![U.S. map on the dashboard displaying four location icons: three with alerts and pop-up details for one campus.](../image/dashboard-icons-campus.png "Safe Workplace Dashboard map with location icons")

The locations \[cmn\_location\] defined for the organization are the reference that Performance Analytics uses to generate alerts. Configure the building definitions in Workplace Core with a parent location and the corresponding latitude and longitude.

To associate locations with infectious diseases, such as COVID-19 data, from the COVID-19 Global Health Data Set, verify that all locations are associated with a state or country.

## Create a campus to appear on the Safe Workplace Dashboard

There are multiple methods that you can use to create a campus that appears on the Safe Workplace Dashboard.

-   Auto-map a location and create a campus.
-   Manually associate a location and create a campus.
-   Manually map a location to a campus \(Workplace Core\).

## Auto-map multiple locations and create campuses

You can create multiple campuses with corresponding latitude and longitude coordinates and a site automatically by selecting multiple locations.

The campuses appear on the Safe Workplace Dashboard.

## Manually map a location to a campus

You can map an existing campus to an existing location manually and have it appear on the Safe Workplace Dashboard.

## Manually map a location to a campus \(Workplace Core\)

As an alternative, you can use Workplace Core to manually create a campus and have it appear on the Safe Workplace Dashboard.

-   **[Auto-map a location and create a campus](../task/autoconfig-safe-wp-dash.md)**  
Create multiple campuses automatically by mapping them from locations so that they appear on the Safe Workplace Dashboard.
-   **[Manually map a location and campus](../task/man-create-campus.md)**  
Manually map an existing location to an existing campus and site using Campus Locations.
-   **[Manually map a location to a campus \(Workplace Core\)](../task/configure-safe-workplace-dashboard.md)**  
Use Workplace Core as an alternative to the Safe Workplace Dashboard to manually map a location to a campus so that it appears on your Safe Workplace Dashboard.

**Parent Topic:**[Safe Workplace Dashboard](safe-workplace-dashboard.md)

