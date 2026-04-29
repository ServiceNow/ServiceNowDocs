---
title: Request provisioning of an SFDC org with a CPQ environment
description: Learn how to submit a request through CPQ Support for environment setup.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ with other apps, Integrate, Sales and Order Management]
---

# Request provisioning of an SFDC org with a CPQ environment

Learn how to submit a request through CPQ Support for environment setup.

## Before you begin

Role required: admin

## Procedure

1.  Install Salesforce CPQ version 244 or later.

2.  Provide the email address associated with a user in the org who will serve as the first Admin user.

    This user will grant other users access after they appear in the User Access list of users after attempting to log in.

3.  Create a user in the desired SFDC org for CPQ provisioning.

    Set the user's email to provisioning@logik.io. This user should have permissions to install packages. If a CPQ user cannot be created, provide the My Domain URL of the org as well.

4.  Log a case by using the Support Center or by sending an email message to support@logik.io with the subject "New Environment Request." Provide the following details:

    -   The SFDC org ID \(Setup → Settings → Company Settings → Company Information → Salesforce.com Organization ID\)
    -   A short note explaining that you created a user with email provisioning@logik.io and that we need to retrieve these credentials
    -   The My Domain URL of the org and the org ID, if a CPQ user cannot be created
    CPQ Support and DevOps will notify you when the work is complete.


