---
title: Releases in ReleaseOps
description: Scheduled and on-demand releases are how changes are deployed to target instances with ReleaseOps. Releases can contain one or more deployment requests.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ReleaseOps, deploy changes, update sets, pipeline, ATF, scheduled release, custom pipeline, large scale deployment ServiceNow, schedule a release, deployment request, deployment analyzer]
breadcrumb: [Explore, ReleaseOps, Deploying applications, Building applications]
---

# Releases in ReleaseOps

Scheduled and on-demand releases are how changes are deployed to target instances with ReleaseOps. Releases can contain one or more deployment requests.

## Creating a release

Generally, a release manager is responsible for creating releases and mapping a team or organization’s release workflows to a release cadence.

There can be a single release stream or multiple release streams available at any given time. However, only one release can be in the process of deploying to a target instance at any time.

For example, an organization might have two release tracks that they define:

-   A regular weekly cadence for releases, at 10:00 each Friday.
-   A daily cadence for high-priority releases, at 12:00 each day.

The weekly and daily release tracks can coexist without issue.

For more information about creating a release, see [Create a release](../task/create-a-release.md).

## Release types

Releases that are planned and scheduled in advance are considered scheduled releases. These releases can consist of one or more deployment requests. Each deployment request in the release can include of one or more update sets.

On-demand releases are created dynamically when the need arises, such as deploying changes to patch a defect in an application. When a developer creates a deployment request and selects the option for an on-demand release, ReleaseOps dynamically creates a release to drive this request to its target instance. As a result, only one deployment request can be attached to an on-demand release.

**Important:** Changes in an on-demand release are intended to be deployed to their target as soon as possible. However, on-demand releases must still pass the checks in the organization's pipeline. Doing so helps to verify that the changes meet the requirements for the organization's compliance and governance policies, as well as quality assurance checks. Once the on-demand request has passed these checks, the deployment proceeds immediately.

ReleaseOps includes deployment analyzer, a tool provided to introspect a deployment. The deployment analyzer enables release administrators to verify that on-demand releases meet certain criteria, such as only making specific types of code changes. For more information, see [Deployment analyzer in ReleaseOps](deployment-analyzer.md).

