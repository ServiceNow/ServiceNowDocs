---
title: Model categories
description: Model categories define relationships between asset classes, product model classes, and Configuration Management Database \(CMDB\) configuration item \(CI\) classes in the Enterprise Asset Management application.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Model categories

Model categories define relationships between asset classes, product model classes, and Configuration Management Database \(CMDB\) configuration item \(CI\) classes in the Enterprise Asset Management application.

Each model category is divided into sub-categories that correspond to a model class, an asset class, and an existing CMDB CI class. Multiple model categories can be assigned to a single model class and a single asset class. A CI class can be assigned to only a single model category. However, it is not mandatory to assign a CI class to a model category.

![Model category](../image/modelcategory.png)

Various base model categories are available for you to choose from. The top tier model categories are as follows:

-   Medical
-   Facility
-   Transportation
-   Industrial
-   Retail
-   Construction
-   Tactical equipment
-   Wearable
-   Multimedia production equipment

For the complete list of available model categories and their corresponding CMDB CI, asset, and model classes, see [Enterprise model categories and corresponding classes](../reference/enterprise-model-categories.md).

**Note:** If you do not wish to use any of the existing sub-categories within a top tier model category, you can create your own sub-categories. See [Create model categories](../task/create-custom-model-category.md) for detailed instructions.

**Warning:** ServiceNow strongly recommends that you use only the existing top tier model categories.

