---
title: Component properties for the Playbook intake
description: Component properties enable you to configure the behavior of the Playbook intake component instance on the third-party website.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Web Embeddables component properties, Web Embeddables reference, Reference, Customer Service Management]
---

# Component properties for the Playbook intake

Component properties enable you to configure the behavior of the Playbook intake component instance on the third-party website.

<table id="table_csm_base_entities"><thead><tr><th>

Component property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the playbook case create form. Title will be replaced by case number if there’s no short description after record is created.

</td></tr><tr><td>

Table

</td><td>

Table in which the record is created.

</td></tr><tr><td>

Record generator

</td><td>

Playbook record generator used to create the record for which the playbook is defined.

</td></tr><tr><td>

Prefill fields

</td><td>

Query that automatically populates fields on the Playbook case form. Example account = Solana^state=draft.The query overrides all the template fields configured on the record generator.

</td></tr><tr><td>

Playbook experience

</td><td>

Optionally, select a playbook experience to use. If not selected, the Global Playbook Experience is used.

</td></tr><tr><td>

Hide stages

</td><td>

Option to hide playbook stages to display activities of current stage.

</td></tr><tr><td>

Stage orientation

</td><td>

Horizontal orientation displays playbook stages horizontally and activities vertically.Vertical orientation displays playbook stages vertically and activities nested within each stage.

</td></tr><tr><td>

Visible horizontal stages

</td><td>

Displays the number of stages visible in the horizontal stage picker for the playbook without scrolling.

</td></tr><tr><td>

Activity view mode

</td><td>

View mode for displaying playbook activities in a stacked or focused layout.

</td></tr><tr><td>

Hide record creation confirmation

</td><td>

Option to hide the confirmation page after the record is created and opens the Playbook case view page.

</td></tr><tr><td>

Confirmation text

</td><td>

Confirmation text when the record is submitted successfully.

</td></tr><tr><td>

Confirmation sub-text

</td><td>

Confirmation subtext when the record is submitted successfully.

</td></tr><tr><td>

Hide reference number

</td><td>

Option to hide reference number of the record on the confirmation message.

</td></tr><tr><td>

Reference number label

</td><td>

Display text for the reference number label on the confirmation message.

</td></tr><tr><td>

Hide primary button

</td><td>

Option to hide the primary button on the confirmation message.

</td></tr><tr><td>

Primary button label

</td><td>

Display text for the primary button label.

</td></tr><tr><td>

Hide secondary button

</td><td>

Option to hide the secondary button on the confirmation message.

</td></tr><tr><td>

Secondary button label

</td><td>

Display text for the secondary button label.

</td></tr><tr><td>

Hide errors

</td><td>

Option to hide the error messages from end user when the component fails to load initially.

</td></tr></tbody>
</table>**Related topics**  


[Configure the Playbook intake component instance](../task/config-playbook-intake-comp.md)

[Embed the Playbook intake component instance on the third-party website](../task/embed-playbook-intake-comp.md)

[Event handler in the Playbook intake component](we-playbook-intake-event-handler.md)

[Sample code for the Playbook intake component](we-playbook-intake-sample-code.md)

