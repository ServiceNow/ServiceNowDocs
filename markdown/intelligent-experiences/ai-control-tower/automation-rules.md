---
title: Automation rules
description: The Automation rules define how AI assets are set to be under managed assets.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 1
breadcrumb: [Configurations, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Automation rules

The Automation rules define how AI assets are set to be under managed assets.

## Automation rules Overview

The Automation rules page displays all default rules available in AI Control Tower. The AI Stewards can modify the existing rules or create rules based on their organizational requirements.

## Rule limits

The Administrators can configure system-enforced limits on asset management rules through system properties. The recommended defaults are 5 active rules and 10 total rules, controlled by the following system properties:

|System properties|description|
|-----------------|-----------|
|sn\_ai\_governance.management\_rule.max\_active\_rules|Max active rules|
|sn\_ai\_governance.management\_rule.max\_total\_rules|Max total rules|

## Rules execution

Only active rules are evaluated during scheduled runs; inactive rules are skipped. The scheduled job 'Run AI Asset Management Rules’ is executed for every 6 hours, but AI stewards can trigger immediate execution on any active rule using the **Run Now** action. Rules that are no longer needed can be deleted. If an asset is qualified for a rule, it will be automatically moved under managed assets.

## References

For information on managed and unmanaged assets, see [Assets list- managed and unmanaged assets](../task/assets-list-managing-and-unmanaging-assets.md)

For information on creating rules, see [Create an Automation rule](../task/create-automation-rules.md)

