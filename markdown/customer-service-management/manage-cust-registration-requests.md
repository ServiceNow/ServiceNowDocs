---
title: Manage customer registration requests
description: Users with the customer administrator role can approve or reject registration requests that customers submit from the Customer Service Portal.Approve a registration request from a user that was submitted from the Customer Service Portal with a valid registration code.Reject a registration request from a user that was submitted from the Customer Service Portal.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use Customer Service Portal, Customer communication, Use, Customer Service Management]
---

# Manage customer registration requests

Users with the customer administrator role can approve or reject registration requests that customers submit from the Customer Service Portal.

## Approve a registration request with a valid registration code

Approve a registration request from a user that was submitted from the Customer Service Portal with a valid registration code.

### Before you begin

Role required: sn\_customerservice.customer\_admin

### Procedure

1.  Navigate to the customer portal.

2.  Click **Approvals**.

    The Approvals list displays registration requests with these states: **Requested** and **No Longer Required**.

3.  Click a request in the Approvals list with a state of **Requested**.

4.  If desired, add any **Comments** to this request.

5.  Click **Approve**.

    A user account is created and an email is sent to the contact’s email address with a user ID and temporary password. The user is also assigned these roles: sn\_esm\_user and snc\_external.


## Reject a registration request

Reject a registration request from a user that was submitted from the Customer Service Portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin

### Procedure

1.  Navigate to the customer portal.

2.  Click **My Approvals**.

3.  Click a request in the Approvals list with a state of **Requested**.

4.  Click **Reject**.

    An email regarding the rejection is sent to the requestor’s email address.


