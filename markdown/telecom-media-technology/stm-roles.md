---
title: Roles installed with Service Test Management
description: Review the roles that Service Test Management installs, what each role can access, and the roles that each one contains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/stm-roles.html
release: australia
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 1
keywords: [service test management roles, test\_def\_creator, test\_def\_manager, permissions]
breadcrumb: [Getting started with Service Test Management, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Roles installed with Service Test Management

Review the roles that Service Test Management installs, what each role can access, and the roles that each one contains.

## Roles for test results

These roles apply to test runs, test measures, threshold rule violations, and applied consequences.

|Role|Access|Contains|
|----|------|--------|
|sn\_st\_mgmt.test\_viewer|Read test runs, test measures, threshold rule violations, and applied consequences.|None|
|sn\_st\_mgmt.test\_writer|Write the same tables.|sn\_st\_mgmt.test\_viewer|
|sn\_st\_mgmt.test\_creator|Create records in the same tables.|sn\_st\_mgmt.test\_viewer, sn\_st\_mgmt.test\_def\_viewer|
|sn\_st\_mgmt.test\_delete|Delete records in the same tables.|None|
|sn\_st\_mgmt.test\_manager|Create, write, and delete tests.|sn\_st\_mgmt.test\_creator, sn\_st\_mgmt.test\_delete, sn\_st\_mgmt.test\_writer|

## Roles for test definitions

These roles apply to test definitions, threshold rules, and measure consequences.

|Role|Access|Contains|
|----|------|--------|
|sn\_st\_mgmt.test\_def\_viewer|Read test definitions, threshold rules, and measure consequences.|None|
|sn\_st\_mgmt.test\_def\_writer|Write the same tables.|sn\_st\_mgmt.test\_def\_viewer|
|sn\_st\_mgmt.test\_def\_creator|Create records in the same tables. Creates test definitions and test groups.|sn\_st\_mgmt.test\_def\_viewer|
|sn\_st\_mgmt.test\_def\_manager|Create and write test definitions. Publish, retire, archive, and copy test definitions. Publish and retire test groups.|sn\_st\_mgmt.test\_def\_creator, sn\_st\_mgmt.test\_def\_writer|

**Related topics**  


[Exploring Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-explore.md)

