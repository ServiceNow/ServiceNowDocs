---
title: Customer Signature Required activity not displaying or WSUD verification task not getting generated
description: This reference topic provides troubleshooting steps to resolve the Customer Signature Required activity not appearing in the playbook. It also resolves the Written Statement for Unauthorized Debit \(WSUD\) document verification task not being generated.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: topic
last_updated: "2022-08-11"
reading_time_minutes: 1
breadcrumb: [WSUD Troubleshooting, Reference, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Customer Signature Required activity not displaying or WSUD verification task not getting generated

This reference topic provides troubleshooting steps to resolve the Customer Signature Required activity not appearing in the playbook. It also resolves the Written Statement for Unauthorized Debit \(WSUD\) document verification task not being generated.

## Condition

The **Customer Signature Required** activity doesn't display in the playbook, or the WSUD document verification task isn't generated.

## Remedy

## Procedure

1.  Verify that a dispute was created for at least one Debit transaction.

2.  Ensure the [Dispute Rules Content Pack for Nacha](../../dispute-content-pack-for-nacha/concept/dispute-rules-content-pack-for-nacha.md) is installed.

3.  Verify whether the reason code is eligible for WSUD.

4.  Confirm that a Contact was provided while creating the case for an Account.


**Parent Topic:**[Written Statement for Unauthorized Debit \(WSUD\) Troubleshooting](../concept/wsud-troubleshooting-reference.md)

