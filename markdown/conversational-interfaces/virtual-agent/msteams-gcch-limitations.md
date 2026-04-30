---
title: Limitations in GCC-H or DoD for Microsoft Teams integration with Virtual Agent
description: Learn about the limitations for Microsoft Teams Government Community Cloud - High \(GCC-H\) or the US Department of Defense \(DoD\) Microsoft Teams integration with Virtual Agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD, Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Limitations in GCC-Hor DoD for Microsoft Teams integration with Virtual Agent

Learn about the limitations for Microsoft Teams Government Community Cloud - High \(GCC-H\) or the US Department of Defense \(DoD\)Microsoft Teams integration with Virtual Agent.

## Limitations

1.  **Manifest version**: Up to v1.10. Ensure that the template that you create has version 1.10 or an earlier version.
2.  **Adaptive Cards**: Enable the **sn\_va\_teams.send\_image\_as\_data** system property to upload images to your conversation on Microsoft Teams that is integrated with GCC-High. Apply this system property to image and card controls. If you're using an image URL, ensure that its source is a ServiceNow instance.

