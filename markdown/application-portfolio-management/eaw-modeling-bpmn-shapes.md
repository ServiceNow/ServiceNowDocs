---
title: Business Process Modeling Notation \(BPMN\) shapes
description: Use the BPMN shapes to generate diagrams for your current business processes and model the future state of the business processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-modeling-bpmn-shapes.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Shapes to create a modeling diagram, Exploring Enterprise Modeling and Visualization in the EA Workspace, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Business Process Modeling Notation \(BPMN\) shapes

Use the BPMN shapes to generate diagrams for your current business processes and model the future state of the business processes.

## BPMN shapes in Enterprise Modeling and Visualization

You can add a shape to the canvas by either selecting the shape or by dragging the shape from the **Shapes** palette to the canvas.

You can also adjust the size of shapes by selecting a shape and then drag any of its edges or corner handles. Pulling outward increases the shape's dimensions, while dragging inward reduces its size. However, BPMN-Event shapes can’t be resized.

When you drag a BPMN shape from the **Shapes** palette to the canvas, the shape icon you drag matches the shape's appearance on the canvas. This helps you confirm the correct shape before placing it on the canvas.

BPMN shapes are organized into sub-categories in the **Shapes** palette: **Event**, **Activity**, **Gateway**, and **General**. Expand a sub-category to see and add its shapes.

## BPMN: General shapes

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-icon-pool.png"\] Alt text: Pool|Pool|
|\[Omitted image "bpmn-icon-lane.png"\] Alt text: Lane|Lane|

## BPMN-Event shapes

Event shapes represent something that happens during a process. Events are categorized by their position in the process flow — start, intermediate, or end — and by the trigger type that causes or results from the event. Boundary events are attached to an activity shape and fire when a specific condition occurs while the activity is running. BPMN-Event shapes cannot be resized.

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-start-event-compensation.png"\] Alt text: Start \(Compensation\)|Start \(Compensation\)|
|\[Omitted image "bpmn-start-event-error.png"\] Alt text: Start \(Error\)|Start \(Error\)|
|\[Omitted image "bpmn-start-event-escalation.png"\] Alt text: Start \(Escalation\)|Start \(Escalation\)|
|\[Omitted image "bpmn-start-event-condition.png"\] Alt text: Start Interrupting Conditional|Start Interrupting Conditional|
|\[Omitted image "bpmn-start-event-message.png"\] Alt text: Start Interrupting Message|Start Interrupting Message|
|\[Omitted image "bpmn-start-event-signal.png"\] Alt text: Start Interrupting Signal|Start Interrupting Signal|
|\[Omitted image "bpmn-start-event-timer.png"\] Alt text: Start Interrupting Timer|Start Interrupting Timer|
|\[Omitted image "bpmn-start-event-multiple.png"\] Alt text: Start \(Multiple\)|Start \(Multiple\)|
|\[Omitted image "bpmn-start-event-non-interrupting-condition.png"\] Alt text: Start \(Non-Interrupting Condition\)|Start \(Non-Interrupting Condition\)|
|\[Omitted image "bpmn-start-event-non-interrupting-escalation.png"\] Alt text: Start \(Non-Interrupting Escalation\)|Start \(Non-Interrupting Escalation\)|
|\[Omitted image "bpmn-start-event-non-interrupting-message.png"\] Alt text: Start \(Non-Interrupting Message\)|Start \(Non-Interrupting Message\)|
|\[Omitted image "bpmn-start-event-non-interrupting-multiple.png"\] Alt text: Start \(Non-Interrupting Multiple\)|Start \(Non-Interrupting Multiple\)|
|\[Omitted image "bpmn-start-event-non-interrupting-parallel-multiple.png"\] Alt text: Start \(Non-Interrupting Parallel Multiple\)|Start \(Non-Interrupting Parallel Multiple\)|
|\[Omitted image "bpmn-start-event-non-interrupting-signal.png"\] Alt text: Start \(Non-Interrupting Signal\)|Start \(Non-Interrupting Signal\)|
|\[Omitted image "bpmn-start-event-non-interrupting-timer.png"\] Alt text: Start \(Non-Interrupting Timer\)|Start \(Non-Interrupting Timer\)|
|\[Omitted image "bpmn-start-event-none.png"\] Alt text: Start \(None\)|Start \(None\)|
|\[Omitted image "bpmn-start-event-parallel-multiple.png"\] Alt text: Start \(Parallel Multiple\)|Start \(Parallel Multiple\)|
|\[Omitted image "bpmn-intermediate-event-catch-cancel.png"\] Alt text: Intermediate \(Catch-Cancel\)|Intermediate \(Catch-Cancel\)|
|\[Omitted image "bpmn-intermediate-event-catch-compensation.png"\] Alt text: Intermediate \(Catch-Compensation\)|Intermediate \(Catch-Compensation\)|
|\[Omitted image "bpmn-intermediate-event-catch-condition.png"\] Alt text: Intermediate \(Catch-Conditional\)|Intermediate \(Catch-Conditional\)|
|\[Omitted image "bpmn-intermediate-event-catch-error.png"\] Alt text: Intermediate \(Catch-Error\)|Intermediate \(Catch-Error\)|
|\[Omitted image "bpmn-intermediate-event-catch-escalation.png"\] Alt text: Intermediate \(Catch-Escalation\)|Intermediate \(Catch-Escalation\)|
|\[Omitted image "bpmn-intermediate-event-catch-message.png"\] Alt text: Intermediate \(Catch-Message\)|Intermediate \(Catch-Message\)|
|\[Omitted image "bpmn-intermediate-event-catch-multiple.png"\] Alt text: Intermediate \(Catch-Multiple\)|Intermediate \(Catch-Multiple\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-condition.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Condition\)|Intermediate \(Catch-Non-Interrupting Condition\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-escalation.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Escalation\)|Intermediate \(Catch-Non-Interrupting Escalation\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-message.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Message\)|Intermediate \(Catch-Non-Interrupting Message\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-multiple.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Multiple\)|Intermediate \(Catch-Non-Interrupting Multiple\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-parallel-multiple.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Parallel Multiple\)|Intermediate \(Catch-Non-Interrupting Parallel Multiple\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-signal.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Parallel Multiple\)|Intermediate \(Catch-Non-Interrupting Parallel Multiple\)|
|\[Omitted image "bpmn-intermediate-event-catch-non-interrupting-timer.png"\] Alt text: Intermediate \(Catch-Non-Interrupting Timer\)|Intermediate \(Catch-Non-Interrupting Timer\)|
|\[Omitted image "bpmn-intermediate-event-catch-parallel-multiple.png"\] Alt text: Intermediate \(Catch-Parallel Multiple\)|Intermediate \(Catch-Parallel Multiple\)|
|\[Omitted image "bpmn-intermediate-event-catch-signal.png"\] Alt text: Intermediate \(Catch-Signal\)|Intermediate \(Catch-Signal\)|
|\[Omitted image "bpmn-intermediate-event-catch-timer.png"\] Alt text: Intermediate \(Catch-Timer\)|Intermediate \(Catch-Timer\)|
|\[Omitted image "bpmn-intermediate-event-catch-link.png"\] Alt text: Intermediate \(Link-Catch\)|Intermediate \(Link-Catch\)|
|\[Omitted image "bpmn-intermediate-event-none.png"\] Alt text: Intermediate \(None\)|Intermediate \(None\)|
|\[Omitted image "bpmn-intermediate-event-throw-compensation.png"\] Alt text: Intermediate \(Throw-Compensation\)|Intermediate \(Throw-Compensation\)|
|\[Omitted image "bpmn-intermediate-event-throw-escalation.png"\] Alt text: Intermediate \(Throw-Escalation\)|Intermediate \(Throw-Escalation\)|
|\[Omitted image "bpmn-intermediate-event-throw-link.png"\] Alt text: Intermediate \(Throw-Link\)|Intermediate \(Throw-Link\)|
|\[Omitted image "bpmn-intermediate-event-throw-message.png"\] Alt text: Intermediate \(Throw-Message\)|Intermediate \(Throw-Message\)|
|\[Omitted image "bpmn-intermediate-event-throw-multiple.png"\] Alt text: Intermediate \(Throw-Multiple\)|Intermediate \(Throw-Multiple\)|
|\[Omitted image "bpmn-intermediate-event-throw-signal.png"\] Alt text: Intermediate \(Throw-Signal\)|Intermediate \(Throw-Signal\)|
| |Cancellation End|
|\[Omitted image "bpmn-end-event-compensation.png"\] Alt text: Compensation End|Compensation End|
|\[Omitted image "bpmn-end-event-link.png"\] Alt text: End \(Link\)|End \(Link\)|
|\[Omitted image "bpmn-end-event-none.png"\] Alt text: End \(None\)|End \(None\)|
|\[Omitted image "bpmn-end-event-error.png"\] Alt text: End Error|End Error|
|\[Omitted image "bpmn-end-event-message.png"\] Alt text: End Message|End Message|
|\[Omitted image "bpmn-end-event-signal.png"\] Alt text: End Signal|End Signal|
|\[Omitted image "bpmn-end-event-terminate.png"\] Alt text: End Terminate|End Terminate|
|\[Omitted image "bpmn-end-event-escalation.png"\] Alt text: Escalation End|Escalation End|
|\[Omitted image "bpmn-end-event-multiple.png"\] Alt text: Multiple End|Multiple End|
|||
|||
|||

## BPMN-Activity shapes

Activity shapes represent work performed within a process. Activities are divided into tasks, which are atomic units of work, and sub-processes and call activities, which reference other process flows. You can also apply a marker to any task shape to indicate how the activity executes — for example, whether it loops or runs in parallel.

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-acitivity-business-rule-task.png"\] Alt text: Business Rule Task|Business Rule Task|
|\[Omitted image "bpmn-acitivity-manual-task.png"\] Alt text: Manual Task|Manual Task|
|\[Omitted image "bpmn-acitivity-receive-task.png"\] Alt text: Receive Task|Receive Task|
|\[Omitted image "bpmn-acitivity-script-task.png"\] Alt text: Script Task|Script Task|
|\[Omitted image "bpmn-acitivity-send-task.png"\] Alt text: Send Task|Send Task|
|\[Omitted image "bpmn-acitivity-service-task.png"\] Alt text: Service Task|Service Task|
|\[Omitted image "bpmn-acitivity-task.png"\] Alt text: Task|Task|
|\[Omitted image "bpmn-acitivity-user-task.png"\] Alt text: User Task|User Task|
| | |
|||
|||
|||
|||

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-activity-business-rule-call-activity.png"\] Alt text: Business Rule Call Activity|Business Rule Call Activity|
|\[Omitted image "bpmn-activity-call-activity.png"\] Alt text: Call Activity|Call Activity|
|\[Omitted image "bpmn-activity-manual-call-activity.png"\] Alt text: Manual Call Activity|Manual Call Activity|
|\[Omitted image "bpmn-activity-script-call-activity.png"\] Alt text: Script Call Activity|Script Call Activity|
|\[Omitted image "bpmn-activity-user-call-activity.png"\] Alt text: User Call Activity|User Call Activity|
|\[Omitted image "bpmn-activity-sub-process.png"\] Alt text: Sub-Process|Sub-Process|
|\[Omitted image "bpmn-activity-adhoc-sub-process.png"\] Alt text: Adhoc Sub-Process|Adhoc Sub-Process|
| |Transaction Sub-Process|

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-acitivity-loop-business-rule-task.png"\] Alt text: Loop - Business Rule Task|Loop - Business Rule Task|
|\[Omitted image "bpmn-acitivity-loop-manual-task.png"\] Alt text: Loop - Manual Task|Loop - Manual Task|
|\[Omitted image "bpmn-acitivity-loop-receive-task.png"\] Alt text: Loop - Receive Task|Loop - Receive Task|
|\[Omitted image "bpmn-acitivity-loop-script-task.png"\] Alt text: Loop - Script Task|Loop - Script Task|
|\[Omitted image "bpmn-acitivity-loop-send-task.png"\] Alt text: Loop - Send Task|Loop - Send Task|
|\[Omitted image "bpmn-acitivity-loop-service-task.png"\] Alt text: Loop - Service Task|Loop - Service Task|
|\[Omitted image "bpmn-acitivity-loop-default-task.png"\] Alt text: Loop - Task|Loop - Task|
|\[Omitted image "bpmn-acitivity-loop-user-task.png"\] Alt text: Loop - User Task|Loop - User Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-business-rule-task.png"\] Alt text: Multi Instance Parallel - Business Rule Task|Multi Instance Parallel - Business Rule Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-manual-task.png"\] Alt text: Multi Instance Parallel - Manual Task|Multi Instance Parallel - Manual Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-receive-task.png"\] Alt text: Multi Instance Parallel - Receive Task|Multi Instance Parallel - Receive Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-script-task.png"\] Alt text: Multi Instance Parallel - Script Task|Multi Instance Parallel - Script Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-send-task.png"\] Alt text: Multi Instance Parallel - Send Task|Multi Instance Parallel - Send Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-service-task.png"\] Alt text: Multi Instance Parallel - Service Task|Multi Instance Parallel - Service Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-task.png"\] Alt text: Multi Instance Parallel - Task|Multi Instance Parallel - Task|
|\[Omitted image "bpmn-acitivity-multi-instance-parallel-user-task.png"\] Alt text: Multi Instance Parallel - User Task|Multi Instance Parallel - User Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-business-rule-task.png"\] Alt text: Multi Instance Sequential - Business Rule Task|Multi Instance Sequential - Business Rule Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-manual-task.png"\] Alt text: Multi Instance Sequential - Manual Task|Multi Instance Sequential - Manual Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-receive-task.png"\] Alt text: Multi Instance Sequential - Receive Task|Multi Instance Sequential - Receive Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-script-task.png"\] Alt text: Multi Instance Sequential - Script Task|Multi Instance Sequential - Script Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-sendTask.png"\] Alt text: Multi Instance Sequential - Send Task|Multi Instance Sequential - Send Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-service-task.png"\] Alt text: Multi Instance Sequential - Service Task|Multi Instance Sequential - Service Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-default-task.png"\] Alt text:|Multi Instance Sequential - Task|
|\[Omitted image "bpmn-acitivity-multi-instance-sequential-user-task.png"\] Alt text: Multi Instance Sequential - User Task|Multi Instance Sequential - User Task|
|\[Omitted image "bpmn-acitivity-compensation-business-rule-task.png"\] Alt text: Compensation - Business Rule Task|Compensation - Business Rule Task|
|\[Omitted image "bpmn-acitivity-compensation-manual-task.png"\] Alt text: Compensation - Manual Task|Compensation - Manual Task|
|\[Omitted image "bpmn-acitivity-compensation-receive-task.png"\] Alt text: Compensation - Receive Task|Compensation - Receive Task|
|\[Omitted image "bpmn-acitivity-compensation-script-task.png"\] Alt text: Compensation - Script Task|Compensation - Script Task|
|\[Omitted image "bpmn-acitivity-compensation-send-task.png"\] Alt text: Compensation - Send Task|Compensation - Send Task|
|\[Omitted image "bpmn-acitivity-compensation-service-task.png"\] Alt text: Compensation - Service Task|Compensation - Service Task|
|\[Omitted image "bpmn-acitivity-compensation-default-task.png"\] Alt text: Compensation - Task|Compensation - Task|
|\[Omitted image "bpmn-acitivity-compensation-user-task.png"\] Alt text: Compensation - User Task|Compensation - User Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-business-rule-task.png"\] Alt text: Loop &amp; Compensation - Business Rule Task|Loop &amp; Compensation - Business Rule Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-manual-task.png"\] Alt text: Loop &amp; Compensation - Manual Task|Loop &amp; Compensation - Manual Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-receive-task.png"\] Alt text: Loop &amp; Compensation - Receive Task|Loop &amp; Compensation - Receive Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-script-task.png"\] Alt text: Loop &amp; Compensation - Script Task|Loop &amp; Compensation - Script Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-send-task.png"\] Alt text: Loop &amp; Compensation - Send Task|Loop &amp; Compensation - Send Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-service-task.png"\] Alt text: Loop &amp; Compensation - Service Task|Loop &amp; Compensation - Service Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-default-task.png"\] Alt text: Loop &amp; Compensation - Task|Loop &amp; Compensation - Task|
|\[Omitted image "bpmn-acitivity-loop-compensation-user-task.png"\] Alt text: Loop &amp; Compensation - User Task|Loop &amp; Compensation - User Task|

## BPMN-Gateway shapes

Gateway shapes control how the process flow splits and merges. Gateways can be resized on the canvas.

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-gateway-complex.png"\] Alt text: Complex|Complex|
|\[Omitted image "bpmn-icon-gateway-default.png"\] Alt text: Default|Default|
| |Event|
| |Event Based \(Start\)|
|\[Omitted image "bpmn-icon-gateway-exclusive.png"\] Alt text: Exclusive|Exclusive|
|\[Omitted image "bpmn-icon-gateway-inclusive.png"\] Alt text: Inclusive|Inclusive|
|\[Omitted image "bpmn-icon-gateway-parallel.png"\] Alt text: Parallel|Parallel|
|||
|||
|||
|||

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-gateway-cancel-end.png"\] Alt text: Cancel \(End\)|Cancel \(End\)|
|\[Omitted image "bpmn-gateway-cancel-bounary-interrupting.png"\] Alt text: Cancel Boundary \(Interrupting\)|Cancel Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-compensation-end.png"\] Alt text: Compensation \(End\)|Compensation \(End\)|
|\[Omitted image "bpmn-gateway-compensation-interrupting.png"\] Alt text: Compensation \(Interrupting\)|Compensation \(Interrupting\)|
|\[Omitted image "bpmn-gateway-compensation-throwing.png"\] Alt text: Compensation \(Throwing\)|Compensation \(Throwing\)|
|\[Omitted image "bpmn-gateway-conditional-boundary-interrupting.png"\] Alt text: Compensation Boundary \(Interrupting\)|Compensation Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-conditional.png"\] Alt text: Conditional|Conditional|
|\[Omitted image "bpmn-gateway-conditional-catching.png"\] Alt text: Conditional \(Catching\)|Conditional \(Catching\)|
|\[Omitted image "bpmn-gateway-conditional-interrupting.png"\] Alt text: Conditional \(Interrupting\)|Conditional \(Interrupting\)|
|\[Omitted image "bpmn-gateway-conditional-non-interrupting.png"\] Alt text: Conditional \(Non-Interrupting\)|Conditional \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-conditional-boundary-interrupting.png"\] Alt text: Conditional Boundary \(Interrupting\)|Conditional Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-conditional-boundary-non-interrupting.png"\] Alt text: Conditional Boundary \(Non-Interrupting\)|Conditional Boundary \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-end.png"\] Alt text: End|End|
|\[Omitted image "bpmn-gateway-error-end.png"\] Alt text: Error \(End\)|Error \(End\)|
|\[Omitted image "bpmn-gateway-error-interrupting.png"\] Alt text: Error \(Interrupting\)|Error \(Interrupting\)|
|\[Omitted image "bpmn-gateway-error-boundary-interrupting.png"\] Alt text: Error Boundary \(Interrupting\)|Error Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-escalation-end.png"\] Alt text: Escalation \(End\)|Escalation \(End\)|
|\[Omitted image "bpmn-gateway-escalation-interrupting.png"\] Alt text: Escalation \(Interrupting\)|Escalation \(Interrupting\)|
|\[Omitted image "bpmn-gateway-escalation-non-interrupting.png"\] Alt text: Escalation \(Non-Interrupting\)|Escalation \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-escalation-boundary-throwing.png"\] Alt text: Escalation \(Throwing\)|Escalation \(Throwing\)|
|\[Omitted image "bpmn-gateway-escalation-boundary-interrupting.png"\] Alt text: Escalation Boundary \(Interrupting\)|Escalation Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-escalation-boundary-non-interrupting.png"\] Alt text: Escalation Boundary \(Non-Interrupting\)|Escalation Boundary \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-intermediate.png"\] Alt text: Intermediate|Intermediate|
|\[Omitted image "bpmn-gateway-link-catching.png"\] Alt text: Link \(Catching\)|Link \(Catching\)|
|\[Omitted image "bpmn-gateway-link-throwing.png"\] Alt text: Link \(Throwing\)|Link \(Throwing\)|
|\[Omitted image "bpmn-gateway-message.png"\] Alt text: Message|Message|
|\[Omitted image "bpmn-gateway-message-catching.png"\] Alt text: Message \(Catching\)|Message \(Catching\)|
|\[Omitted image "bpmn-gateway-message-end.png"\] Alt text: Message \(End\)|Message \(End\)|
|\[Omitted image "bpmn-gateway-message-interrupting.png"\] Alt text: Message \(Interrupting\)|Message \(Interrupting\)|
|\[Omitted image "bpmn-gateway-message-non-interrupting.png"\] Alt text: Message \(Non-Interrupting\)|Message \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-message-boundary-throwing.png"\] Alt text: Message \(Throwing\)|Message \(Throwing\)|
|\[Omitted image "bpmn-gateway-message-boundary-interrupting.png"\] Alt text: Message Boundary \(Interrupting\)|Message Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-message-boundary-non-interrupting.png"\] Alt text: Message Boundary \(Non-Interrupting\)|Message Boundary \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-multiple.png"\] Alt text: Multiple|Multiple|
|\[Omitted image "bpmn-gateway-multiple-catching.png"\] Alt text: Multiple \(Catching\)|Multiple \(Catching\)|
|\[Omitted image "bpmn-gateway-multiple-end.png"\] Alt text: Multiple \(End\)|Multiple \(End\)|
|\[Omitted image "bpmn-gateway-multiple-interrupting.png"\] Alt text: Multiple \(Interrupting\)|Multiple \(Interrupting\)|
|\[Omitted image "bpmn-gateway-multiple-non-interrupting.png"\] Alt text: Multiple \(Non-Interrupting\)|Multiple \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-multiple-start.png"\] Alt text: Multiple \(Start\)|Multiple \(Start\)|
|\[Omitted image "bpmn-gateway-multiple-throwing.png"\] Alt text: Multiple \(Throwing\)|Multiple \(Throwing\)|
|\[Omitted image "bpmn-gateway-multiple-boundary-interrupting.png"\] Alt text: Multiple Boundary \(Interrupting\)|Multiple Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-multiple-boundary-non-interrupting.png"\] Alt text: Multiple Boundary \(Non-Interrupting\)|Multiple Boundary \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-parallel-multiple.png"\] Alt text: Parallel Multiple|Parallel Multiple|
|\[Omitted image "bpmn-gateway-parallel-multiple-catching.png"\] Alt text: Parallel Multiple \(Catching\)|Parallel Multiple \(Catching\)|
|\[Omitted image "bpmn-gateway-parallel-multiple-interrupting.png"\] Alt text: Parallel Multiple \(Interrupting\)|Parallel Multiple \(Interrupting\)|
|\[Omitted image "bpmn-gateway-parallel-multiple-non-interrupting.png"\] Alt text: Parallel Multiple \(Non-Interrupting\)|Parallel Multiple \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-parallel-multiple-boundary-interrupting.png"\] Alt text: Parallel Multiple Boundary \(Interrupting\)|Parallel Multiple Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-parallel-multiple-boundary-non-interrupting.png"\] Alt text: Parallel Multiple Boundary \(Non-Interrupting\)|Parallel Multiple Boundary \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-signal.png"\] Alt text: Signal|Signal|
|\[Omitted image "bpmn-gateway-signal-catching.png"\] Alt text: Signal \(Catching\)|Signal \(Catching\)|
|\[Omitted image "bpmn-gateway-signal-end.png"\] Alt text: Signal \(End\)|Signal \(End\)|
|\[Omitted image "bpmn-gateway-signal-interrupting.png"\] Alt text: Signal \(Interrupting\)|Signal \(Interrupting\)|
|\[Omitted image "bpmn-gateway-signal--non-interrupting.png"\] Alt text: Signal \(Non-Interrupting\)|Signal \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-signal-throwing.png"\] Alt text: Signal \(Throwing\)|Signal \(Throwing\)|
|\[Omitted image "bpmn-gateway-signal-boundary-interrupting.png"\] Alt text: Signal Boundary \(Interrupting\)|Signal Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-signal-boundary-non-interrupting.png"\] Alt text: Signal Boundary \(Non-Interrupting\)|Signal Boundary \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-start.png"\] Alt text: Start|Start|
|\[Omitted image "bpmn-gateway-terminate.png"\] Alt text: Terminate|Terminate|
|\[Omitted image "bpmn-gateway-timer.png"\] Alt text: Timer|Timer|
|\[Omitted image "bpmn-gateway-timer-catching.png"\] Alt text: Timer \(Catching\)|Timer \(Catching\)|
|\[Omitted image "bpmn-gateway-timer-interrupting.png"\] Alt text: Timer \(Interrupting\)|Timer \(Interrupting\)|
|\[Omitted image "bpmn-gateway-timer-non-interrupting.png"\] Alt text: Timer \(Non-Interrupting\)|Timer \(Non-Interrupting\)|
|\[Omitted image "bpmn-gateway-timer-boundary-interrupting.png"\] Alt text: Timer Boundary \(Interrupting\)|Timer Boundary \(Interrupting\)|
|\[Omitted image "bpmn-gateway-timer-boundary-non-interrupting.png"\] Alt text: Timer Boundary \(Non-Interrupting\)|Timer Boundary \(Non-Interrupting\)|

|Shape|Name|
|-----|----|
|\[Omitted image "bpmn-icon-pool.png"\] Alt text: Pool|Pool|
|\[Omitted image "bpmn-icon-lane.png"\] Alt text: Lane|Lane|

**Parent Topic:**[Shapes to create a modeling diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-modeling-shapes.md)

