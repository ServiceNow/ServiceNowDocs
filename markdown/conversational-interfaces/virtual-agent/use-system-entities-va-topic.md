---
title: Use system-derived entities in an NLU topic
description: Associate system-derived entities such as such as date, time, duration, or location with a node in a topic.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating a Virtual Agent topic, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Use system-derived entities in an NLU topic

Associate system-derived entities such as such as date, time, duration, or location with a node in a topic.

## Before you begin

Create the Booking Reservations NLU model and system entities \(`FromLocation` and `ToLocation`\) as described in [Create a system-derived entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nlu-service/create-system-derived-entity.md). In this example procedure, you will create a topic that can slot fill locations that are used in an utterance.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  [Create a new topic](create-virtual-agent-topic.md) called `Booking Reservations`.

    When completing the **Properties** tab, make sure that you choose the Booking Reservations NLU model that you created in an earlier exercise.

2.  Drag a Text bot response component onto the canvas, and then select it.

    In the properties sheet, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Node name|Type `Intro`.|
    |Response Message|Type `Let's get you booked on a flight`.|

    ![In the Text response properties, the Node name is "Intro," and the Response Message is, "Let's get you booked on a flight."](../images/sys-entities-example-1.png "Intro Text response properties")

3.  Drag a Text user input component onto the canvas.

    In the properties sheet, fill in the fields.

<table id="table_p4m_fzy_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Type `Fromwhere`.

</td></tr><tr><td>

Prompt

</td><td>

Type `Where are you departing from?`

</td></tr><tr><td>

Input format

</td><td>

Select **Text**. This doesn't restrict the input format.

</td></tr><tr><td>

NLU entity

</td><td>

Select `FromLocation`.This list only shows existing entities, such as system entities or entities that you created for the model.

</td></tr><tr><td>

Do not ask users to confirm recognized entity

</td><td>

Select this option to avoid having Virtual Agent ask the user to confirm the location.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Topic switching

</td></tr><tr><td>

Enable NLU to switch topics

</td><td>

Slide this toggle switch to enable topic switching.

</td></tr></tbody>
</table>    ![In the Fromwhere Text user input node, the prompt reads, "Where are you departing from?" The NLU entity used is FromLocation. Topic switching is enabled.](../images/sys-entities-example-2.png "Fromwhere Text user input response properties")

4.  Drag another Text user input component onto the canvas.

    In the properties sheet, fill in the fields.

<table id="table_bh3_y1z_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Type `Towhere`.

</td></tr><tr><td>

Prompt

</td><td>

Type `Where are you heading?`

</td></tr><tr><td>

Input format

</td><td>

Select **Text**. This doesn't restrict the input format.

</td></tr><tr><td>

NLU Entity

</td><td>

Select `ToLocation`.This list only shows existing entities, such as system entities or entities that you created for the model.

</td></tr><tr><td>

Do not ask users to confirm recognized entity

</td><td>

Select this option to avoid having Virtual Agent ask the user to confirm the location.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced \(optional\)

</td></tr><tr><td class="sub-head" colspan="2">

Topic switching

</td></tr><tr><td>

Enable NLU to switch topics

</td><td>

Slide this toggle switch to enable topic switching.

</td></tr></tbody>
</table>    ![In the Towhere Text user input node, the prompt reads, "Where are you heading?" The NLU entity used is ToLocation. Topic switching is enabled.](../images/sys-entities-example-3.png "Towhere Text user input response properties")

5.  Drag another Text bot response component onto the canvas, and then select it.

    In the properties sheet, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Node name|Type `Confirmation`.|
    |Response Message|Type `Great! I have you booked on a flight from [Fromwhere] to [Towhere]. Bon voyage!` Use dot-walking to replace `[Fromwhere]` and `[Towhere]` with the input variables you created in the previous nodes.|

    ![The Confirmation node displays the message, "Great! I have you booked on a flight from blank to blank," which will be slot-filled from the Fromwhere and Towhere input variables.](../images/sys-entities-example-4.png "Confirmation text response properties")

6.  Click **Save**.


## What to do next

Use additional system-derived entities for your Booking a Reservation topic. For example, you can use system-derived entities to capture the dates that the user wants to travel.

For more information about default system entities, see [NLU system entities](../reference/nlu-system-entities.md).

**Parent Topic:**[Creating a Virtual Agent topic](create-virtual-agent-topic.md)

