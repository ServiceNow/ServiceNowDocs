---
title: Legacy - Development considerations
description: When you are developing code, consider some of these suggestions for the most efficient performance.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Legacy - Production deployment tips, Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Development considerations

When you are developing code, consider some of these suggestions for the most efficient performance.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   **Production instances shouldn’t publish to the Git repository**

    To protect the integrity of production, you shouldn’t push changes to publish to the Git repository from production even though technically you can open and commit changes in the application in ServiceNow® Studio. The “Can Edit Application in Studio” option can be disabled in production on the **sys\_app** record. But it resets at the next source code operation that triggers an update \(that is, when you apply remote changes or switch branches\).

-   **Dependencies are not installed when installing an application from the Git repository**

    Source-controlled applications do not automatically install or upgrade if they are listed as the dependency of your application. Instead, the customer must install or upgrade the source-controlled application on its own. The customer is also responsible for installing and upgrading the applications in the correct order.

-   **Tight control on source control privileges in production**

    The source code operations are generally available to those with development privileges in the instance. Since production environments shouldn’t have ongoing development, be sure to tightly control admin and delegated development privileges to avoid data loss and other serious consequences.


**Parent Topic:**[Legacy - Production deployment tips](tips-production-deployment.md)

