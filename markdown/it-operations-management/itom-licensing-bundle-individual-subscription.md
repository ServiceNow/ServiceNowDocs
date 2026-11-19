---
title: ITOM/OT SU Licensing Bundle and Individual \(ala carte\) subscription
description: You can purchase subscriptions for individual ITOM applications \(a la carte\) or as a bundle covering multiple ITOM applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-licensing-bundle-individual-subscription.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITOM/OT SU Licensing subscription types, Explore ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# ITOM/OT SU Licensing Bundle and Individual \(ala carte\) subscription

You can purchase subscriptions for individual ITOM applications \(a la carte\) or as a bundle covering multiple ITOM applications.

The ITOM/OT SU Licensing application calculates and displays the subscription usage for ITOM products. It displays the ITOM products individually or as part of a bundle, based on your subscription. Your organization can purchase ITOM subscriptions both as a bundle and individually \(a la carte\). The licensing module deducts consumed subscriptions from the bundle first, before deducting from individually purchased subscriptions.

If your organization surpasses the allocated number of subscription units, the Subscriptions window indicates the corresponding subscriptions as overdrawn. When subscriptions from both bundle and a la carte options exceed the allocation, the surplus is identified as taken from the a la carte subscription. If the total subscriptions for an application covered solely by the bundle surpass the allocation, the Subscriptions window displays the bundle as overdrawn. The individual application is not listed separately.

## Subscription deduction process: Bundle usage and a la carte scenario

If you purchased ITOM subscriptions as a bundle and acquired a la carte subscription for an application included in the bundle, subscriptions are deducted in a specific order. The licensing module deducts consumed subscriptions from the bundle first, then from the separately purchased subscriptions.

In the following example, an organization utilized all subscriptions allocated by the ITOM Pro bundle for ITOM AIOps. Subsequently, the licensing module deducted from the a la carte subscriptions for ITOM AIOps.

\[Omitted image "itom-license-summary-all.png"\] Alt text: Subscriptions window showing subscriptions consumed within bundle.

## Subscription display: Application covered by bundle and a la carte subscriptions

If your organization surpasses the total number of subscriptions in both the bundle and a la carte subscriptions, the licensing module regards it as overdrawn on the a la carte subscription. However, if your organization exceeds the subscriptions specifically for an application covered solely by the bundle, it is considered overdrawn on the bundle.

\[Omitted image "itom-license-subscr-all-diagram.png"\] Alt text: The diagram shows how the licensing module calculates bundle and a la carte subscriptions for the same ITOM applications.

## Subscription calculation illustration: Bundle and a la carte allocation

The diagram illustrates how the licensing module calculates subscriptions through bundle and a la carte methods for specific applications covered by the bundle.

\[Omitted image "itom-license-summary-some-overdraft.png"\] Alt text: Subscriptions window showing overdrafts on the bundle and a la carte subscriptions.

In this scenario, the Subscriptions window indicates the a la carte subscriptions for this application as overdrawn. If your organization exceeds the total subscriptions for an application covered solely by the bundle, the Subscriptions window displays the bundle as overdrawn.

In the provided figure, ITOM AIOps consumed 860 subscriptions, surpassing the subscriptions provided by the bundle \(500\) and a la carte \(250\). Consequently, the Subscriptions window indicates the ITOM AIOps a la carte subscription as overdrawn.

For ITOM Visibility, which consumed 550 subscriptions, and with no a la carte subscriptions purchased, the ITOM Pro bundle covering ITOM Visibility appears as overdrawn.

