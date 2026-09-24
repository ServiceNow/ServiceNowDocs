---
title: Service Exchange \(formerly Service Bridge\) release notes
description: The ServiceNow Service Exchange application, formerly known as Service Bridge, enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. See the following sections for release notes by version.Manage visibility and knowledge base assignment for FDS-synced knowledge articles, and add a scan check that sends a P1 alert when the Service Exchange Admin Group has no active users, stopping once it's populated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-exchange-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Exchange \(formerly Service Bridge\) release notes

The ServiceNow® Service Exchange application, formerly known as Service Bridge, enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. See the following sections for release notes by version.

## About Service Exchange

-   Run provider and consumer instances on different platform releases and application versions without disrupting the active entitlements or processes.
-   Keep the development of shared catalogs and the workflows/integrations in the provider instance while sharing them with consumers as simple record producers that generate integrated requests in the provider instance.
-   Share selected foundational data types with your consumers on a scheduled cadence to reduce manual effort, and eliminate the need to share data externally.

See [Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/tmt-service-bridge-both-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/technology-industry-rn-landing.md)

## Version 2.4.0

Manage visibility and knowledge base assignment for FDS-synced knowledge articles, and add a scan check that sends a P1 alert when the Service Exchange Admin Group has no active users, stopping once it's populated.

### What's new

-   **[Knowledge article sync via FDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/knowledge-base-assignment.md)**

    Assign knowledge articles from a source instance to a valid knowledge base on the target instance via Foundation Data Sync. The target instance creates a company knowledge base automatically when the source does not specify one.

-   **[Hide a synced knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/hide-synced-knowledge-article.md)**

    Hide a knowledge article that was synced to the target instance through Foundation Data Sync \(FDS\) so that it's no longer visible to other users. Knowledge articles synced from a source instance aren't owned by the target instance, so actions like Retire and Checkout don't apply to them.


