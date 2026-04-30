---
title: Service Exchange release notes
description: The ServiceNow Service Exchange application enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Service Exchange release notes

The ServiceNow® Service Exchange application enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Xanadu release.

## Service Exchange highlights for the Xanadu release

-   Enable providers to adopt new features and provide uninterrupted service to their consumers who have not upgraded.
-   Assess entitlements for compatibility before syncing them to consumers.
-   Enable consumers to run specific processes such as approvals before synchronizing tasks with their providers.
-   Support automated synchronization of configuration data between provider and consumer instances.

See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US) for more information.

**Important:** Service Exchange is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Service Exchange to Xanadu

-   Service Exchange 2.x.x that is being released with the Xanadu release does not support migration of the Service Exchange \(Legacy\) versions. If you are using a Service Exchange \(Legacy\) version, before you upgrade to the Xanadu release, you must follow instructions in the [Service Exchange for Providers \(Legacy\) - Migration Utility \(KB1499823\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.
-   If you are upgrading from version 1.x.x of Service Exchange, follow the steps listed in [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release - KB1700387\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) to migrate your Service Exchange applications.
-   Due to the introduction of mismatched version support, new entitlements cannot be activated until both the consumers and providers upgrade to the Xanadu release. Older active entitlements will continue to work but new ones cannot be activated.

## New in the Xanadu release

-   **[Service Exchange mismatched version support](https://www.servicenow.com/docs/access?context=service-bridge-v2-mismatch-version&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

    Providers and consumers can run different versions of the Service Exchange applications without affecting their ability to exchange data. Providers can adopt new features without coordinating their application upgrades with their consumers.

-   **[Configuration revisions](https://www.servicenow.com/docs/access?context=service-bridge-v2-config-revision&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

    Providers can develop and deploy new versions or revisions of entitlements with updated functionality to compatible consumers without affecting consumers who have not updated their application. Consumers can therefore use older revisions of entitlements including remote task definitions, remote record producers, and foundation data sync offerings while deploying new revisions.

-   **[Consumer pre-flows](https://www.servicenow.com/docs/access?context=service-bridge-v2-conf-consumer-flow&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

    Consumers can control data synchronization with their providers by associating a flow with a Service Exchange remote record producer and run consumer-defined processes, such as approvals, before a task is synchronized to their provider.

-   **[Integration with Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=service-bridge-v2-omt-intg&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US)**

    Providers can enable customers to quickly order entitled Sales Customer Relationship Management product offerings from their service catalog by publishing them as remote record producers on consumer instances.


## Deprecations

-   Service Exchange \(legacy\) application is now deprecated and no longer supported or available for new activation. The Service Exchange for Consumers application provides the latest experience for this functionality.
-   Service Exchange for Providers \(legacy\) application is now deprecated and no longer supported or available for new activation. The Service Exchange for Providers application provides the latest experience for this functionality.

See [KB1499823](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) for details on migrating from the legacy version.

## Activation information

Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The Sales Customer Relationship Management applications enable you to manage the product sales life cycle in your organization, including pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

