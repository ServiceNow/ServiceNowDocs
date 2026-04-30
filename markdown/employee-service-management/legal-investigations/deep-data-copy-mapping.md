---
title: Data mapping fields
description: Data mapping of tables is necessary when ethics matter is transferred by the legal fulfiller to HR and an HR Employee Relations case is transferred to the Legal department.
locale: en-US
release: zurich
product: Legal Investigations
classification: legal-investigations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Data mapping fields

Data mapping of tables is necessary when ethics matter is transferred by the legal fulfiller to HR and an HR Employee Relations case is transferred to the Legal department.

## Involved Party

Legal Table: sn\_lg\_investigate\_involved\_party.

HR Table: sn\_hr\_er\_involved\_party.

|Legal Fields|HR Fields|
|------------|---------|
|external\_user|not\_in\_system|
|type|type|
|internal\_party|user|
|external\_party|name|

## Allegations

Legal Table: sn\_lg\_investigate\_allegation​.

HR Table: sn\_hr\_er\_allegation.

|Legal Fields|HR Fields|
|------------|---------|
|allegation\_type|allegation\_type|
|allegation\_subtype|allegation\_subtype|
|description|description|

## Subjects of Allegation

Legal Table: sn\_lg\_investigate\_m2m\_allegation\_party.

HR Table: sn\_hr\_er\_m2m\_allegation\_party.

|Legal Fields|HR Fields|
|------------|---------|
|involved\_party|involved\_party|
|allegation|allegation|
|outcome|outcome|

## Evidence/Artifact​

Legal Table: sn\_lg\_matter artifact​.

HR Table: sn\_em\_evidence​.

|Legal Fields|HR Fields|
|------------|---------|
|sn\_lg\_matter\_artifact.short\_description|name|
|involved\_party\_users|subjects\_of\_allegation|
|submitted\_by|submitted\_by\_involved\_party|

## Evidence of type link​

Legal Table: sn\_lg\_matter\_artifact\_external\_storage.

HR Table: sn\_em\_evidence.

|Legal Fields|HR Fields|
|------------|---------|
|sn\_lg\_matter\_artifact\_external\_storage.short\_description|name|
|link|url source|

## Interviews

Legal Table: sn\_lg\_matter task.

HR Table: sn\_hr\_er\_interview.

|Legal Fields|HR Fields|
|------------|---------|
|involved\_party|interviewee|
|interview\_notes|notes|

## Corrective/Recommended Actions

Legal Table: sn\_lg\_matter task.

HR Table: sn\_hr\_er\_corrective action.

|Legal Fields|HR Fields|
|------------|---------|
|involved\_party|involved\_party|
|also\_present|also\_present|
|discussion\_date|discussion\_date|
|description|description|
|state|status|
|recommended\_action\_type|corrective\_action\_type|
|due\_date|due\_date|

**Note:** The **Description** field includes **Assigned to** or **Discussion held by** fields for user name.

**Parent Topic:**[Legal Investigations reference](legal-investigations-reference.md)

