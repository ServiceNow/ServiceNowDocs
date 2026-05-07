---
title: Show or hide the conversation panel
description: Show or hide the conversation panel in the real-time transcription \(RTT\) interface using the rtt\_show\_conversation\_tab identity property. This feature allows the contact center providers to control the visibility of the conversation panel using the identity property.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ICC call control features, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Show or hide the conversation panel

Show or hide the conversation panel in the real-time transcription \(RTT\) interface using the **rtt\_show\_conversation\_tab** identity property. This feature allows the contact center providers to control the visibility of the conversation panel using the identity property.

## Configure and set up the conversation panel

Show or hide the conversation panel using the **rtt\_show\_conversation\_tab** property:

-   true – Displays the conversation panel
-   false – Hides the conversation panel

Follow these steps to add the property to enable or disable the conversation panel feature in your application as follows:

1.  Navigate to the provider application associated with your Interactions.
2.  Create the property**rtt\_show\_conversation\_tab**.

The **Call Transcript** tab doesn't show if the **rtt\_show\_conversation\_tab** property is false or doesn't exist.

