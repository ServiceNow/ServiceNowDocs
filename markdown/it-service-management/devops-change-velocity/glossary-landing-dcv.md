---
title: DevOps Change Velocity glossary
description: Learn about the terms and concepts in DevOps Change Velocity.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.Glossary terms are grouped alphabetically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/devops-change-velocity/glossary-landing-dcv.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 3
keywords: [glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms, glossary terms]
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# DevOps Change Velocity glossary

Learn about the terms and concepts in DevOps Change Velocity.

**Parent Topic:**[DevOps Change Velocity reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/devops-change-velocity/devops-change-velocity-reference.md)

## A

Glossary terms are grouped alphabetically.

### Accelerate metrics

The four DevOps Insights metrics that measure software delivery performance in DevOps Change Velocity. Deployment frequency and lead time measure speed, while change failure rate and mean time to recovery measure stability.

### artifact package

A named grouping of artifact versions in DevOps Change Velocity that is deployed together. The package and its artifact versions determine which commits are included in the associated change request.

### artifact version

A registered version of a build output in DevOps Change Velocity, associated with the commits that were built into it. Artifact versions are used to determine which commits appear in a change request.

## C

Glossary terms are grouped alphabetically.

### change acceleration

The DevOps Change Velocity capability that creates change requests automatically from a pipeline. It uses change approval flows and change approval policies to approve those change requests under conditions that you define.

### change receipt

A pipeline step setting in DevOps Change Velocity that creates a change request without pausing the pipeline for approval. The change request includes all pipeline data and is placed in a post-implementation state.

### committer risk score

A score assigned to a committer in DevOps Change Velocity. The DevOps risk condition uses it to calculate the risk and impact of a change request.

## D

Glossary terms are grouped alphabetically.

### DevOps change model

A base system change model in DevOps Change Velocity with the states New, Assess, Authorize, Scheduled, Implement, Review, Closed, and Canceled. Each state has its own flow that runs when the required conditions are met.

### DevOps Simplified change model

A base system change model in DevOps Change Velocity with a shorter state path than the DevOps change model. Its states are New, Authorize, Scheduled, Implement, Review, Closed, and Canceled, omitting the Assess state.

## I

Glossary terms are grouped alphabetically.

### import based evidence collection

A DevOps Change Velocity setting that attaches pipeline evidence to a change request using import requests instead of step-level webhook notifications. Enabling it reduces instance overhead by skipping step-level pipeline processing.

### import request

A record in DevOps Change Velocity that imports plan, repository, and pipeline data from a connected tool, either on demand or on a polling schedule. Each import request is processed as a set of import request pages.

### inbound event

A record created in DevOps Change Velocity when a connected tool sends a notification to the instance. Inbound events are processed by the base system subflows associated with the event's capability.

## M

Glossary terms are grouped alphabetically.

### manual configuration mode

A mode in DevOps Change Velocity that lets you set a tool connection's state yourself instead of configuring the webhook automatically. Use it when you have only read-only permission to the tool and an administrator adds the instance to the webhook for you.

## R

Glossary terms are grouped alphabetically.

### run commits

The commits that DevOps Change Velocity identifies as having been built by a particular job or pipeline run. For a commit to appear as a run commit, its commit record must already exist in ServiceNow before the run starts.

## S

Glossary terms are grouped alphabetically.

### step execution

A record of a single pipeline step's run in DevOps Change Velocity. Its state drives the callback that resumes, terminates, or cancels the pipeline after a change request is approved, rejected, or canceled.

## T

Glossary terms are grouped alphabetically.

### task execution

A record of a job run within a pipeline execution in DevOps Change Velocity. Run commits and the test, software quality, and security results produced by the job are associated to it.

### type compatibility flag

A property that controls whether DevOps Change Velocity can create change requests from a change type as well as a change model. When it is set to false, change requests are created only from a change model.

