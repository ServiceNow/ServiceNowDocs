---
title: Change Management glossary
description: Learn about the terms and concepts used in Change Management.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/glossary-itsm-change-management.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-11-06"
reading_time_minutes: 10
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Change Management glossary

Learn about the terms and concepts used in Change Management.

**Parent Topic:**[Reference section for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/reference-change-management.md)

## A

Glossary terms are grouped alphabetically.

### Advanced Security \(change model\)

Allows user criteria in addition to role-based access to specify who can create changes from the change model and who can edit the change model configuration.

### affected CI

A CI in the affected CIs related list of a change. Specifies the CIs that are in scope for implementing the change.

### Allow Child Change Creation

Change model state attribute that must be active on a primary change model state to create child changes when a primary change enters that state. Normally used with Scaled Change.

### Allow CI Modification

A change model state attribute \(allow\_ci\_modification\) that determines the states in which the configuration item and affected CIs on a change can be modified.

### Allow Implementation

A change model state attribute \(allow\_implementation\) that determines the states in which proposed CI changes can be applied from a change request.

### approval definition

A set of criteria in a change approval policy that determines whether an approval is user-based or group-based, whether it's approved or rejected automatically, and whether a response is required.

### Approval with e-Signature

A Change Management capability that lets approvers verify their identity with e-signatures when approving change requests and standard change proposals.

### automatic transition

A model state transition option that moves the change request automatically when its conditions are met and prevents manual selection of the State field.

### Automatically Add Change Requests

A CAB definition option that automatically adds change requests matching the Change Request Addition Conditions to the CAB meeting agenda.

## B

Glossary terms are grouped alphabetically.

### blackout schedule

A schedule associated with a blackout window that specifies times during which normal change activity should not be scheduled, such as code freezes at the end of the year.

### blackout window

A schedule period against which conflict detection checks a change request, including the windows of parent and child CIs.

## C

Glossary terms are grouped alphabetically.

### CAB agenda item

An entry that connects a change request or standard change proposal to the CAB meeting where it is reviewed.

### CAB definition

A Change Management record \(cab\_definition\) that defines a Change Advisory Board and sets the attributes of all CAB meetings generated from it.

### CAB Workbench

The Change Management interface that a CAB manager uses to schedule, plan, and run Change Advisory Board meetings, including agenda, attendees, and approvals.

### Calculated Risk Score

A lookup \(sn\_chg\_probability\_risk\_lookup\) that maps banded success probability values \(High, Medium, Low\) against impact to give the risk value of a change request.

### Change Advisory Board

A group that meets to review and authorize change requests and review recently implemented changes in Change Management.

#### CAB

### change approval policy

A Change Management policy that evaluates policy inputs against the conditions on its decisions and applies the associated approval definition to generate the required approvals.

### Change Approval Policy workflow activity

A workflow activity that controls the approval process for a change request by creating user and group approvals according to a change approval policy record.

### change lockdown

A Change Management record that pauses in-flight change requests during major unplanned IT, critical, or financial events; only an enforced lockdown places matched changes on hold.

### Change Management Worker

A table \(chg\_mgt\_worker\) that tracks the execution of conflict detection and the asynchronous creation of Child change requests.

### change model

A definition of the states a change request moves through, the transitions and conditions between them, and related elements such as approval policies and templates, tailored to a change use case.

### change model attribute

A tag assigned to a state in a change model that scripts can check to turn functionality on or off for that state.

### change model category

A category and child category that define a hierarchy of change models.

### Change Model Success

A success probability method, based on the model of the change request, that shows the percentage of successful changes for each change model and type.

#### CMS

### Change Risk Calculator

A Change Management method that uses predefined properties and conditions to calculate the risk value of a change request.

### change schedule

A timeline view of change requests, change tasks, blackout periods, and maintenance windows, based on criteria set in a change schedule definition.

### change schedule definition

A record that defines the configuration options and related records used to display a change schedule.

### change success score

A score based on a team's historical data that indicates how likely an assignment group is to complete a change request without issues.

### Change Success Score card

A card next to the Assignment group field on the change request form that shows the success score details of the assignment group.

### change task

A piece of work related to a change request, such as planning, implementing, testing, or reviewing the change.

### change template

A template, created from a change model, that provides predefined field values and field policies for common change requests.

### Child change

A change request generated from a Primary change for one affected CI that copies key fields from the Primary change.

### Child change model

A change model that defines the states required by the Child changes generated from a Primary change model's flow.

### compliance dynamic schema

A Change Management feature that stores the risk and compliance details of a change as name and value pairs in a single field of the Change Request table.

### conflict calendar

A graphical view of potential scheduling conflicts for a change request, including other changes, blackout schedules, and changes outside maintenance schedules.

### conflict detection

A Change Management process that checks a change request's schedule against blackout schedules, maintenance schedules, and other change requests for the same CIs.

### Copy Change

A change request form action that copies details of an active or canceled change request to a new one.

## D

Glossary terms are grouped alphabetically.

### decision

A record in a change approval policy that holds conditions referencing policy inputs and applies an associated approval definition.

### dynamic attribute

An attribute defined in the compliance dynamic schema namespace that has an enforced type, can offer choice values, and can belong to a dynamic category.

## E

Glossary terms are grouped alphabetically.

### emergency change

A high-priority change implemented immediately to resolve a major incident or apply a security patch; it bypasses group and peer review and goes to the Authorize state for CAB approval.

### Evaluate Change Model

A flow action that evaluates a change request against its change model, determines whether the state should change, and changes it if a condition matches.

### Exclude from conflict detection

A change request check box that makes conflict detection unavailable for that change request and excludes it as a conflict for other changes.

## F

Glossary terms are grouped alphabetically.

### flapper algorithm

An algorithm that uses a learning pattern to identify false positives in CI property changes so they don't trigger unauthorized change requests.

## I

Glossary terms are grouped alphabetically.

### Impacted Services/CIs

A related list on a change request that shows the business services, other CIs, and service offerings impacted by the affected CIs.

### Inside Change Lockdown

A conflict type reported when a change request falls inside an active lockdown period; the change request is placed on hold automatically.

### ITIL change process assignment

A setting where a change manager designates an active change model to represent the Normal, Standard, or Emergency ITIL change process used by the ChangeRequest API.

## M

Glossary terms are grouped alphabetically.

### maintenance schedule

A schedule that specifies the periods during which change requests should be scheduled; a change that does not adhere to it generates a conflict.

### Mass Update CI

A Change Management feature that applies the same update to all CIs of a selected CI class from a change request.

### model state

A state defined within a change model, with its own attributes, state transitions, and state field policies.

### model state transition

A defined movement of a change request from one model state to another, which can be automatic and can carry transition conditions.

## N

Glossary terms are grouped alphabetically.

### Next Generation Change Risk

A risk evaluation technique that uses Impact and Success Probability parameters for a data-driven calculation of change risk.

### normal change

A service change that is not a standard or emergency change and requires assessment, approval, and CAB authorization before implementation.

## P

Glossary terms are grouped alphabetically.

### policy input

A variable source in a change approval policy, such as a change field or referenced record value, that is evaluated by the conditions on a decision.

### predefined transition condition type

A reusable condition, defined with the condition builder or a script, that can be referenced from the transition conditions of any change model.

### Predictive Intelligence for Change Management

A Change Management capability that uses machine-learning algorithms to suggest standard change templates and enhance change risk assessment.

### Primary change

A change request that holds all affected CIs and generates one Child change per CI when it reaches the configured trigger state.

### Primary change model

A change model configured so that a change using it generates one Child change for each affected CI.

## R

Glossary terms are grouped alphabetically.

### Refresh Impacted Services

An action that populates the Impacted Services/CIs related list and the Service Offerings and Business Applications related lists based on the affected CIs.

### risk and compliance attributes

A change request field that holds risk and compliance details, such as audit trail required, downtime, and rollback time, as name and value pairs.

### risk and compliance category

A change request field that references the hierarchical dynamic category that groups the risk and compliance attributes for a change.

### risk assessment

An optional Change Management method that assesses the risk value of a change using information provided by the end user.

### risk condition

A rule, built with the condition builder or a script, that sets the Risk and Impact values of a change request.

### Risk for proposed change

A Predictive Intelligence solution definition \(Similarity and Categorization type\) that predicts the potential risk of a change.

### Rolling Meeting Window

A CAB definition field that sets the number of days for which CAB meetings are created.

## S

Glossary terms are grouped alphabetically.

### scaled change

A Change Management capability for environments with many CIs, where a single Primary change generates and coordinates a Child change for each affected CI.

### scaled change flow

A flow on a Primary change model that triggers when the Primary change reaches the configured state and creates the Child changes.

### Scheduling Assistant

A conflict calendar component that displays available time slots so you can resolve a scheduling conflict.

### span style

A color applied to change requests or events in a change schedule based on specified conditions, by default reflecting the Risk value.

### standard change

A pre-authorized, low-risk, relatively common change that follows a specified procedure and does not require CAB authorization.

### Standard change candidates

A Predictive Intelligence solution definition \(Clustering type\) that analyzes change clusters and suggests opportunities for standard change templates.

### standard change catalog

A catalog of pre-approved standard change templates from which users request standard changes.

### standard change proposal

A proposal for a new standard change template that the change management team reviews and approves or rejects.

### standard change template

A repeatable, pre-approved template in the standard change catalog; change requests created from it do not require change approval.

### state field policy

A policy on a change model state that makes a change request field mandatory, read-only, or both while the change is in that state.

### State Field Policy Managed

A Mandatory Fields transition condition that the system adds automatically to transitions into a state when a field is made mandatory in a state field policy.

### style rule

A condition-based rule that defines the color of a span or label in a change schedule based on field values.

### success probability

A calculation of the probability of success of a change request using the Change Model Success, Change Success Score, or Calculated method.

### success probability definition

A definition that sets the success probability and matching conditions of a change request, with an order field that sets execution precedence.

### success score rating

A rating \(Low, Medium, High, Excellent\) that maps a calculated success score range to a color and text on the Change Success Score card.

## T

Glossary terms are grouped alphabetically.

### template category

A category and child category used to classify change templates by change model, usage, and requirements.

### threshold enforcement mode

A Major Change property that can be set to warning, which logs the condition and allows Child change generation, or blocking, which logs the condition and stops generation.

### transition condition

A condition that must be fulfilled for a change request to move between model states.

## U

Glossary terms are grouped alphabetically.

### unauthorized change request

A change request the system creates automatically when an unplanned change occurs on a CI that is not part of an open change request.

### user criteria

A record that groups users by role, group, company, location, or department and controls who can view, use, or modify a change model.

