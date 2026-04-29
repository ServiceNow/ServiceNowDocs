---
title: Managing multiple releases through release bundles
description: Release bundles help you to group multiple releases to track and manage them concurrently from a single place.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Managing multiple releases through release bundles

Release bundles help you to group multiple releases to track and manage them concurrently from a single place.

Release coordinators and product managers can easily track the progress of each release using release bundles. Release bundles help to identify dependencies and potential conflicts, and make any necessary adjustments to ensure a smooth and coordinated release process. They also enable communication and collaboration among team members, as everyone can access the same information and stay updated on the status of each release.

**Note:** You cannot add releases that are in the Draft state to a release bundle.

You can include a release in multiple release bundles, which can be useful for larger projects. It can help in better coordination between multiple teams working on different features. It can also help with managing and prioritizing updates.

## State of a release bundle

The **State** field shows the overall state of the release bundle, which is determined by the states of its releases, as mentioned below:

-   Draft: When there are no releases in the bundle.
-   Ready: When all releases are either in the Pending or Draft state.
-   In Progress: When at least one release is in the In Progress, Review, or Restarting state, or when there's a combination of Draft and Completed states among the releases.
-   Completed: When all releases have either the Completed or Cancelled state. For the Completed release bundle, the Active is set to false.

## Features and benefits

Release bundles offer the following features and benefits:

-   **Centralized management**

    Provides release coordinators and project managers to manage multiple releases concurrently from one place.

-   **Progress and quality monitoring**

    Monitor progress of releases across multiple teams and projects and ensure the quality of releases within the bundle.

-   **Change request tracking**

    Track all change requests in releases.


-   **[Create a release bundle](../task/dpr-create-release-bundle.md)**  
Create a release bundle to manage and track multiple releases from a single place. These releases can have different release readiness targets. However grouping them together in bundles helps you manage them all efficiently.
-   **[Track multiple releases from a release bundle](../task/dpr-track-release-bundle.md)**  
Track the progress of releases in a release bundle concurrently to improve efficiency and streamline the release management process. You can also identify dependencies and potential conflicts in your releases and coordinate with team members working on different releases.

**Parent Topic:**[Manage releases for digital products and services](../task/dpr-manage-releases.md)

