---
title: ITOM/OT SU Licensing Bundle and Individual \(ala carte\) subscription
description: You can purchase subscriptions for individual ITOM applications \(a la carte\) or as a bundle covering multiple ITOM applications.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ITOM/OT SU Licensing subscription types, Exploring ITOM/OT SU Licensing, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# ITOM/OT SU Licensing Bundle and Individual \(ala carte\) subscription

You can purchase subscriptions for individual ITOM applications \(a la carte\) or as a bundle covering multiple ITOM applications.

The ITOM/OT SU Licensing application calculates and displays the subscription usage for ITOM products. It displays the ITOM products individually or as part of a bundle, based on your subscription. In cases where your organization has purchased ITOM subscriptions both as a bundle and individually \(a la carte\), the licensing module deducts the consumed subscriptions from the bundle first, before deducting from the individually purchased subscriptions.

If your organization surpasses the allocated number of subscription units, the Subscriptions window indicates the corresponding subscriptions as overdrawn. If the combined number of subscriptions from both bundle and a la carte options exceeds the allocation, the licensing module identifies the surplus as taken from the a la carte subscription. Furthermore, if the total subscriptions for an application covered solely by the bundle surpass the allocation, the Subscriptions window displays the bundle as overdrawn without listing the individual application separately.

## Subscription deduction process: Bundle usage and a la carte scenario

If you purchased ITOM subscriptions as a bundle and also acquired a la carte subscriptions for an application included in the bundle, the licensing module deducts the consumed subscriptions from the bundle before subtracting from the separately purchased subscriptions.

In the following example, an organization utilized all subscriptions allocated by the ITOM Pro bundle for ITOM Health. Subsequently, the licensing module deducted from the a la carte subscriptions for ITOM Health.

![Subscriptions window showing subscriptions consumed within bundle.](../image/itom-license-summary-all.png "Subscription consumption by bundles")

## Subscription display: Application covered by bundle and a la carte subscriptions

If your organization surpasses the total number of subscriptions in both the bundle and a la carte subscriptions, the licensing module regards it as overdrawn on the a la carte subscription. However, if your organization exceeds the subscriptions specifically for an application covered solely by the bundle, it is considered overdrawn on the bundle.

![The diagram shows how the licensing module calculates bundle and a la carte subscriptions for the same ITOM applications.](../image/itom-license-subscr-all-diagram.png "Licensing module calculates bundle and a la carte subscriptions for the same ITOM applications")

## Subscription calculation illustration: Bundle and a la carte allocation

The diagram illustrates how the licensing module calculates subscriptions through bundle and a la carte methods for specific applications covered by the bundle.

![Subscriptions window showing overdrafts on the bundle and a la carte subscriptions.](../image/itom-license-summary-some-overdraft.png "Overdrafts on the bundle and a la carte subscriptions")

In this scenario, the Subscriptions window indicates the a la carte subscriptions for this application as overdrawn. If your organization exceeds the total subscriptions for an application covered solely by the bundle, the Subscriptions window displays the bundle as overdrawn.

In the provided figure, ITOM Health consumed 810 subscriptions, surpassing the subscriptions provided by the bundle \(500\) and a la carte \(250\). Consequently, the Subscriptions window indicates the ITOM Health a la carte subscription as overdrawn.

For ITOM Visibility, which consumed 550 subscriptions, and with no a la carte subscriptions purchased, the ITOM Pro bundle covering ITOM Visibility appears as overdrawn.

