---
title: Configure HR Multi Instance Integration for Provider
description: Plan and implement the configuration of HR Multi Instance Integration for Provider.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Configure HR Multi Instance Integration for Provider

Plan and implement the configuration of HR Multi Instance Integration for Provider.

## Configuration overview

1.  Activate the HR Multi Instance Integration for Provider application from ServiceNow Store, which installs the following plugins:
    -   HR Multi Instance Integration Base
    -   Service Bridge for Provider
    -   Human Resources Scoped App: Core

        **Note:** In addition, you can also install ServiceNow Agent workspace for HR case management to enable agents to work on HR cases in provider instance.

2.  Configure HR Multi Instance Integration for Provider by performing the following steps:
    1.  Register a service bridge consumer. A company or account must exist for the consumer in the provider instance and user must be associated with the company. If you want to enable domain separation, you must associate a domain to the company. For more information, see [Register a Service Exchange consumer](https://www.servicenow.com/docs/access?context=service-bridge-v2-onboarding&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

        **Note:** Import users from a consumer instance into the provider instance before registering a service bridge consumer. For more information, see [Import users](import-users-hr-mii.md).

    2.  Create a remote record producer and publish it. For more information, see [Remote catalogs](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-apps&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

        **Note:**

        -   You can create remote record producers only if you have provider administrator \[sn\_hr\_mii\_provider\] role along with a delegated\_developer role.
        -   Create a remote record producer under the HR Multi Instance Integration Base scope so that the catalogs are available on the consumer instance. After you revise a remote record producer, you must update the value in the **Record producer** field in HR service.
        -   When creating remote record producers, select the flow **Create HR case from provider task**. This step is required for auto- creating an HR case from a provider task when the remote record producer is triggered.
    3.  [Enable magic links](https://www.servicenow.com/docs/access?context=service-bridge-v2-magic-links&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US) to let consumer users complete assigned tasks from provider instance. Magic links enable consumer users to directly access the linked resource in the provider instance without having to manually log in.
    4.  Configure an HR service to trigger a case when the remote record producer is triggered. When you create an HR service, select the configured remote record producer in the **Record producer** field. See [Configure an HR service](configure-hr-service.md).

