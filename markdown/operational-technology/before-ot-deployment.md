---
title: Before deploying Operational Technology \(OT\) Discovery
description: To discover assets in your OT environment, the Discovery for Operational Technology \(OT\) solution provides the Service Graph Connector, the Discovery Console for OT, the Discovery Sensor for OT, and the OT Discovery Collector.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Deploy Operational Technology Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Before deploying Operational Technology \(OT\) Discovery

To discover assets in your OT environment, the Discovery for Operational Technology \(OT\) solution provides the Service Graph Connector, the Discovery Console for OT, the Discovery Sensor for OT, and the OT Discovery Collector.

## Before you deploy

Consider these questions before planning your OT Discovery deployment. This list is not exhaustive.

-   Are you looking at OT devices or IT devices in the OT network?
-   Have you planned the Site location?
-   What is the network layout and architecture of the Site location? Is it a flat or segmented layout?
    -   The best way to start is to place a Discovery Sensor for OT in a location that includes many of the devices to be queried.

    -   Next, place additional Sensors in areas of the network that might have segmentation or other barriers, such as a NATed environment or segmented silos.

-   Are there any network zones in place? Identify any NATed networks or copy-paste networks \(sites with identical IP ranges\).

    **Note:** When Sensors can reach the same zoned location or when assets are dual-homed, carefully document the zoned Sensor configuration to avoid creating duplicate asset records.

-   What communication pathways exist within the site? This information helps determine optimal Discovery Sensor for OT placement.
-   If Sensors are deployed in each Network \(NW\) zone, can they communicate with the assets in the OT network?
-   Are there any sub-networks where the Sensor can't reach? Are there any devices where the OT Discovery Collector needs to be installed?
-   Where does the Discovery Console for OT get installed?
-   Can one Console be used for multiple sites or does the deployment require one Console per site?
-   Are there communication paths between the Sensors and the Console?
-   Does the MID Server exist in DMZ?
-   Is there a communication path between the Console and the MID Server?
-   Are there any other tools \(IDS or Discovery tools\) in the environment?

## Adding capabilities over time

With OT Discovery, you can add layers of capabilities over time such as:

-   Deploying the Discovery Console for OT and Discovery Sensor for OT in a central location with access to multiple sites.
-   Deploying the Discovery Sensor for OT at individual sites, with additional Sensors deployed as needed for policy enforcement or non-IP-enabled asset monitoring.

## Adding locations over time

On a site-by-site level, you can add locations over time, such as deploying the Discovery Console for OT and the Discovery Sensor for OT at a pilot site. See the Console's [Sites page](sites-page.md) for more information.

