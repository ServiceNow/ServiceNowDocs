---
title: WSUD signing email not sent to customer
description: This reference topic provides troubleshooting steps to resolve a Written Statement for Unauthorized Debit \(WSUD\) not being emailed to a customer during ACH dispute intake.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [WSUD Troubleshooting, Reference, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# WSUD signing email not sent to customer

This reference topic provides troubleshooting steps to resolve a Written Statement for Unauthorized Debit \(WSUD\) not being emailed to a customer during ACH dispute intake.

## Condition

No email is sent to the customer for signing the document.

## Cause

The consumer/contact record may have an invalid or missing email address.

## Remedy

## Procedure

1.  Verify that the Consumer/Contact record has a valid email address.

2.  If the email address is missing or invalid:

    1.  Close the current case.

    2.  Update the contact with a valid email address.

    3.  Recreate the case to trigger the email and document generation process again.


## Alternate remedy - manually send an email link

## Procedure

1.  Manually send the signing link to the consumer's or contact's email address: `http://<BASE URL>/<PORTAL>?id=ticket&table=sn_doc_task&sys_id=<SYS ID>&view=<PORTAL>`

    -   &lt;BASE\_URL&gt;: Instance domain \(for example, `https://mycompany.service-now.com`\)
    -   &lt;PORTAL&gt;: Portal name \(csp or csm only\)
    -   &lt;SYS\_ID&gt;: Unique record ID of the document task

**Parent Topic:**[Written Statement for Unauthorized Debit \(WSUD\) Troubleshooting](../concept/wsud-troubleshooting-reference.md)

