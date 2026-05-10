---
title: Explore HR Multi Instance Integration
description: Learn about the benefits and key offerings of the HR Multi Instance Integration application.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Explore HR Multi Instance Integration

Learn about the benefits and key offerings of the HR Multi Instance Integration application.

## HR Multi Instance Integration overview

Partners and service providers for HR service fulfillment often are running their own instance of HR Service Delivery. HR Multi Instance Integration provides inter-instance communication and uniform HR service experiences \(for remote HR services and local HR services\) with fulfillment in different instances through the following capabilities:

-   Ability to control your organization employee’s experience according to your organization's culture, branding, and policies.
-   Ability to outsource services.
-   Consistent user experience for employees across the entire HR catalog, regardless of whether they are interacting locally or remotely from any third-party provider.
-   Because HR workflows or business process are not restricted to a single instance, they can flow seamlessly across instances. Ability to fulfill a case partially by providers and partially by consumers.
-   Uniformity and standardization for HR agents on the provider instance enables them to work on local cases or remote HR cases from the provider’s ServiceNow AI Platform instance with a minimal learning curve.
-   Managing and controlling access at the remote catalog level to meet security and compliance requirements at both the provider and consumer instances.
-   Synchronization of relevant information such as submitted request \(provider task\) status, comments, and attachments by service providers.
-   Use Universal Task as the remote tasking medium in consumer instance.
-   Ability to create HR tasks and approval tasks for remote cases.
-   Initiate document signing tasks for remote users via universal tasks.

**Note:** HR Multi Instance Integration is dependent on the following plugins:

-   [Service Bridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/tmt-service-bridge-both-landing-page.md)
-   [Human Resources Scoped App: Core](../reference/case-knowledge-management-landing-page.md)

## HR Multi Instance Integration users

<table id="table_etz_brt_cdc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider administrator

</td><td>

-   Can register customers in a provider instance.
-   Can create and publish remote catalogs in a provider instance.
-   Can view records in transport queue in a provider instance.
-   Can [Enable magic links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-magic-links.md) to let consumer users complete assigned tasks from provider instance.

</td></tr><tr><td>

HR agent or Provider agent

</td><td>

-   Can differentiate remote cases from local cases and work on it for basic case fulfillment in a provider instance.
-   Can create HR tasks, approval tasks, and document tasks for consumer users.
-   Can interact with consumer users via comments, attachments, and track state changes on the remote HR case on a provider instance.

</td></tr></tbody>
</table><table id="table_mv4_2ds_b2c"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Consumer administrator

</td><td>

-   Can register providers in a consumer instance.
-   Can subscribe to remote catalogs from external service provider.
-   Can activate catalogs to enable consumer employee to raise a request from consumer instance to provider instance.
-   Can view records in a transport queue in a consumer instance.
-   Can configure the value of the **Redirect timeout** option in the magic links settings.

</td></tr><tr><td>

Consumer employee

</td><td>

-   Can access and submit service requests from a consumer employee portal.
-   Can complete the HR tasks, approval tasks, and document tasks via the URL links in assigned tasks.

</td></tr></tbody>
</table>## HR Multi Instance Integration workflow

The following graphic explains how an HR service request is partially fulfilled by providers and partially fulfilled by consumers.

![Infographic explaining how an HR service request is partially fulfilled by providers and partially by consumers.](../image/hr-mii-flow.png "Flow")

## HR Multi Instance Integration benefits

|Benefit|Users|
|-------|-----|
|HR workflows or business process are not restricted to single instance and can flow seamlessly across instances for fulfillment.|Provider|
|Restrict only users with specific roles to view records in provider instance.|Provider administrator|
|Uniformity and standardization for HR agents on the provider instance enables them to work on local cases or remote HR cases from the provider’s ServiceNow AI Platform instance with a minimal learning curve.|Provider agent|
|Create HR tasks, approval tasks, and document tasks for remote users.|Provider agent|

<table id="table_zrt_hds_b2c"><thead><tr><th>

Benefit

</th><th>

Users

</th></tr></thead><tbody><tr><td>

No need to maintain in-house expertise or agents for outsourced services \(redundant and transactional in nature\).

</td><td>

Consumer

</td></tr><tr><td>

HR workflows or business process are not restricted to single instance and can flow seamlessly across instances for fulfillment.

</td><td>

Consumer

</td></tr><tr><td>

Restrict only users with specific roles to view records in consumer instance.

</td><td>

Consumer administrator

</td></tr><tr><td>

Consistent user experience for employees across the entire HR catalog, regardless of whether they are interacting locally or remotely from any third-party provider.Place a request via an HR catalog from a consumer instance and fulfill the request from a provider instance.

Complete HR tasks, approval tasks, and document tasks, if any, via magic links.

</td><td>

Consumer employee

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using HR Multi Instance Integration, see:

-   [Configuring HR Multi Instance Integration](config-hr-mii-bs.md)
-   [Using HR Multi Instance Integration](using-hr-mii.md)
-   [Reference for HR Multi Instance Integration](../reference/reference-hr-multi-instance.md#)

