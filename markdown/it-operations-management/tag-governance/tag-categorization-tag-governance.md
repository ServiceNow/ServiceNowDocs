---
title: Tag Categorization in Tag Governance
description: By automatically grouping similar tag keys into predefined categories, Tag Categorization streamlines the management of configuration items \(CIs\) and cloud resources while promoting clear and consistent tagging practices.
locale: en-US
release: yokohama
product: Tag Governance
classification: tag-governance
topic_type: concept
last_updated: "2025-06-23"
reading_time_minutes: 2
breadcrumb: [Exploring Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Tag Categorization in Tag Governance

By automatically grouping similar tag keys into predefined categories, Tag Categorization streamlines the management of configuration items \(CIs\) and cloud resources while promoting clear and consistent tagging practices.

## Tag categorization requirements

**Note:**

The Tag Categorization feature in Tag Governance leverages the CI tag category \[svc\_tag\_categories\] and the CI tag key \[svc\_tag\_names\] tables in Service Mapping. Full access to these tables requires installation of the version 1.16.3 or later of Service Mapping Plus. Without it, access to these tables might be limited, affecting your ability to recategorize tags, modify tag definitions, or fully use the feature. For more information, see [Install Service Mapping Plus](../../service-mapping/task/install-service-mapping-plus.md).

## Tag Categorization overview

Tag Categorization helps streamline and improve the accuracy of tag management by providing preconfigured categories to help you group tags for your CIs. A daily scheduled job categorizes newly added tags and maps any unrecognized tag keys to the appropriate category. For more information about the predefined tag categories, see [Components installed with Tag Governance](../reference/components-installed-tag-governance.md).

You can modify the tag category definitions, create your own categories, or add additional tag keys as needed. For more information, see [Modify tag category information for Tag Categorization](../task/modify-tag-category-info-tag-categorization.md).

The Tag category policy confirms that all categories are properly mapped and up-to-date. It retrieves records and checks for category mappings to identify any missing categories. CIs that are missing a category are marked as non-compliant, which helps you address and remediate any tag category issues.

The system uses the **sn\_itom\_tag.recategorization\_required** property to determine whether recategorization is needed. By default, this property is set to false, but when a change to a category occurs, a business rule sets the property to true, indicating that recategorization is needed. A daily scheduled job then checks this property and if it is set to true, begins the recategorization process. This process automatically updates the tag mappings within 24 hours of the change, but you can also initiate recategorization to apply the changes immediately. All changes and updates are stored in the CI tag category table.

## Tag Categorization and domain separation

Tag Categorization supports domain-specific management. If an instance isn’t domain-separated, the categories are added to the global domain. For domain-separated instances, the categories are added to each leaf domain. When you access or manage tags, the system gets domain information from the CI and adds tag mappings to the matching category in the appropriate domain. For general information about domain separation with Tag Governance, see [Domain separation and Tag Governance](tag-governance-domain-separation.md).

