---
title: Configure automatic updates for entity owner and class
description: Configure an entity filter to automatically update entity owner and class when source data changes or an entity moves between filters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/configure-automatic-updates-for-entity-owner-and-entity-class.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Entity filters, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Configure automatic updates for entity owner and class

Configure an entity filter to automatically update entity owner and class when source data changes or an entity moves between filters.

## Before you begin

Role required: sn\_grc.manager or sn\_grc.library\_manager

## About this task

Entity owner and entity class are derived from the configuration defined on an entity filter. When automatic updates are enabled, the system re-evaluates the owner and class when source record changes or entity filter membership changes affect an entity.

If multiple entity filters can derive owner and class values for the same entity, you can designate a filter as **Preferred for owner and class derivation**.

## Procedure

1.  In the filter navigator, search for **Entity Types** and select it from the results.

    Entity Types is available under Scoping in each GRC application module, such as Audit, Policy and Compliance, Advanced Risk Assessment, and Risk.

2.  Open the entity type that contains the entity filter that you want to configure.

3.  In the **Entity Filters** related list, open the entity filter.

4.  Select the **Assignment** tab.

5.  Select **Auto-update owner**.

6.  Configure the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Derive owner from source field|Uses a field on the source record to determine the entity owner.|
    |Source field for owner|Specifies the source record field that contains the owner value.|
    |Preferred for owner and class derivation|Marks the entity filter as preferred when deriving owner and class values for an entity that matches multiple filters.|
    |Empty owner|Specifies the action to take when no owner value is returned from the configured source field, such as using the default owner or skipping entity creation.|

7.  Select **Update**.


## Result

The system automatically re-evaluates and updates the entity owner and entity class when source record changes or entity filter membership changes affect the entity.

**Parent Topic:**[Entity filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/what-is-an-entity-filter.md)

