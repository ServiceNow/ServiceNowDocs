---
title: Entity owner and class derivation behavior
description: Entity owner and entity class derivation settings determine how the system selects owner and class values when one or more entity filters apply to an entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/entity-owner-and-class-derivation-behavior.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-09-02"
reading_time_minutes: 2
breadcrumb: [Entity filters, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity owner and class derivation behavior

Entity owner and entity class derivation settings determine how the system selects owner and class values when one or more entity filters apply to an entity.

|Scenario|Result|
|--------|------|
|An entity matches a single entity filter.|The entity owner and entity class are derived from that entity filter.|
|An entity matches multiple entity filters and no filters are marked as preferred.|The entity owner and entity class are derived based on the entity filter with the highest precedence.|
|An entity matches one preferred entity filter and one or more non-preferred entity filters.|The preferred entity filter takes precedence.|
|An entity matches multiple preferred entity filters.|The preferred entity filter created first takes precedence.|

|Field|Description|
|-----|-----------|
|Auto-update owner|Automatically updates the entity owner and entity class when source record changes or entity filter membership changes affect an entity.|
|Derive owner from source field|Uses a field on the source record to determine the entity owner.|
|Source field for owner|Specifies the source record field that contains the owner value.|
|Preferred for owner and class derivation|Marks an entity filter as preferred when deriving owner and class values.|
|Empty owner|Specifies the action to take when no owner value is returned from the configured source field.|

|Event|Result|
|-----|------|
|Source record values change.|The system re-evaluates the entity owner and entity class.|
|An entity no longer matches an entity filter.|The system re-evaluates the applicable derivation source.|
|An entity begins matching another entity filter.|The system re-evaluates the entity owner and entity class.|
|Entity filter configuration changes are applied.|The system re-evaluates the entity owner and entity class for affected entities.|

**Parent Topic:**[Entity filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/what-is-an-entity-filter.md)

**Related topics**  


[Entity filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/what-is-an-entity-filter.md)

[Configure automatic updates for entity owner and class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-automatic-updates-for-entity-owner-and-entity-class.md)

