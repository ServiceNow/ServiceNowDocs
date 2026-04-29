---
title: Migration from Test Management 1.0 to Test Management 2.0
description: Migrate your test data from Test Management 1.0 to Test Management 2.0, and start using Test Management 2.0 for its enhanced testing capabilities and features.
locale: en-US
release: australia
product: Test Management
classification: test-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Test Management applications, Strategic Portfolio Management]
---

# Migration from Test Management 1.0 to Test Management 2.0

Migrate your test data from Test Management 1.0 to Test Management 2.0, and start using Test Management 2.0 for its enhanced testing capabilities and features.

Apply the following migration steps on a non-production instance, verify if the migration is completed as intended, and then perform the migration steps on a production instance.

## Migration steps

To migrate your test data from Test Management 1.0 to Test Management 2.0, complete the following steps in order:

1.  Activate the required plugins. For more information, see [Migration from Test Management 1.0 to Test Management 2.0](migrate-test.md).
2.  Convert your test suites. For more information, see [Convert test suites](migrate-test-suites.md).
3.  Verify the migrated data on a non-production instance before repeating on production.

## Activate plugins

Activate the Test Management 2.0 \(com.snc.test\_management.2.0\) and Test Management 2.0 — Data Migration \(com.snc.test\_migration\_v1\_v2\) plugins.

## Migrate data

The migration process allows you to move test suites, test cases, and tests.

**Note:**

-   Test plans cannot be migrated due to significant change of data model.
-   Test suites, test cases, and tests that are migrated to Test Management 2.0 will not be removed from Test Management 1.0.

Test cases that are migrated to Test Management 2.0 are converted to test versions in the following manner:

|Test Management 1.0: Test case|Test Management 2.0: Test version|
|------------------------------|---------------------------------|
|Short Description|Short Description|
|Domain|Domain|
|Test Suite|Creates a relationship between test and test set|
|Prerequisites|Link to the old test case|

Tests that are migrated to Test Management 2.0 are converted to test steps in the following manner:

|Test Management 1.0: Test|Test Management 2.0: Test step|
|-------------------------|------------------------------|
|Order|Order|
|Domain|Domain|
|Detailed description|Link to the old test|
|Test|Step|
|Test data|Link to the old test|
|Expected result|Verification step|

Test suites that are migrated to Test Management 2.0 are converted to test sets in the following manner:

|Test set in Test Management 1.0|Test set in Test Management 2.0|
|-------------------------------|-------------------------------|
|Name|Name|
|Owner|Owner|
|Domain|Domain|

## Add custom fields to migration

You have added custom fields to the tables of Test Management 1.0, and want to move the fields to the corresponding custom columns in Test Management 2.0. In such a case, include the custom fields into migration by overriding the mapping information in the script include **TestMigrationTableMapping**. The default mapping is provided in the script include **TestMigrationTableMappingBase**.

## Convert test suites

[Convert test suites](migrate-test-suites.md) with underlying test cases to test sets and tests.

