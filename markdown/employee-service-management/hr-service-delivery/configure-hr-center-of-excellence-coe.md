---
title: Enable or disable an HR Center of Excellence \(COE\)
description: Enable or disable an HR Center of Excellence \(COE\) for use. COEs are tables that extend the HR Case \[sn\_hr\_core\_case\] table and part of a functional discipline, such as total rewards or talent management. COEs are also part of HR services that contain topic category and detail.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR service categorization, HR Centers of Excellence data model, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Enable or disable an HR Center of Excellence \(COE\)

Enable or disable an HR Center of Excellence \(COE\) for use. COEs are tables that extend the HR Case \[sn\_hr\_core\_case\] table and part of a functional discipline, such as total rewards or talent management. COEs are also part of HR services that contain topic category and detail.

## Before you begin

Role required: sn\_hr\_core.admin

Deactivate COEs manually on all your environments, if your company:

-   Does not use COEs.
-   Wants to deactivate COEs.
-   Has multiple environments and you're using system update sets to update changes.

    **Note:** System update sets capture deactivation in one environment, but after a patch or upgrade, COEs are active in your other environments. See [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).


## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **COE Configuration**.

2.  Enable or disable the applicable HR Center of Excellence \(COE\).

    **Note:** The COEs available to you may differ depending on the HR package you have.

    -   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
    -   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](../concept/hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
    -   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
    -   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.
    ![COE Configuration page displaying a list of HR cases like "Employee Relations," "HR Benefits," and "HR Payroll," each with an adjacent toggle switch for enabling or disabling.](../image/coe-enable-disable.png)

    COEs that are not associated with any HR services, topic details, categories, or record producers are automatically disabled.

    When you disable a COE, all associated HR services are also disabled. However, the extended tables linked to that COE remain accessible and are not disabled. Any active cases under the deactivated COE will continue to remain active; only the COE itself is deactivated.

3.  Click **Save**.


**Parent Topic:**[HR service categorization](../concept/hr-service-categorization.md)

