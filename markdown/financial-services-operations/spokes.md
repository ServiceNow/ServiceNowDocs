---
title: Integrating with spokes
description: By integrating spokes with the Financial Services Operations \(FSO\) applications, flow designers can provide the actions within Workflow Studio for specific applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/financial-services-operations/spokes.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating applications, Financial Services Operations \(FSO\)]
---

# Integrating with spokes

By integrating spokes with the Financial Services Operations \(FSO\) applications, flow designers can provide the actions within Workflow Studio for specific applications.

A spoke is a scoped application containing Workflow Studio content dedicated to a particular application or record type. You can integrate a ServiceNow application with a FSO banking application spoke such as Jack Henry jXchange Socure, or FRISS.

|Plugin name|Description|Plugin directory|
|-----------|-----------|----------------|
||By using the Equifax spoke integration, you can access important information about the credit history for a customer, fraud alerts, digital identity verification, transaction screening, and other relevant data.|\[com.sn\_equifax\_spoke\]|
||By using the Ethoca spoke integration, you can access detailed merchant information and subscription control, view digital receipts, and manage their disputes.|\[com.sn\_ethoca\_spoke\]|
||Flow designers can use the Jack Henry jXchange spoke to access the actions to automate the financial processes within ServiceNow. You can use this integration to do tasks such as account management, transaction processing, or fraud detection.|\[com.sn.jha.spoke\]|
||By using the Socure spoke integration, you can improve your customer onboarding, authentication processes and for identity verification tasks. Flow designers can incorporate these identity verification processes into their workflows. Tasks include validating user information, performing risk assessments, or preventing fraudulent activities.|\[com.sn\_socure\_spoke\]|
||By using the Mastercard spoke integration, you can perform tasks such as searching transactions, creating claims, and processing chargebacks.|\[com.sn\_mastercard\_spoke\]|
||Dispute agents can use the  to seamlessly invoke Visa APIs under Visa Resolve Online \(VROL\) for Visa card dispute process.|\[com.sn\_visa\_spoke\]|
||Dispute agents can use the  to resolve disputes at the pre-dispute stage, prevent formal disputes and costly chargebacks, and manage the dispute resolution process more effectively and efficiently.|\[com.sn\_verifi\_spoke\]|

|Spoke|Description|Plugin|
|-----|-----------|------|
||The FRISS spoke enables insurance companies to enhance their fraud prevention measures and protect their organizations from financial losses. It provides the actions that are designed for fraud prevention and risk assessment tasks. Flow designers can incorporate the fraud detection processes into their workflows by using actions. Actions include analyzing the customer data, identifying suspicious activities, and generating fraud alerts.|\[com.sn\_friss\_spoke\]|
||The Guidewire spoke integration provides actions within Workflow Studio for managing insurance-related tasks. The spoke actions include creating policies, updating claims information, and retrieving billing data.|\[com.sn\_guidewire\_spoke\]|

**Parent Topic:**[Integrate applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/fso-integrate-other-applications.md)

