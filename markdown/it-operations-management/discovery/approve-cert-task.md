---
title: Approve certificate tasks
description: Sometimes you need to manually approve a certificate task to ensure the validity and security of TLS certificates.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Approve certificate tasks

Sometimes you need to manually approve a certificate task to ensure the validity and security of TLS certificates.

## Before you begin

Role required: admin

## About this task

If the approval is requested for a routing policy, select the routing policy created. Approvals are only supported in the Fulfiller approval experience at this time.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Approval**.

2.  Open the automatically created approval task.

3.  Check the new certificate details and **Choose Routing Policy &amp; Approve**.


## Result

1.  The automated flow for requesting a new certificate is initiated.
2.  You can open the certificate task by navigating to **Certificate Management** &gt; **New Certificate Task**.
3.  Ensure that the automated flow is triggered.
4.  If the CA approves the certificate request, both the Order ID and Certificate ID are retrieved for the newly requested certificate. If the CA does not approve, only the Order ID is fetched.

    **Note:** For Entrust CA Gateway, Certificate Serial Number and Enrollment Id are fetched.


