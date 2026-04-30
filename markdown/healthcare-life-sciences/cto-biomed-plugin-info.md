---
title: Setting up plugins for Care Team Operations for Biomed
description: The Field Service Management \[com.snc.work\_management\] plugin is required for work order synchronization to function with Care Team Operations for Biomed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Care Team Operations for Biomed, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Setting up plugins for Care Team Operations for Biomed

The Field Service Management \[com.snc.work\_management\] plugin is required for work order synchronization to function with Care Team Operations for Biomed.

For Care Team Operations for Biomed to create work orders from Healthcare Biomed cases, the Field Service Management \[com.snc.work\_management\] plugin must be installed.

This plugin provides all roles and features needed for the healthcare biomed case to synchronize with work orders.

It also provides the following roles for Care Team Operations for Biomed:

-   biomed.dispatcher
-   biomed.agent
-   biomed.qualifier

**If the Field Service Management \[com.snc.work\_management\] plugin isn’t installed:**

Work orders won’t****be created from healthcare biomed cases. Instead, agents work on fulfilling those cases directly from their portals.

Cases created are assigned to assignment groups based on the requesting location associations and are configured normally with CSM case management functionality.

