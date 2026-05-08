---
title: Migrating from the legacy Ideas application to Idea Portal
description: If you are upgrading to the Australia release, complete the migration tasks after the upgrade to start using the new Idea Portal.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Innovation Management, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrating from the legacy Ideas application to Idea Portal

If you are upgrading to the Australia release, complete the migration tasks after the upgrade to start using the new Idea Portal.

Review the following information and make any necessary changes to your configuration:

## Idea States

The new Idea Portal provides new idea states such as Completed, Under Review, and In Backlog, which are mapped with your existing idea states. The following tables provide a comparison to the existing idea states and the equivalent new states with their values.

|Idea State|Value|
|----------|-----|
|Draft|-5|
|Submitted|1|
|NA|NA|
|NA|NA|
|Accepted|2|
|NA|NA|
|NA|NA|
|Closed complete|3|
|Closed skipped|7|
|NA|NA|
|NA|NA|

|Idea State|Value|
|----------|-----|
|Draft|-5|
|Submitted|1|
|Under Review|-1|
|Need more information|-2|
|In Backlog|2|
|Planned|4|
|In Development|5|
|Completed|3|
|Unlikely to Implement|7|
|Duplicate|8|
|Already Exists|9|

Starting with the Australia release, idea states are stored in and retrieved from the Idea \[im\_idea\_core\] table. You can continue to use your existing idea states along with the new idea states. However, if you want to use only these new states for managing your ideas, navigate to the Choice \[sys\_choice\] table and delete the old idea states.

## Idea categories

Organize your ideas using categories, for example, to group ideas that are relevant to a particular product, department, or business unit. If your existing ideas are not associated with any category, [create new categories](../task/category-configuration-existing-table.md) or select an existing table to [define categories](../task/category-configuration-existing-table.md) to which you can map your ideas. The Ideas application also installs a set of default new categories to which you can associate your existing ideas.

If your ideas are already associated with categories and you want to use the new categories, you can map your existing idea categories to the default new categories. You then write and use a script to create m2m mapping between existing ideas and categories.

**Note:** You must map an existing idea with appropriate categories for your ideas to appear in the Idea Portal.

## Converting ideas to demands or project, stories, initiatives, and epics

You can convert an idea into work entities other than demands. The **Create Task** button enables you to convert an idea into a project, epic, or story as well as a demand becomes available in the Idea form.

You must have the required Agile plugins Agile Development 2.0 and Scaled Agile Framework \(SAFe\) and Continual Improvement Management installed to view these options.

If you want to allow conversion of ideas only to a demand, disable the **Create Task** button and continue using the **Accept** button or disable the **Accept** and **Defer** buttons to use other options. For more information see, Using the form designer.

## Business rules

Review the existing business rules in the idea table. Set the business rules that you don't want to apply as False.

## Navigation for legacy Idea application

To encourage your users to submit ideas through the new Idea Portal, remove navigation for old Idea application from the application menu and deactivate the Submit an Idea option from the Service Catalog. For more information see, Enable or disable an application menu or module.

**Parent Topic:**[Configuring Innovation Management](../concept/configuring-innovation-management.md)

