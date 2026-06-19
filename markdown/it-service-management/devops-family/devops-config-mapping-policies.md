---
title: Mapping policies in DevOps Config
description: Mapping a policy to a deployable enables you to validate updates on it. These policies in DevOps Config are powered by Policy as Code Engine \(PaCE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-family/devops-config-mapping-policies.html
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring DevOps Config, DevOps Config, IT Service Management]
---

# Mapping policies in DevOps Config

Mapping a policy to a deployable enables you to validate updates on it. These policies in DevOps Config are powered by Policy as Code Engine \(PaCE\).

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

After you create a policy, you can map it to a deployable to invoke the policy when any changes are made to the deployable. You can map policies using the following mappings:

-   **Static mapping**

    In static mapping, a policy is directly mapped to deployables. This mapping type helps you to apply policies to different environments or configurations. However, if you have to map a policy to multiple deployables, you would have to do it multiple times for each deployable. Validation is triggered on directly mapped policies for a deployable.

-   **Dynamic mapping**

    In dynamic mapping, a policy is mapped to deployables dynamically based on pre-defined conditions. This mapping type helps you to apply policies to a larger set of deployables across multiple applications that all meet the same conditions. Validation is triggered on dynamically mapped policies at run time for a deployable.


You can view all policies mapped to deployables of an application by selecting the **View mapped policies** option on the **Policies** tab on the Application form. Select a deployable from the list to view policies mapped to it using both static mapping or dynamic mapping.

\[Omitted image "cdm-app-policies-tab.png"\] Alt text: Policies tab on the Application form to view all mappings and manage static mappings.

-   **[Map policies to a deployable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/cdm-deployable-map-policy-to.md)**  
Map policies to a deployable to define the validation processes that the config data must pass.You can map policies to a deployable using static mapping or dynamic mapping.

**Parent Topic:**[Configuring DevOps Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-family/setting-up-devops-config-validation.md)

