---
title: Creating, testing, and moving customizations
description: Use these procedures to create, test, and move customizations from a development system to a production system.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer system update sets, System update sets, Deploying applications, Building applications]
---

# Creating, testing, and moving customizations

Use these procedures to create, test, and move customizations from a development system to a production system.

## Three-step import process

A common process for developing customizations with update sets involves moving changes from development, to test, to production instances.

1.  Create an update set on the development instance.
2.  Make customizations and changes on the development instance.
3.  Mark the update set as Complete.
4.  Log in to the test instance and retrieve the completed update set from the development instance.
5.  Commit the update set on the test instance, and test customizations thoroughly.
6.  If the update set has problems in the test instance, repeat steps 1 - 5 to develop the fix on the development instance with another update set.
7.  Identify a common path for update sets to move from instance to instance and maintain that model. Never migrate the same update set from multiple sources. Move update sets from dev to test and then from test to production.
8.  Commit the update set on production. If the update set required a fix, commit both update sets in the order they were made.

## Two-step import process

If your development environment consists of only two instances, you can combine your development and testing instances into a single staging instance.

1.  Create an update set on the staging instance.
2.  Make customizations and changes on the staging instance.
3.  Mark the update set as Complete.
4.  Test customizations thoroughly on the staging instance.
5.  If the update set has problems, repeat steps 1 - 4 to develop the fix on the staging instance with another update set.
6.  Log in to the production instance and retrieve the completed update set from the staging instance. If the update set required a fix, retrieve both update sets.
7.  Commit the update set on production. If the update set required a fix, commit both update sets in the order they were made.

**Parent Topic:**[Administer system update sets](../concept/administer-system-update-sets.md)

