---
title: Multi-service monitoring for shared endpoints
description: A single HTTP endpoint or discovered API is tagged to more than one application service so every team that depends on it is notified when it fails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/multi-service-monitoring.html
release: australia
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [synthetic monitoring, multi-service, application service, shared endpoint, CMDB]
breadcrumb: [Explore, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Multi-service monitoring for shared endpoints

A single HTTP endpoint or discovered API is tagged to more than one application service so every team that depends on it is notified when it fails.

## Why tag more than one service

In earlier releases, an HTTP endpoint check or a discovered API check could relate to only one application service. If a shared endpoint served several teams, each team had to create its own check against the same endpoint. This was necessary to see that endpoint's health reflected against their own service.

You can now tag a single HTTP endpoint or discovered API to multiple application services. One check now represents every team that depends on that shared endpoint. The underlying CMDB relationships between the endpoint and each application service are preserved rather than replaced when a new service is added.

## How it works

When you select more than one application service for an HTTP endpoint or discovered API, synthetic monitoring creates a Connects to::Connected by relationship between the endpoint and each service you select. Adding a new service to an endpoint does not remove the relationships to services that were already tagged.

The endpoint's related services list shows every application service tagged to it, with duplicate entries removed, so each team can see which other services share the same endpoint.

When a shared endpoint fails a test, the resulting event is evaluated against every application service tagged to that endpoint, and each of those services can show the impact on the Service Health dashboard.

**Note:** Alert routing to each team individually is not part of this release. All teams tagged to a shared endpoint currently see the same alert configuration for the check.

otherprops="store-2026-09"&gt;How the Service Health dashboard resolves impacted services depends on how the endpoint was added to the CMDB:

-   **Endpoints created directly in synthetic monitoring**

    Impacted services display on the Service Health dashboard through an automatic fallback mechanism.

    **Important:** When you upgrade to a higher platform version, manually created entries must be repopulated using upgrade scripts. Contact ServiceNow support to request these scripts.

-   **Endpoints discovered and mapped through Discovery or Service Mapping**

    Impacted services display on the Service Health dashboard because they're resolved through the platform's Discovery/Service Mapping model.


## Where multi-service tagging applies

-   HTTP endpoint checks. See [Create and edit a synthetic monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-synthetic-monitor.md).
-   API Insights discovered API checks. See [Create a synthetic monitor for a discovered API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/create-synthetic-monitor-for-discovered-api.md).

