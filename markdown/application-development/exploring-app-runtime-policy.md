---
title: Exploring Application Runtime Policy
description: Application Runtime Policy \(ARP\) is an opt-in zero-trust security framework for custom applications that tracks and enforces fine-grained controls over what resources an application can access at runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/exploring-app-runtime-policy.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [explore, Application Runtime Policy, ARP, zero trust, app security]
breadcrumb: [Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Exploring Application Runtime Policy

Application Runtime Policy \(ARP\) is an opt-in zero-trust security framework for custom applications that tracks and enforces fine-grained controls over what resources an application can access at runtime.

## Application Runtime Policy \(ARP\) overview

Application Runtime Policy \(ARP\) is an opt-in, zero-trust security framework for custom app creation and runtime. It enforces fine-grained controls over scripting, record, platform, and cross-scope or cross-origin network resources.

When ARP is activated for an application in development, network and cross-scope access policies are automatically tracked and recorded in the application's policy metadata as you develop application functions. The generated policies can be automatically approved or can require review and manual approval, depending on how ARP is configured for the application.

Activating ARP also generates one default quota configurations record for the application in development.

## ARP users

|User|Description|
|----|-----------|
|Custom application developers|Developers who build custom applications on the ServiceNow AI Platform. They opt in to ARP during development to define and review the resource access policies their application requires before making the application available to other instances in their organization.|
|ServiceNow Store partner developers|Partner developers who develop and publish applications to the ServiceNow Store. ARP gives ServiceNow Store partners a structured way to declare and certify their application's runtime resource access, which reduces the time required for certification review.|

## ARP workflow

The following steps describe the end-to-end ARP workflow from application development to installation on a different ServiceNow AI Platform instance.

1.  Opt in to ARP at development time from the custom application \[sys\_app\] form by setting the **Application Runtime Policy** field to **Tracking** or **Enforcing**.
2.  As you develop application functionality, ARP tracks client and server-side cross origin network requests and automatically creates policy records in the application's metadata.
    -   In Tracking mode, policies automatically have the **Allowed** status.
    -   In Enforcing mode, policies are created with a status of **Requested** and the access is blocked until you approve the policy.
    -   The first instance of each violation is recorded in the Runtime Policy Violation Log, regardless of whether ARP is activated in Tracking or Enforcing mode.
3.  If using the Enforcing mode, review each policy record and sets its status to **Allowed** to allow access, or **Denied** to block it.
4.  When the application is ready for publication, the approved policies are packaged and published with the application to your organization's Application Repository or to the ServiceNow Store.

    For more information about publishing to the Application Repository, see [Publish an application to the application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-repository-self-hosted/t_PublishAppsToTheAppRepository.md). For more information about publishing an application to the ServiceNow Store, see [Publish an application to the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/t_PublishAppsToTheServiceNowStore.md).

    If you publish to the ServiceNow Store, the Runtime Policy summary displays the information that will be included on the application's listing details.

5.  When the application is installed to a new instance, ARP enforces policies that are configured to permit access. Undeclared cross-origin and cross-scope access is rejected and logged.

    **Note:** After an application built with ARP is installed, its cross-scope privileges can be modified and the update can be published to the Application Repository as an application customization. For more information about modifications to cross-scope privileges, see [Cross-scope privilege record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/c_CrossScopePrivilegeRecord.md). For more information about customizing applications, see [Manage customizations to applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-repository-self-hosted/manage-customizations-store-apps.md).


## ARP benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Limits each application to its own scope by default, so unintended access to external hosts or other application APIs must be explicitly declared and approved.|[Network policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/review-network-policy-arp.md), [Cross-Scope Privilege](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/review-cross-scope-policy-arp.md)|Custom application developers, ServiceNow Store partner developers|
|Automatically creates and approves policies in Tracking mode, so developers can build out application functionality without stopping to manually configure each access requirement.|[Tracking mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/arp-opt-in.md)|Custom application developers, ServiceNow Store partner developers|
|Prevents a single application from consuming excessive instance resources by defining quota limits for API transactions, UI transactions, and scheduled jobs.|[Quota configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/arp-quota-configurations.md)|Custom application developers, ServiceNow Store partner developers|
|Reduces the overhead of granular policy creation by letting developers define broad access patterns for an entire pillar using a single segment policy record.|[Segment policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/create-segment-policy-arp.md)|Custom application developers, ServiceNow Store partner developers|
|Enables automatic ServiceNow Store certification by conforming to variable runtime guarantees about application behavior on ServiceNow AI Platform instances|ARP policy enforcement|ServiceNow Store partner developers|
|Provides application-level cross-scope and cross-origin access information to potential customers before they obtain or install the application, improving transparency.|[ServiceNow Store application listing details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/store-listing-details.md), [Application Manager application details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/app-details-app-mgr.md)|ServiceNow AI Platform administrators|

## What to explore next

To learn more about configuring and using Application Runtime Policy, see:

-   [Configuring Application Runtime Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/configuring-app-runtime-policy.md)
-   [Using Application Runtime Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/using-arp.md)
-   [Application Runtime Policy reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-runtime-policy-reference.md)

