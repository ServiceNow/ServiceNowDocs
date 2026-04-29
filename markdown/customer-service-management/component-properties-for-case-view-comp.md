---
title: Component properties for the Case view
description: Component properties enable you to configure the behavior of the Case view component instance on a third-party website.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Web Embeddables component properties, Web Embeddables reference, Reference, Customer Service Management]
---

# Component properties for the Case view

Component properties enable you to configure the behavior of the Case view component instance on a third-party website.

<table id="table_csm_base_entities"><thead><tr><th>

Component property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table from which the case or task shown on the Case view component.By default, this field is set to the Case \[sn\_customerservice\_case\] table.

**Note:** Case view component can show the records from any extended table of case or task table.

</td></tr><tr><td>

Record ID

</td><td>

The system identifier \(sys\_id\) of the record from the specified table.

</td></tr><tr><td>

Header configuration

</td><td>

Display different fields from the record in the header. The details display on the header are defined in the UX Header Configurations \[sys\_ux\_header\_config\] table.The default label is `Embedded Experiences Case view Header Configuration` and sys\_id is \(1db45f9118520210f8775b8843daf927\).

</td></tr><tr><td>

Hide actions

</td><td>

Option to show or hide the action button on the header.By default, the header displays all actions.

</td></tr><tr><td>

Action configuration

</td><td>

Display different actions available for the record from the UX Actions Configuration \[sys\_ux\_action\_config\].The default label is 'Embedded Experiences Case view Action Configuration' and sys\_id is \(b226535518520210f8775b8843daf9fb\).

**Note:** If the Action configuration field is empty, all actions are hidden.

</td></tr><tr><td>

Hide activity

</td><td>

Option to show or hide past activities associated with your record, starting with the most recent.By default, it shows activity tab.

</td></tr><tr><td>

Hide attachments

</td><td>

Option to show or hide attachment tab on the case detailed view.By default, it shows attachment tab.

</td></tr><tr><td>

Hide all related lists

</td><td>

Option to show or hide related lists on the case detailed view.By default, it shows all related lists.

</td></tr><tr><td>

Table view

</td><td>

Table view is used to identify the related lists associated with the record.

</td></tr><tr><td>

Show custom tab

</td><td>

Option to show or hide custom tab. By default, it hides custom tab.

</td></tr><tr><td>

Hide playbook process tab

</td><td>

Option to hide the process tab which is displayed when a playbook is available for the record.

</td></tr><tr><td>

Playbook experience

</td><td>

Select a playbook experience to use. If not selected, the Global Playbook Experience is used.

</td></tr><tr><td>

Hide playbook stages

</td><td>

Option to hide playbook stages to display activities of the current stage.

</td></tr><tr><td>

Playbook stage orientation

</td><td>

Horizontal orientation displays playbook stages horizontally and activities vertically.

 Vertical orientation displays playbook stages vertically and activities nested within each stage.

</td></tr><tr><td>

Visible horizontal playbook stages

</td><td>

Displays the number of stages visible in the horizontal stage picker for the playbook without scrolling.

</td></tr><tr><td>

Playbook activity view mode

</td><td>

View mode for displaying playbook activities in a stacked or focused layout.

</td></tr><tr><td>

Hide errors

</td><td>

Option to show or hide error messages for the end user on the third-party website.By default, it shows errors.

</td></tr></tbody>
</table>**Related topics**  


[Configure the Case view component instance](../task/configure-case-view-component-on-instance.md)

[Embed the Case view component instance on the third-party website](../task/embed-case-view-comp-on-third-party-website.md)

[Event handler in the enhanced Case view component](we-case-view-event-handler.md)

[Sample code to handle the Case view component](we-case-view-sample-code.md)

