---
title: Service Exchange \(formerly Service Bridge\) release notes
description: The ServiceNow Service Exchange application, formerly known as Service Bridge, enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. See the following sections for release notes by version.Now Service Exchange connections are now more secure and recover faster. Stronger authentication replaces password-based access, and the system automatically fixes known connection errors, so you spend less time on manual troubleshooting and keep integrations running reliably.Manage visibility and knowledge base assignment for FDS-synced knowledge articles, and add a scan check that sends a P1 alert when the Service Exchange Admin Group has no active users, stopping once it's populated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-exchange-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Exchange \(formerly Service Bridge\) release notes

The ServiceNow® Service Exchange application, formerly known as Service Bridge, enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. See the following sections for release notes by version.

## About Service Exchange

-   Run provider and consumer instances on different platform releases and application versions without disrupting the active entitlements or processes.
-   Keep the development of shared catalogs and the workflows/integrations in the provider instance while sharing them with consumers as simple record producers that generate integrated requests in the provider instance.
-   Share selected foundational data types with your consumers on a scheduled cadence to reduce manual effort, and eliminate the need to share data externally.
-   Upgrade consumer connections from Resource Owner Password Credentials \(ROPC\) to Client Credentials OAuth by using the Upgrade Auth action on the Connection record, to improve security and compliance without off-boarding or re-onboarding.

See [Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/tmt-service-bridge-both-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/technology-industry-rn-landing.md)

## Version 2.5.x

Now Service Exchange connections are now more secure and recover faster. Stronger authentication replaces password-based access, and the system automatically fixes known connection errors, so you spend less time on manual troubleshooting and keep integrations running reliably.

### What's new

-   ****

### What's changed

-   **[Upgrade authorization on a provider instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown) and [Upgrade authorization on a consumer instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)**

    Upgrade consumer connections from Resource Owner Password Credentials \(ROPC\) to Client Credentials OAuth by using Upgrade Auth on the connection record, to authenticate connections as an application rather than of with a user's password, improving security and compliance. Run the upgrade once from the provider instance to update both instances, keep the connection active, and avoid off-boarding and re-onboarding the consumer.


-   **[Automatic mitigation for connection issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)**

    Fix known connection errors automatically when a connection goes down, to restore data exchange faster and reduce manual troubleshooting. Review each fix in the issue work notes in the Now Service Exchange Center.


### What's deprecated or removed

-   ****

### Plugin information

-   **New plugins**

     \(\): 

-   **Deprecated plugins**

     \(\): 

-   **Plugins planned for deprecation**

     \(\): Planned for deprecation in . 

-   **Renamed or changed plugins**

     \(\): 


## Version 2.4.0

Manage visibility and knowledge base assignment for FDS-synced knowledge articles, and add a scan check that sends a P1 alert when the Service Exchange Admin Group has no active users, stopping once it's populated.

### What's new

-   **[Knowledge article sync via FDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/knowledge-base-assignment.md)**

    Assign knowledge articles from a source instance to a valid knowledge base on the target instance via Foundation Data Sync. The target instance creates a company knowledge base automatically when the source does not specify one.

-   **[Hide a synced knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/hide-synced-knowledge-article.md)**

    Hide a knowledge article that was synced to the target instance through Foundation Data Sync \(FDS\) so that it's no longer visible to other users. Knowledge articles synced from a source instance aren't owned by the target instance, so actions like Retire and Checkout don't apply to them.


