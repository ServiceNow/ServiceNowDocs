---
title: Service Level Management glossary
description: Learn about the terms and concepts used in Service Level Management.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-level-management/glossary-itsm-service-level-management.html
release: brazil
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-11-19"
reading_time_minutes: 4
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Service Level Management glossary

Learn about the terms and concepts used in Service Level Management.

**Parent Topic:**[Service Level Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/service-level-management/service-level-management-reference.md)

## A

Glossary terms are grouped alphabetically.

### actual elapsed time

In Service Level Management, the time accumulated on a task SLA, calculated on a 24x7 basis regardless of the SLA schedule.

## B

Glossary terms are grouped alphabetically.

### breach time

In Service Level Management, the date and time on a task SLA by which the SLA must be completed before it's marked as breached.

### business elapsed time

In Service Level Management, the time accumulated on a task SLA based on the schedule in the task SLA. If no schedule is specified, it equals the actual elapsed time.

### business time left

In Service Level Management, the business time remaining by which a task SLA must be completed.

## D

Glossary terms are grouped alphabetically.

### Default SLA flow

The base system flow in Service Level Management that creates events to send notifications, for example when a task SLA reaches 50% of its allotted time.

## E

Glossary terms are grouped alphabetically.

### Escalation engine

The pre-2010 Service Level Management SLA engine that tracks only one SLA per task, using the SLA Due, Made SLA, and Escalation fields on the task table.

## O

Glossary terms are grouped alphabetically.

### operational level agreement

In Service Level Management, a non-contractual agreement type that tracks service levels internal to the organization.

#### OLA

## R

Glossary terms are grouped alphabetically.

### relative duration

A Service Level Management SLA duration type that is relative to the task SLA start time and defined by a script, such as Next business day by 4pm.

### retroactive pause

An SLA definition option in Service Level Management that adds the pause time accumulated since the retroactive start time to a new task SLA, which moves the breach time later.

### retroactive start

An SLA definition option in Service Level Management that takes the task SLA start time from a date and time field on the task, such as Created or Opened.

## S

Glossary terms are grouped alphabetically.

### schedule source

An SLA definition field in Service Level Management that specifies where the schedule for new task SLAs comes from: No schedule, the SLA definition, or a task table field.

### service contract

In Service Level Management, a contract record \[ast\_service\] that groups the SLAs for a single vendor or customer, along with its related CIs, locations, groups, users, and child contracts.

### sla\_admin

The Service Level Management role with full administrative rights, such as configuring SLM properties, running SLA repair, and managing SLA definitions.

### SLA breakdown

A Service Level Management feature that shows task ownership and SLA duration data for task SLA records, to identify which teams and users contribute to SLA compliance.

### SLA condition

One of up to six criteria on a Service Level Management SLA definition \(start, cancel, pause, resume, stop, reset\) that set when a task SLA is attached, paused, resumed, reset, canceled, or completed.

### SLA condition rule

In Service Level Management, a rule that controls how SLA definition conditions combine to attach, pause, complete, reattach, or cancel an SLA. It's defined globally and can be overridden per SLA definition.

### SLA definition

In Service Level Management, a record that defines the timings, conditions, workflows, and other information required to create and progress task SLAs.

### SLA engine

The Service Level Management engine that evaluates SLA definitions and their conditions against a task to create task SLA records and change their stage.

### sla\_manager

The Service Level Management role that lets users define SLA definitions and view SLA repair logs and the SLA Overview dashboard, but not change SLM properties.

### SLA repair

A Service Level Management function that removes a task SLA record, then recreates and recalculates it from the start using the task history, to correct timing information.

### SLA timeline

A Service Level Management feature that shows the task updates that triggered stage changes during the life cycle of a task SLA.

### SLA timer

A Service Level Management component that visually displays the current stage of a task SLA, such as In-progress, Paused, or Breached.

### SLA timer configuration

In Service Level Management, a configuration record that determines which task SLA appears in the SLA timer component, such as First to breach or Task to SLA mapping.

### SLA transition

In Service Level Management, a change that a task SLA goes through during processing: attach, pause, resume, complete, reattach, or cancel.

### SLAConditionBase

The Service Level Management script include that implements the default SLA transitions and serves as the default set of SLA condition rules.

## T

Glossary terms are grouped alphabetically.

### task SLA

In Service Level Management, the record generated when an SLA definition is triggered against a task, holding all the tracking data for that SLA \[task\_sla\].

### time zone source

An SLA definition field in Service Level Management that specifies which time zone is used for schedule calculation, such as the caller's time zone.

## U

Glossary terms are grouped alphabetically.

### underpinning contract

In Service Level Management, an agreement type processed as a non-contractual SLA, whose progress can be tracked alongside SLAs and OLAs.

### user specified duration

A Service Level Management SLA duration type that sets a static duration, such as 8 hours, along with a business schedule.

