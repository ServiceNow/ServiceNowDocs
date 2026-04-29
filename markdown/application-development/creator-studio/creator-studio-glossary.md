---
title: Creator Studio glossary
description: Learn about the terms and concepts used in Creator Studio.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio glossary

Learn about the terms and concepts used in Creator Studio.

**Parent Topic:**[Creator Studio reference](../reference/creator-studio-reference.md)

## activity

Activities in a playbook complete automated tasks, such as obtaining approvals, assigning records, and sending emails.

## automation

Tasks or requests moving through a workflow without manual intervention.

## board view

A traditional layout of viewing a playbook, which shows each activity as a card in the navigation panel. When you select an activity, for example a task, its editable details appear in the canvas for you to work with them.

## catalog

A collection of items that represent all the items a requestor can ask for.

## collaboration descriptor

Level of collaborative access assigned to a developer. The collaboration descriptor that someone is assigned determines if they can assign, manage, and monitor delegated development permissions. For example, people who are Owners of an app can do more than people with the Editor collaboration type.

## delegated development

A collaborative process that enables developers to invite other people into apps so they can co-create and develop the app together.

## deployment

The process of an app moving from a non-production instance like development or QA through to production. Production is the instance that your customers see, or your “live” instance.

## diagram view

A visually intuitive diagram that shows you the order that activities occur in the playbook. When you select an activity, such as the trigger or a decision, a modal pops up where you can edit its details.

## dot-walking

Describes the structure of a variable that contains one or more reference fields, separated by a dot for each table involved.

## dynamic behavior

A form for a catalog item can use dynamic behavior to automatically update based on how users answer a question. For example, if a user says they don't want lunch for an event they're attending, you can make a **Meal preference** field disappear.

**Note:** Dynamic behaviors are also called Catalog UI Policies.

## extend a table

When you create a table based off an existing table. Extending a table means the new table inherits the parent \(extended\) table's columns, as well as its business logic. Apps built in Creator Studio generally extend the Request Task table.

## field

A field in Creator Studio is a column on the app's underlying table. If you're using condition builder, a field is either a column on the table or a question from the form.

## form

A content page that displays fields and values for a single record from a database table.

## form template

A pre-defined set of questions arranged on a form provided by Creator Studio.

## fulfiller

Someone who works on requests. Fulfillers may also approve or deny requests, depending on any approval automation for the app.

## item

Something a requestor can ask for, such as new computer equipment or time off work. Each item requires its own form in Creator Studio.

## playbook

A set of automated activities that occur based on a trigger. For example, sending an email when a request is approved. Think of playbooks as pre-programmed workflows that kick in after a form is submitted. They are like if/then statements: If this happens, then that will happen.

## record

A task or request that needs to be acted on. All rows in that table for an app are individual records. Records have different states depending on what actions have been taken.

## reference-based question

A question on a form that retrieves its possible answers from the table that you define.

## release notes

The information about what's included in each new version of the deployed app. Release notes help administrators to track what the changes are between app versions.

## requestor

Someone requesting something, like a piece of equipment or permission to do something, such as take time off work.

## target table

The table where apps created in Creator Studio store their requests. Admininstrators can change the table that an app saves its data to. For more information, see [Administering an app's associated table](creator-studio-admin-app-table.md).

## trigger

The event that makes an automated playbook begin running. For example, submitting a request automatically assigns it to a manager.

## version number

A number assigned to the app that increases with each subsequent time it's deployed.

## workflow

Defined sequence of steps automating processes in Sales and Order Management.

