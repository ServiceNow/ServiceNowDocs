---
title: Limitations in GCC-H or DoD for Microsoft Teams integration with Virtual Agent
description: Learn about the limitations for Microsoft Teams Government Community Cloud - High \(GCC-H\) or the US Department of Defense \(DoD\) Microsoft Teams integration with Virtual Agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate VA with MS Teams for GCC-H, Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Limitations in GCC-Hor DoD for Microsoft Teams integration with Virtual Agent

Learn about the limitations for Microsoft Teams Government Community Cloud - High \(GCC-H\) or the US Department of Defense \(DoD\)Microsoft Teams integration with Virtual Agent.

## Limitations

1.  **Manifest version**: Up to v1.10. Ensure that the template that you create has version 1.10 or an earlier version.
2.  **Adaptive Cards**: Enable the **sn\_va\_teams.send\_image\_as\_data** system property to upload images to your conversation on Microsoft Teams that is integrated with GCC-High. Apply this system property to image and card controls. If you're using an image URL, ensure that its source is a ServiceNow instance.

**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD](../concept/va-integ-msteams-gcch.md)

