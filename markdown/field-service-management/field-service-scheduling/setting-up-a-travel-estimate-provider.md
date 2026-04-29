---
title: Setting up a travel estimate provider
description: Set up a travel estimate provider in Schedule Optimization for each of your technician groups to streamline and enhance the travel planning process.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a scheduling attribute, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Setting up a travel estimate provider

Set up a travel estimate provider in Schedule Optimization for each of your technician groups to streamline and enhance the travel planning process.

## Travel estimate providers

Efficient allocation of work order tasks depends on accurately estimating travel time, considering both the technician's location and the task's location. Schedule Optimization uses travel estimate providers, which calculate distances between technicians and task and are assigned by admins to groups.

You can use third-party map providers in Schedule Optimization to expand your mapping service options beyond the default provider. The supported travel estimate providers are straight-line, Beans.ai, and other third-party providers.

-   Straight-line: This default configuration serves as a backup when a primary configuration isn’t available and a secondary configuration hasn’t been selected. This provider can be modified but it cannot be deleted.
-   Beans.ai: This map provider provides more accurate travel time estimates. Locations that are deemed invalid through geocoding or aren’t reachable by road are excluded from task assignments
-   Third-party map providers: Schedule Optimization supports integration with third-party providers. To configure a third-party provider, you must already have a connection and credential established for that provider.

For more information, see [Create a scheduling attribute for Schedule Optimization](../task/configure-scheduling-attributes.md).

## Map vendor call types

Property: **map\_vendor\_call\_types property**

-   Sync: Default value.
-   Async: Changing the default value to async can improve performance and may result in more outbound requests.

For more information on properties, see [Schedule Optimization properties](../reference/schedule-optimization-properties.md).

## Travel band modifiers

Travel band modifiers adjust travel times based on the time of day, such as during rush hour. You can add these modifiers to either straight-line or Beans.ai configurations. A multiplier is a number used in the configuration to adjust travel time based on expected traffic conditions. When traffic is expected to be heavier than usual, a multiplier greater than 1 increases the travel time. For example, a multiplier of 1.2 adds extra time to account for delays. When traffic is lighter, such as during off-peak hours, a multiplier less than 1 reduces the travel time. For instance, a multiplier of 0.8 shortens the estimated travel time to reflect faster travel.

-   Purpose: Adjust travel times during certain times of day, such as rush hour.
-   Configuration:
    -   Add travel band modifiers to your straight-line or Beans.ai configuration.
    -   Modify travel time results using a multiplier or the time-of-day feature provided by a travel time provider.
    -   **Travel Band Details**:
        -   Range: 30 minutes to four hours.
        -   Can’t overlap.
        -   Set different start and end times for each travel band.

            **Note:** For example, to increase travel time during rush hour to simulate traffic not capture by the baseline values, you could set a travel band for your straight-line configuration between noon and 15:00 Monday through Friday with a multiplier of 1.2.


