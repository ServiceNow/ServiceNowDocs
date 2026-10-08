---
title: Playbook record generator
description: Use the playbook record generator to guide a user through the record creation process using the Playbook Experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/playbook-record-generator-overview.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-09-15"
reading_time_minutes: 2
breadcrumb: [Designing playbooks, Use, Workflow Studio, Build workflows]
---

# Playbook record generator

Use the playbook record generator to guide a user through the record creation process using the Playbook Experience.

Playbooks requires a record to be created or updated before a process can start. However, you can use the playbook record generator to enable users to create a record using the playbook experience. You can then configure your workspace or UI Builder page to display the record generator Playbook Experience component in place of the standard new record form. The component appears when a user opens a new record tab.

## When to use the record generator

The record generator is best suited to record-based playbooks that start automatically when the record is created. If you need to launch a playbook on demand or supply inputs at launch time rather than through a triggered record, consider on-demand launcher properties instead.

## How the record generator works

Before the record exists, the playbook displays a representation of the process definition configured for the record generator. A dynamically inserted first activity contains the new record form, while the remaining activities in the process stay pending. This preview lets the user see the full process up front without a record backing it yet.

Playbook record generator inserts a record generator activity as the first step within a specified process definition created with Playbooks. This record generator activity contains a new record form. After a user submits the form, the system creates the record. Record creation normally triggers the process definition shown in the preview. If no process definition is running after submission, the playbook manually triggers the one shown to the user before record creation. The record generator activity's type then changes from Record Generator to Record, because it's now associated with the created record. The running process replaces the preview without the user leaving the playbook, for a seamless and guided record creation experience.

## Selecting a record generator

You can configure more than one record generator for the same table. When several record generators apply, the one with the lowest Order value is selected by default. A caller can override this default selection explicitly by supplying a process definition or record generator identifier in the query passed to the playbook component.

## Configuration options

Administrators can specify the name of the record generator activity, the form view, and the process definition shown to the user before the record is created. The button the user selects to submit the form \(**Continue**\) is itself a declarative action. Administrators can override its label, styling, or conditions the same way they would customize any other declarative action.

## Redirect to the created record

The out-of-the-box playbook layouts handle the refresh and redirect to the newly created record automatically. If you build a custom layout, you're responsible for wiring this yourself: binding the playbook component to the target parent table, and handling the event the component dispatches when the record is created so your page can route to it.

-   **[Configure a playbook record generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/configure-playbook-record-generator.md)**  
Configure a record generator to let a user create the parent record for a process from inside the Playbook Experience.
-   **[Edit a record after record generator submission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/edit-record-after-record-generator-submission.md)**  
Keep a record editable after a playbook record generator creates it.

**Parent Topic:**[Designing playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/playbook-experience-admins.md)

