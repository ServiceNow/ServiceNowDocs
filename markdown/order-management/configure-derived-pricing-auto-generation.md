---
title: Disable auto-generation of derived pricing lines
description: Disable automatic addition of derived product lines to quotes when sellers manage these lines manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-derived-pricing-auto-generation.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [derived pricing]
breadcrumb: [Configuring derived pricing, Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Disable auto-generation of derived pricing lines

Disable automatic addition of derived product lines to quotes when sellers manage these lines manually.

## Before you begin

Role required: admin

Starting with Pricing Management application version 18.0.3, the pricing engine automatically adds derived product lines to quotes during pricing initialization by default. Disable this feature only if sellers manage derived product lines manually. When disabled, sellers must add each derived product line and align its start and end dates with the source lines. The pricing engine excludes derived lines whose dates don't align with their source lines.

To disable automatic addition, add the **sn\_csm\_pricing.auto\_add\_target\_lines** property in the System Properties \[sys\_properties\] table and set its value to `false`. For instructions, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Warning:** Decide whether sellers add derived product lines automatically or manually during implementation. After sellers start adding these lines manually, don't set the **sn\_csm\_pricing.auto\_add\_target\_lines** property back to `true`. The pricing engine can't reconcile manually added lines with its automatic date alignment, so it can change the dates on existing derived product lines or remove them.

## Result

The pricing engine applies the updated settings on the next pricing transaction.

