---
title: Submit privacy requests using external-facing PDR form
description: Submit a privacy request through your organization's external-facing Personal Data Rights \(PDR\) form, either for yourself or as an authorized agent acting on behalf of someone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/submit-privacy-request-external-pdr.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [PDR external-facing form, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Submit privacy requests using external-facing PDR form

Submit a privacy request through your organization's external-facing Personal Data Rights \(PDR\) form, either for yourself or as an authorized agent acting on behalf of someone.

## Before you begin

Role required: none

This form is generally embedded into an organization's website and is publicly available to customers, ex-employees, and third-party Individuals.

## About this task

The external-facing PDR form adapts to where you're submitting from and who the data subject is. The country and, where applicable, the state you select determines which privacy rights are available to you.

If you're submitting on behalf of someone else as an authorized agent, the form asks for both your details and the data subject's details, and you receive a follow-up email asking for proof of authorization before the request is processed.

After submitting your privacy request, verify your email address using a six-digit code. On successful verification, your request is processed and you receive an acknowledgment email with your PDR case number. See [Privacy data request fulfillment workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/privacy-req-fulfill-workflow.md).

## Procedure

1.  Append `/now/grc/portal/public/pdr` to your organization's ServiceNow instance URL \(for example, `https://<instance-name>.service-now.com/now/grc/portal/public/pdr`\).

2.  From the **Language** drop-down, select the language you want to view the form in.

3.  In the **Country** field, select your country of residence.

4.  If applicable, select your state or region.

    The form automatically displays the privacy rights available for your jurisdiction.

5.  On the **Request information** and **Requester details** pages of the form, fill in the fields.

    For field descriptions, see [External-facing PDR form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/ext-form-intake-fields.md).

6.  Review the information you entered, and select **Continue**.

    A six-digit verification code is sent to your email address.

7.  Enter the six-digit verification code, and select **Submit**.


## Result

After successful verification, your privacy request is submitted for processing, and you receive an acknowledgment email with your PDR case number. If you submitted as an authorized agent, you receive an email asking you to provide proof of authorization for the request. After that proof is validated, the privacy team reviews the request and responds within the timeframe required by applicable privacy laws.

**Note:** If you enter the verification code incorrectly or skip it, the request is not processed. For security reasons, you can't retry the code on the same submission. Start a new request if verification fails. This protects your data and the organization's systems from unauthorized or repeated attempts.

