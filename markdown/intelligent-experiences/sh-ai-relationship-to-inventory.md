---
title: How Shadow AI fits with your AI asset inventory
description: Learn why detected AI services are kept separate from your governed AI asset inventory, and how you can manage them in Shadow AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-relationship-to-inventory.html
release: australia
topic_type: concept
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [inventory, asset list, Shadow AI]
breadcrumb: [Explore, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# How Shadow AI fits with your AI asset inventory

Learn why detected AI services are kept separate from your governed AI asset inventory, and how you can manage them in Shadow AI.

AI assets in the AI assets inventory are meant to be clean, trusted records. Each AI asset in the inventory is a governed asset record that your organization has deliberately onboarded through a connector. AI services detected by Shadow AI are kept separate from that list on purpose.

## Keeping detected AI services apart from the AI asset inventory

Shadow AI uses multiple detection methods, including Armis and Agent Client Collector \(ACC\), to populate detected AI services in Shadow AI tables. An AI steward configures service graph and trace connectors to discover AI assets meant for governance and review and populates the inventory with them. Keeping the two parts of the inventory separate means unreviewed AI services won't mix with the AI assets that your organization already trusts and manages. This division keeps the AI asset inventory a collection of records that you can rely on during an audit or a governance review.

## How AI assets and Shadow AI differ

|AI Assets|Shadow AI|
|---------|---------|
|Populated by governed connectors you set up and approve|Populated automatically by Shadow AI detection methods including Armis and ACC detection|
|Contains AI systems your organization has already reviewed and manages|Contains AI systems detected automatically, pending your review|

