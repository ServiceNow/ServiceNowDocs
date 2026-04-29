---
title: Post-Production Domain Separation Activation Utility
description: The post-production Domain Separation activation utility aids in the activation of Domain Separation in a live environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup and administration, Domain separation for service providers, Access Management]
---

# Post-Production Domain Separation Activation Utility

The post-production Domain Separation activation utility aids in the activation of Domain Separation in a live environment.

## Post-Production Domain Separation Activation Utility plugin

The Post-Production Domain Separation Activation Utility plugin \(com.glide.domain.activation\_utility\) simplifies the task of creating a domain-separated environment in a post production live environment. Customers may want to activate Domain Separation on post production environments to take greater advantage of the ServiceNow AI Platform capabilities. The utility provides a step-by-step guided setup for creating domains.

**Note:** The process of populating domain records in domain separated tables requires downtime or restricted access to the instance.

## What the Activation utility does

-   Provides a step-by-step guided setup for creating domains.
-   Runs a background job to handle the installation of domain separation with both Process and Data Separation properties disabled.
-   Keeps process records that are visible to the target\(first\) domain
-   Detects, identifies, and logs errors during the domain creation process
-   Presents resolutions for common errors
-   Logs all actions performed during the setup process for audit purposes
-   Generates a detailed summary, including all actions taken, domains created, and any changes made to the syste

