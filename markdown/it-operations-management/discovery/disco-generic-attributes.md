---
title: Discovery generic attributes
description: Discovery generic attributes enable you to define custom attributes at the schedule, range, and range set level. These attributes attach metadata that can influence CMDB field population and Discovery runtime behavior, providing granular control based on the scope of the discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery generic attributes

Discovery generic attributes enable you to define custom attributes at the schedule, range, and range set level. These attributes attach metadata that can influence CMDB field population and Discovery runtime behavior, providing granular control based on the scope of the discovery.

## How it works

Discovery generic attributes use a declarative, rule-based approach for applying metadata during Discovery. Each attribute defines a scope, action, target, and value. You can attach attributes at different levels of the Discovery hierarchy to control how metadata is applied. When attributes exist at multiple scope levels, Discovery applies them using a precedence hierarchy. Attributes defined at a more specific scope take precedence over those at a broader scope. This hierarchy enables you to set default attribute values at a broad level while overriding them for specific scopes where different values are needed.

## Attribute scope hierarchy

Discovery reconciles attributes from multiple scope levels by applying a precedence order. Attributes at a more specific scope override attributes with the same key at a broader scope. The available scope levels and their precedence depend on the use case. For more information, see [Automatic CI field population](ci-field-disco-attributes.md).

## Use case

You can use Discovery generic attributes to automatically populate CI fields based on the Discovery scope. This enables you to apply consistent metadata to discovered CIs without manual intervention. For more information, see [Define CI field attributes](../task/define-ci-attributes.md).

