---
title: Configure, customize, or build new apps
description: Configuration and customization are hallmarks of the ServiceNow AI Platform that enable your company to customize workflows to fit its specific needs. You can also build new apps for novel use cases or departmental processes that don't fit within the scope of your current applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Building apps in ServiceNow, Getting Started guide for developers, Building applications]
---

# Configure, customize, or build new apps

Configuration and customization are hallmarks of the ServiceNow AI Platform that enable your company to customize workflows to fit its specific needs. You can also build new apps for novel use cases or departmental processes that don't fit within the scope of your current applications.

Whichever way you choose to make changes to the platform and app functionality, consider the following information to make the most informed choice.

## Configuration and customization

While the terms configuration and customization may sound very similar, they mean different things on the ServiceNow AI Platform. There are many ways you can update OOTB apps to work for your use case. Whether you personalize, configure, customize, or create an application, there are general guidelines for how to approach making your apps work for you. Each relevant term is defined in the following table.

|Term|Definition|
|----|----------|
|Personalization|When users modify an application's look and feel **only for themselves**.|
|Configuration|When users modify an application's behavior **without making changes to flows or the base system code**.|
|Customization|When users make **any change to the flows or the code that are part of the baseline installation** on a ServiceNow instance.|
|Building new|When a user **builds a custom app** using App Engine products like ServiceNow Studio.|

## Impact of changes

The impact of changes you make on the platform can have cost and support implications. Carefully consider the updates you want to make. See examples of each type of change and its implications.

<table id="table_n3f_4yv_5hc"><thead><tr><th>

Change

</th><th>

Examples

</th><th>

Impact

</th></tr></thead><tbody><tr><td>

Personalization

</td><td>

-   Choosing Dark mode or Light mode.
-   Choosing which columns to display in a table.

</td><td>

-   Does not change the baseline code installation.
-   Does not impact customer support or interfere with upgrades.

</td></tr><tr><td>

Configuration

</td><td>

-   Using built-in tools to add tables and more.
-   Setting instance-wide parameters.
-   Using code to extend an app’s functionality.

</td><td>

-   If you add code, you own it, even if it doesn’t alter the baseline code installation.
-   Reverting a configuration should not require code changes.

</td></tr><tr><td>

Customization

</td><td>

-   Creating scripts or business rules with logic that modifies baseline code.
-   Adding custom tables.
-   Adding custom integrations, widgets, portals, or workflows.

</td><td>

-   Customer Service and cost implications.
-   Upgrading to a new version requires reapplying or reverting your customizations.
-   Can create technical debt.

</td></tr><tr><td>

Building new apps

</td><td>

Creating new global or scoped apps, no matter the size or purpose.

</td><td>

-   May impact licensing agreements, based on which products you have provisioned.
-   May impact upgrades.
-   May create technical debt that must be managed.

</td></tr></tbody>
</table>## What happens when you customize

When you customize an application, several things happen that you must be aware of.

1.  Customizations trigger the platform to create a record on the Customer Update \[sys\_update\_xmll\] table.

    Each record on this table must be addressed when upgrading to a new version.

2.  The platform skips customized records during platform upgrades. You must choose what happens to customizations.
    -   Retain each customization.
    -   Revert each customization to the OOTB state.
    -   Merge the customizations with the base system.
3.  With each retained customization, there could be customer support consequences. Because Customer Support agents don't know what the expected behavior of a customization should be, it's difficult to reproduce the issue on an OOTB instance and help with support cases.

Keep these situations in mind when you create customizations.

**Tip:** Remember, only customize an application when the customization extends the intended purpose of the application. If it doesn't extend the intended purpose, consider creating a new application.

## Recommended order of changes

1.  Personalize your instance and apps as much as you’d like.
2.  Configure ServiceNow applications as much as you can before customizing them.
3.  Customize an application to add functionality only when it extends the intent of the application.
4.  Use App Engine developer products, such as Creator Studio and ServiceNow Studio, to create new applications rather than customizing an application to create functionality that doesn’t align with its original purpose.

**Parent Topic:**[Overview of building apps in ServiceNow](overview-building-apps-in-servicenow.md)

