---
title: Playbook Experience
description: Understand how Playbook work in the ServiceNow AI Platform to automate cross-functional processes and consolidate them into task-oriented views for your end users.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Playbook, Playbooks, Workflow Studio, Build workflows]
---

# Playbook Experience

Understand how Playbook work in the ServiceNow AI Platform® to automate cross-functional processes and consolidate them into task-oriented views for your end users.

**All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks** is the design environment where playbook owners build playbooks. Meanwhile, the runtime experience is where end users, such as playbook agents, follow the playbook to complete a business process. To learn more about the Playbook designer, see [Playbook builder](exploring-process-automation-designer.md).

## Runtime experience

Workflow Studio produces these runtime components for Playbooks:

-   **Process executions**

    A process execution stores the details of running a playbook in a context record. You can use a process execution to troubleshoot and verify that playbooks run as expected.

-   **Activity executions**

    An activity execution stores the details of running an activity instance in a context record. You can use an activity execution to troubleshoot and verify that playbooks run as expected.

-   **Playbook runtime**

    Playbook runtime is when a playbook runs for an agent or fulfiller. A playbook runs for agents only after Playbook Experience administrators configure how and where the playbook appears.


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

**Parent Topic:**[Exploring Playbook](process-automation-designer.md)

