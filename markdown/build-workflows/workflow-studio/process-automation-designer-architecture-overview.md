---
title: Playbooks User Experience
description: Understand how Workflow Studio Playbooks work in the ServiceNow AI Platform to automate cross-functional processes and consolidate them into task-oriented views for your end users.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Exploring playbooks, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Playbooks User Experience

Understand how Workflow Studio Playbooks work in the ServiceNow AI Platform® to automate cross-functional processes and consolidate them into task-oriented views for your end users.

**All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**is the design environment where playbook owners build playbooks. Meanwhile, the runtime experience is where end users, such as playbook agents, follow the playbook to complete a business process.

## Design environment

The Playbooks design environment in Workflow Studio consists of these components:

-   **Playbooks**

    A playbook is where a playbook owner configures and organizes multiple instances of Workflow Studio content into a coherent business process. A playbook consists of a trigger and a sequence of stages, which are made up of a sequence of activities.

-   **Trigger definitions**

    A trigger definition specifies the conditions that must be met to run a playbook. A user with the admin, playbook.admin, or pd\_trigger\_author role typically creates and configures a trigger definition that playbook authors can use as a template. A trigger definition specifies the record operation and table conditions that must be met to start running a playbook. A playbook owner typically selects a trigger template when creating a playbook.

-   **Trigger instances**

    A trigger instance is produced when you select a trigger template. The trigger instance stores the conditions that a record must meet to start running the playbook.

-   **Stages**

    A stage is a logical grouping of activities in a playbook. A playbook owner creates a stage to group activities and specify the start rule for when the stage should start running. A stage in your overall business process.

-   **Activity definitions**

    An activity definition maps [subflow](../../workflow-studio/reference/exploring-subflows.md) and [action](../../workflow-studio/concept/exploring-actions.md) inputs and outputs to an activity instance. An activity definition contains:

    -   The automation plan to map the triggering input record data to action or subflow inputs
    -   The activity experience to map action or subflow outputs to a user-facing view of the playbook
    A user with the admin, playbook.admin, or pd\_content\_author roles typically specifies the automation plan and activity experience when creating an activity definition.

-   **Activity instances**

    An activity instance is produced when you add an activity to a playbook. The activity instance stores the automation plan data mappings from the activity definition. You can change these data mappings when the default values do not fit your playbook. The playbook can specify the start rules for when the activity should start running.

-   **Start rules**

    A start rule specifies when a stage or an activity starts running. A playbook owner can use start rules to specify what parts of a playbook run simultaneously and what parts run serially.


For more information about how to use and navigate the Workflow Studio user interface, see [Playbooks](exploring-process-automation-designer.md).

## Runtime experience

Workflow Studio produces these runtime components for Playbooks:

-   **Process executions**

    A process execution stores the details of running a playbook in a context record. You can use a process execution to troubleshoot and verify that playbooks run as expected.

-   **Activity executions**

    An activity execution stores the details of running an activity instance in a context record. You can use an activity execution to troubleshoot and verify that playbooks run as expected.

-   **Playbook runtime**

    Playbook runtime is when a playbook runs for an agent or fulfiller. A playbook runs for agents only after Playbook Experience administrators configure how and where the playbook appears. See Set up a Playbook.


During runtime for a playbook, your instance:

1.  Evaluates any conditions specified in the trigger definition and processes the trigger.
2.  Processes the [Events](../../platform-events/concept/events.md) and starts running the playbook in the background.
3.  Builds the automation plans from each activity into an entire process plan.
4.  Runs the process plan for your playbook.
5.  Stores the process execution information in the Process Execution \[sys\_pd\_context\] table.
6.  Provides data for the running playbook view that agents and fulfillers experience.

![Sequence of playbook processing.](../images/process-definition-runtime-processing.png "Playbook processing")

Your instance processes a playbook during runtime by evaluating trigger conditions, processing the event in the queue, building and running a process plan, storing process execution details, and providing data for the Playbook Experience.

## Data security and HTML sanitization

Playbooks protects against cross-site scripting and code injection by evaluating all string data for HTML markup. The system only preserves HTML markup that is present in its inclusion list. All other HTML markup is removed from string data.

The inclusion list supports these HTML elements and attributes, which cannot be modified.

|HTML element|Included Attributes|
|------------|-------------------|
|a|class, href, target, title|
|abbr|class, title|
|address|class|
|area|alt, class, coords, href, shape|
|article|class|
|aside|class|
|audio|autoplay, class, controls, loop, preload, src|
|b|class|
|bdi|class, dir|
|bdo|class, dir|
|big|class|
|blockquote|cite, class|
|br|class|
|caption|class|
|center|class|
|cite|class|
|code|class|
|col|align, class, span, valign, width|
|colgroup|align, class, span, valign, width|
|dd|class|
|del|class, datetime|
|details|class, open|
|div|class|
|dl|class|
|dt|class|
|em|class|
|emp|class|
|font|class, color, face, size|
|footer|class|
|h1|class|
|h2|class|
|h3|class|
|h4|class|
|h5|class|
|h6|class|
|header|class|
|hr|class|
|html| |
|i|class|
|img|alt, class, height, src, title, width|
|input|aria-label, class, type, value|
|ins|class, datetime|
|li|class|
|mark|class|
|nav|class|
|ol|class|
|p|class|
|pre|class|
|s|class|
|section|class|
|small|class|
|span|class|
|sub|class|
|sup|class|
|svg|class|
|strong|class|
|style| |
|table|align, border, class, valign, width|
|tag|class|
|tbody|align, class, valign|
|td|align, class, colspan, rowspan, valign, width|
|tfoot|align, class, valign|
|th|align, class, colspan, rowspan, valign, width|
|thead|align, class, valign|
|tr|align, class, rowspan, valign|
|tt|class|
|u|class|
|ul|class|
|video|autoplay, class, controls, height, loop, preload, src, width|

**Parent Topic:**[Exploring playbooks](process-automation-designer.md)

