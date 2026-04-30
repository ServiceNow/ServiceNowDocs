---
title: Service Exchange release notes
description: ServiceNow Service Exchange will be renamed for the 2026 Australia release and will maintain the same functionality. This application enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Service Exchange release notes

ServiceNow® Service Exchange will be renamed for the 2026 Australia release and will maintain the same functionality. This application enables providers and consumers to connect and track services directly between instances without having to configure and maintain custom integrations. Service Exchange was enhanced and updated in the Yokohama release.

## Service Exchange highlights for the Yokohama release

-   Providers can now include client and UI policy scripts in remote record producers, which consumers can review and approve.
-   Providers can now copy local catalog items to Service Exchange as remote record producers either in bulk or individually.
-   Providers can simplify and streamline choice-based transform mapping with ServiceNow Now Assist.
-   Consumers can now add variables to remote record producers for use in consumer pre-flows.

See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US) for more information.

**Important:** Service Exchange is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow® to Yokohama

-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility.
-   The Service Exchange Global Script Include is automatically installed or updated when you install the Service Exchange application on the following platform versions:
    -   Washington DC Patch 9
    -   Xanadu Patch 4
    -   Yokohama
-   Service Exchange 2.x.x, which was first released with the Xanadu release, does not support migration of Service Exchange \(Legacy\) versions. If you are using a Service Exchange \(Legacy\) version, before you upgrade to the Yokohama release, you must follow instructions in the [Service Exchange for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.
-   If you are upgrading from Service Exchange version 1.x.x, follow the steps in [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) to migrate your Service Exchange applications.
-   Due to the introduction of mismatched version support, new entitlements cannot be activated until both the consumers and providers upgrade to Service Exchange version 2.x.x. Older active entitlements will continue to work but new ones cannot be activated.
-   If you upgrade to Service Exchange version 2.0.55 with Sales Customer Relationship Management plug-in version 1.0.4 before upgrading the platform to the Yokohama release, the new Deny ACLs will not be installed. To ensure the Deny ACLs get installed, after upgrading to Yokohama, you must click Repair to reinstall the Service Exchange application.

## New in the Yokohama release

-   **[Remote Catalog Item Client Scripts](https://www.servicenow.com/docs/access?context=service-bridge-v2-add-scripts-to-rrp&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)**

    Provider: Perform more complex tasks and gain better control over the completeness and correctness of catalog requests from the consumer by including catalog client scripts, UI Policy scripts, and other common scripts that consumers can choose to include for Remote Catalog items.

-   **[Copy From Service Catalog Item to Remote Catalog Item](https://www.servicenow.com/docs/access?context=service-bridge-v2-copy-catalog-as-rrp&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)**

    Providers: Eliminate the need to re-create catalog items manually in the Service Exchange remote catalog by copying single and multiple catalog items through the UI to remote record producers that can be synchronized to the consumer instance.

-   **[Transform Mapping Assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-exploring&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Providers: Streamline the transformation mapping process and reduce errors by generating transform mappings between provider and consumer tables automatically using the Transform Mapping Assist feature that leverages the NOW large language model \(LLM\).

-   **[Consumer Variable Sets](https://www.servicenow.com/docs/access?context=service-bridge-v2-consumer-variables&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)**

    Consumers: Manage requested content and flow better by adding additional variables to add customization to your remote record producers.


## Activation information

Install Service Exchange by requesting it from the ServiceNow Store.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The Sales Customer Relationship Management applications enable you to manage the product sales life cycle in your organization, including pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.

-   **[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Improve the employee service experience by automating HR interactions and providing a single platform for all HR services. Replace manual and siloed processes with cross-functional digital workflows for increased efficiency. Align business goals with employee needs, including onboarding, career growth, and other transitions.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

