---
title: Configure Autonomous Engineer
description: Configure Autonomous Engineer by installing it from the ServiceNow Store and enabling the features required for planning and parallel execution on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/configure-autonomous-engineer.html
release: australia
topic_type: concept
last_updated: "2026-11-09"
reading_time_minutes: 1
keywords: [Autonomous Engineer, Build Agent, configure, install, agent packs, ServiceNow Studio, setup]
audience: programmer
breadcrumb: [Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Configure Autonomous Engineer

Configure Autonomous Engineer by installing it from the ServiceNow Store and enabling the features required for planning and parallel execution on your instance.

Autonomous Engineer is a separate application available in the ServiceNow Store. Installing Autonomous Engineer also installs Build Agent as a dependency. Configuring Autonomous Engineer involves installing the application and confirming the required roles and permissions.

## Prerequisites

Before configuring Autonomous Engineer, verify the following:

-   Autonomous Engineer is installed on your instance. For installation instructions, see [Install Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-autonomous-engineer.md).
-   You have the admin role.

## Installation

For installation steps, see [Install Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-autonomous-engineer.md).

## Agent packs

Autonomous Engineer uses agent packs with platform knowledge to run implementations. You don't install agent packs. They ship as part of each release, and Autonomous Engineer activates the right pack when it needs it. For more information, see [Agent packs for Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

-   **[Install Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-autonomous-engineer.md)**  
Install Autonomous Engineer from the ServiceNow Store to make it available on your instance.
-   **[Configuring Autonomous Engineer settings in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ae-settings.md)**  
Autonomous Engineer and Build Agent share the same configuration settings. Settings you configure for Build Agent also apply when Autonomous Engineer runs.

**Parent Topic:**[Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer.md)

