---
title: Integration Hub subscription notifications
description: Integration Hub displays an information message whenever you use a spoke, protocol, entitlement, or feature that requires an Integration Hub subscription. You can use this information to identify possible gaps between your planned Integration Hub usage and your current subscription entitlements.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Request Integration Hub, Configure, Integration Hub, Workflow Data Fabric]
---

# Integration Hub subscription notifications

Integration Hub displays an information message whenever you use a spoke, protocol, entitlement, or feature that requires an Integration Hub subscription. You can use this information to identify possible gaps between your planned Integration Hub usage and your current subscription entitlements.

Subscription notifications do not restrict you from using any Integration Hub spoke, protocol, entitlement, or feature. Unlicensed features may be unavailable on your production instance.

## Subscription information available

Your instance attempts to access your Integration Hub subscription information online. When this information is available, the system displays an information message whenever you use a feature not included in your subscription. Flows and action titles also display an information icon for further details. Select the information icon to see a list of features not included in your subscription.

![Information message displaying, "This flow uses features that are not included in your Integration Hub subscription." There is a link to Learn More following the message.](../images/ih-subscription-info-msg.png "Sample subscription notification")

![Information message that says, "This flow uses features that are not included in your Integration Hub subscription." The Install Application With ID and the Wait Until Tracker Completes features are listed.](../images/ih-subscription-info-msg-list.png "Sample subscription notification with list of features")

## Subscription information unknown

When your instance cannot access your subscription information, it displays generic information messages. Whenever you use a feature that requires an Integration Hub subscription, the system displays a reminder information message. Verify that you have an appropriate Integration Hub subscription for the features you want to use.

**Parent Topic:**[Request Integration Hub](../../flow-designer/concept/request-ih-overview.md)

