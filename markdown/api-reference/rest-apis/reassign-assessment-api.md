---
title: Reassign Assessment API
description: The Reassign Assessment API provides an endpoint to reassign an assessment instance to a different user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/reassign-assessment-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
keywords: [assessment instance management]
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Reassign Assessment API

The Reassign Assessment API provides an endpoint to reassign an assessment instance to a different user.

The Reassign Assessment API runs in the sn\_smart\_asmt namespace. This API is offered by default with the base system.

Use this API to transfer assessment ownership when you need to change which user is responsible for completing an in-progress assessment. This is useful when assessments are initially assigned incorrectly, when an employee changes roles, or when you need to delegate assessment completion to a more appropriate team member.

## Common use cases

-   Transferring assessment responsibility when an employee changes roles or leaves the organization
-   Correcting an incorrectly assigned assessment
-   Delegating assessment completion to a more appropriate team member

## Requirements

The Reassign Assessment API requires the following roles to access it:

-   Users with the sn\_smart\_asmt.actor role who have been assigned the assessment \(only the primary owner\)
-   Assessment requestors with the sn\_smart\_asmt.assessment\_reader role
-   Users with the sn\_smart\_asmt.assessment\_admin role

## Important constraints

-   The assessment must be in the Open state to be reassigned. Assessments in other states can't be reassigned using this endpoint.
-   The requesting user must have write access to the assessment's persona assignment record to perform the reassignment.
-   An assessment can't be reassigned to the user it's currently assigned to.

-   **[Reassign Assessment - PATCH /\{userId\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/reassignassessment-PATCH-userId.md)**  
Reassigns an assessment instance to a different user. Use this endpoint when you need to transfer ownership of an in-progress assessment from the current assignee to another user.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/api-rest.md)

